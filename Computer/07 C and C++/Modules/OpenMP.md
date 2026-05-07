# 01 环境搭建与基础编译

OpenMP 是一种为共享内存环境（如多核/处理器）设计的**并行编程 API**，支持 **C/C++ 和 Fortran** 语言。由于其指令内置于主流编译器中，被公认为最简单、最便携的多线程方法之一。它的标准化也在不断演进，例如 [OpenMP 5.2](https://www.openmp.org/wp-content/uploads/OpenMP-Ref-Card-5.2-bookmarks.pdf) 版本完善了基于拓扑的亲和性支持等功能。

*   **编译器支持与启用**：OpenMP 需要编译器支持。主流编译器版本及启用方式如下：
    *   **GCC / Clang**：在编译命令中添加 `-fopenmp` 参数。
		```bash
		g++ -fopenmp -O2 main.cpp -o main
		```
    *   **MSVC (Visual Studio)**：在项目属性页的 `C/C++` → `语言` 中，将 “OpenMP 支持” 设为 “是”。命令行编译可使用 `/openmp` 开关。
    *   **Intel 编译器**：在 Linux 上使用 `-openmp`，在 Windows 上使用 `/Qopenmp`。

> [!NOTE] 关键细节
> *   **编译器版本**：确保你的 GCC ≥ 4.2, Clang ≥ 3.7, MSVC ≥ 2015。
> *   **环境检查**：若不确定环境是否支持，可检查 `_OPENMP` 宏。若未定义，说明 OpenMP 未正确开启。

---

# 02 第一个 OpenMP 程序与并行区（Hello World）

OpenMP 的强大之处在于你只需在代码中插入简单的特殊标记（Pragmas），编译器就会自动为你处理复杂的线程管理、任务分配和同步等底层细节。

**Fork-Join 模型**
OpenMP 采用 **Fork-Join** 并行模型。程序开始时作为主线程执行，当遇到 `parallel` 构造时，会 **Fork（创建）** 一组线程并行执行任务。任务完成后，这些线程 **Join（汇合）**，程序恢复为主线程串行执行。

**基础示例**
```cpp
#include <iostream>
#include <omp.h> // 包含 OpenMP 头文件

int main() {
    // 1. 创建一个并行区，大括号内的代码由多个线程同时执行
    #pragma omp parallel
    {
        int thread_id = omp_get_thread_num(); // 获取线程ID (从0开始)
        int num_threads = omp_get_num_threads(); // 获取总线程数
        std::cout << "Hello from thread " << thread_id 
                  << " of " << num_threads << " threads." << std::endl;
    }
    return 0;
}
```
这段代码演示了如何创建一个并行区，让每个线程执行相同的代码块。

> [!TIP] 实用建议
> *   **控制线程数**：可以通过 `num_threads(4)` 子句指定线程数，或使用 `omp_set_num_threads(4)` 函数。
> *   **“Hello World” 乱序输出**：由于多个线程同时写 `std::cout`，输出顺序不确定且可能交织。这是并行编程的典型现象，说明输出流是**共享资源**，需要保护。

---

# 03 核心：循环并行化（Loop Parallelization）

将循环并行化是 OpenMP 最强大、最常用的功能之一，尤其适合处理大量独立迭代的计算密集型任务。

## 3.1 `parallel for` 指令

此指令将 `parallel` 和 `for` 结合，专门用于将循环迭代分发给线程组。

```cpp
std::vector<int> data(100000, 43);
// 注意：循环变量 i 是 private 的，每个线程有自己的副本
#pragma omp parallel for
for (size_t i = 0; i < data.size(); ++i) {
    // 1. 每次迭代必须独立：data[i] 属于不同的线程，安全
    // 2. 不要在循环内使用 break 等改变控制流
    data[i] = data[i] * data[i]; 
}
```

> [!WARNING] 线程安全细节
> *   **必须是标准 for 循环**：`parallel for` 只能用于形如 `for (init; condition; increment)` 的标准 for 循环，不支持基于范围的 for 循环。
> *   **数据依赖**：务必确保循环的各次迭代之间没有数据依赖关系（在循环迭代间的循环携带依赖，或跨并行区的跨迭代依赖），否则会导致数据竞争。

## 3.2 归约操作 (`reduction`)

当需要在并行循环中跨线程安全地汇总变量时，应使用 `reduction` 子句，而非易出错的 `critical` 或 `atomic`。

```cpp
int sum = 0;
// reduction(+:sum) 会为每个线程创建 sum 的私有副本，最后通过 '+' 操作合并
#pragma omp parallel for reduction(+:sum)
for (int i = 0; i < 1000; ++i) {
    sum += expensive_computation(i);
}
// 支持的操作：+, *, -, &, |, ^, &&, ||, min, max
```

---

# 04 任务调度与工作区共享

## 4.1 调度策略 (`schedule` 子句)

调度策略决定了循环迭代如何分配给线程，对负载不均衡的循环性能影响巨大。可通过 `time` 命令或专用图直观对比它们的差异。
*   **`static`** (默认)：编译时预分配连续块。线程创建和通信开销极小。
*   **`dynamic`**：运行时动态分发。可结合 `chunk_size` 避免频繁分发。
*   **`guided`**：块大小逐渐减小，是 `static` 和 `dynamic` 的折中方案。同样支持 `chunk_size` 参数。

```cpp
// schedule(类型, 块大小)  // 示例
#pragma omp parallel for schedule(dynamic, 32)
for (int i = 0; i < N; ++i) { /* 每次给空闲线程分配32次迭代 */ }
```
*   **图例对比**：如下图所示，不同的调度策略在负载均衡和通信开销间做了不同的权衡。
    ```mermaid
    graph LR
        subgraph Static
            direction LR
            A1[线程 0: 0-249] --- A2[线程 1: 250-499] --- A3[线程 2: 500-749] --- A4[线程 3: 750-999]
        end

        subgraph Dynamic
            direction LR
            B1[线程 0: 0-31] --- B2[线程 1: 32-63] --- B3[线程 0: 128-159] --- B4[线程 2: 64-95] 
        end

        style Static fill:#f9f,stroke:#333,stroke-width:2px
        style Dynamic fill:#ccf,stroke:#333,stroke-width:2px
    ```

    *图例说明：`static` 策略各线程任务块连续且固定；`dynamic` 策略各线程以小块为单位动态争抢任务。*

## 4.2 `sections` 指令

用于并行执行多个功能不同但彼此独立的代码块。通过 `#pragma omp section` 来界定。

```cpp
#pragma omp parallel sections
{
    #pragma omp section
    { task_a(); }
    #pragma omp section
    { task_b(); }
}
```

## 4.3 `single` 指令

指定一个并行区内，某段代码只由一个线程执行一次，其他线程会等待或被 `nowait` 子句跳过。常用于 I/O 或初始化。

```cpp
#pragma omp parallel
{
    compute();
    #pragma omp single
    { std::cout << "Result: " << result << std::endl; }
}
```

---

# 05 数据共享与同步

**错误的数据共享**是**数据竞争**及其他并行 bug 的根源，这是最需要谨慎处理的环节。

## 5.1 数据作用域属性

理解变量的作用域是避免数据竞争的核心。OpenMP 将变量分为以下两类：
*   **`shared` (共享)**：对所有线程可见，**需同步机制保护**。循环外定义的变量默认为共享。
*   **`private` (私有)**：每个线程拥有变量的独立副本，常用于临时变量和循环索引。

以下是常见变量及其默认作用域：

|       变量类型       |   默认作用域   |          说明          |
| :--------------: | :-------: | :------------------: |
|   **循环外定义变量**    | `shared`  | 需同步保护或使用 `reduction` |
| **循环变量 (如 `i`)** | `private` |      每个线程有独立的索引      |
|   **循环内局部变量**    | `private` |     每次迭代都会创建新副本      |

## 5.2 同步指令

- **原子操作 (`atomic`)**
	- 要求对特定内存位置的更新是原子的，**开销较低**，适用于单一赋值或递增等简单操作。
    ```cpp
    #pragma omp atomic
    shared_counter++; // 等同于原子的 fetch_add
    ```
- **临界区 (`critical`)**
	- 确保代码块在任何时刻都只被一个线程执行，**开销较大**。适用于需要保护多行复杂操作的场景。可为临界区命名以实现更细粒度的控制。
    ```cpp
    #pragma omp critical (my_critical_section_name)
    { std::cout << "Thread " << tid << std::endl; }
    ```
- **同步路障 (`barrier`)**
	- 强制所有线程在此处等待，直到所有线程都到达该点后再继续。
	    *   **隐式**：大多数工作共享指令（如 `for`, `single`）结束后有一个隐式 barrier。
	    *   **显式**：使用 `#pragma omp barrier` 手动设置。

> [!NOTE] 同步建议
> *   **优先选择 `atomic` 而非 `critical`**：对于简单的内存更新，`atomic` 通常更快。
> *   **`critical` 用于保护代码段**：当需要保护多行语句且无法用 `atomic` 完成时使用。
> *   **注意隐式 barrier 的开销**：使用 `nowait` 子句可以消除不需要的隐式 barrier，从而提高性能。
> *   **避免锁争用**：过多的 `critical` 或 `atomic` 指令会成为性能瓶颈。

---

# 06 性能衡量与优化

## 6.1 计时与线程管理函数

`#include <omp.h>` 提供了方便的运行时函数来辅助优化：
*   `double omp_get_wtime()`：返回从某个固定时间点以来的秒数，是基准测试的黄金标准。
*   `int omp_get_thread_num()`：返回当前线程ID。
*   `int omp_get_num_procs()`：返回系统可用处理器数量。

## 6.2 OpenMP 优化最佳实践

*   **最小化并行区数量**：`fork/join` 模型有固定开销，应合并小循环或使用 `nowait` 减少线程创建。
*   **避免伪共享 (False Sharing)**：相邻线程频繁写入同一缓存行内的不同变量，会因缓存一致性协议导致性能急剧下降。可通过 `private` 变量、数组填充等解决。
*   **合理选择调度策略**：对计算时间不均的迭代使用 `dynamic` 或 `guided`，对均匀的迭代使用 `static`。
*   **避免过度同步**：应通过设计避免数据竞争，而非过度依赖 `critical`/`atomic`。
*   **选择合适的粒度**：任务粒度太细会导致调度开销过大；太粗则负载不均衡。通过实验找到最佳平衡点。
*   **Don't over-parallelize**：对小任务并行可能得不偿失，应始终通过实际测量来验证优化的有效性。

---

# 07 进阶主题

## 7.1 嵌套并行与亲和性

OpenMP 允许在并行区内再创建并行区，即**嵌套并行**。默认禁用，可通过 `omp_set_nested(1)` 或 `OMP_NESTED` 环境变量启用。建议使用 `omp_set_max_active_levels()` 控制层级深度以避免性能问题。线程对处理器核心的绑定策略（亲和性）可通过 `OMP_PROC_BIND` 环境变量控制，在 NUMA 架构上影响巨大。

## 7.2 任务化 (`task`)：不规则并行的利器

`task` 构造是比 `parallel for`/`sections` 更灵活的动态并行方式，非常适合递归、`while` 循环等不规则结构。线程组中的某个线程通过 `#pragma omp task` 创建任务，线程组中的任意线程可执行这些动态产生的任务。任务间同步通过 `#pragma omp taskwait` 完成。

## 7.3 将计算卸载到加速器 (`target`)

从 OpenMP 4.0 开始，可通过 `target` 指令将代码和数据卸载到 GPU 等加速设备上执行，是迈向异构计算的重要一步。

---

# 08 参考资料与后续学习

*   **劳伦斯利弗莫尔国家实验室教程**: [OpenMP Tutorial](https://hpc-tutorials.llnl.gov/openmp/)


请注意，本教程基于 OpenMP 5.x 的通用规范。不同编译器或版本的支持程度和具体行为可能有细微差异。建议在实际工作中查阅对应的编译器手册（如 [GCC](https://gcc.gnu.org/onlinedocs/libgomp/), [LLVM](https://openmp.llvm.org/), [MSVC](https://learn.microsoft.com/en-us/cpp/parallel/openmp/reference/openmp-directives) 等）以获取最准确的信息。