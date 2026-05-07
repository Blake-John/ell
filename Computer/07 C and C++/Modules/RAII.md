# RAII Tutorial

RAII（Resource Acquisition Is Initialization，资源获取即初始化）是 C++ 中最核心的资源管理范式。它把资源的生命周期绑定到对象的生命周期上，让编译器自动管理资源，从根本上防止了资源泄漏。

---

## 1. 为什么需要 RAII

在 C 风格编程中，资源（动态内存、文件句柄、互斥锁、数据库连接等）需要手动申请和释放，很容易出错：

```cpp
void badFunction() {
    int* data = new int[100];         // 申请内存
    FILE* file = fopen("test.txt", "r"); // 打开文件

    if (someCondition) {
        return;  // ❌ 提前返回，data 和 file 都泄漏了
    }

    if (anotherCondition) {
        throw std::runtime_error("error"); // ❌ 抛出异常，同样泄漏
    }

    // ... 业务逻辑 ...

    delete[] data;   // 正常释放
    fclose(file);
}
```

问题根源在于：**资源释放不是自动的**。只要流程出现分支、提前返回或异常，释放代码就可能被跳过。

RAII 的核心思想是：把资源交给一个**局部对象**，利用 C++ 保证对象生命周期结束时析构函数**一定会被调用**的机制，自动释放资源。

---

## 2. RAII 的基本原理

RAII 有两层含义：

- **资源获取即初始化**（构造函数获取资源）
- **对象析构即资源释放**（析构函数释放资源）

用一个管理动态数组的类来演示：

```cpp
class IntArray {
public:
    // 构造函数：获取资源
    explicit IntArray(size_t size)
        : data_(new int[size]), size_(size) {
    }

    // 析构函数：释放资源
    ~IntArray() {
        delete[] data_;
    }

    // 禁止拷贝（先做简单处理，后续再讲）
    IntArray(const IntArray&) = delete;
    IntArray& operator=(const IntArray&) = delete;

    int& operator[](size_t index) {
        return data_[index];
    }
    size_t size() const { return size_; }

private:
    int* data_;
    size_t size_;
};
```

现在，无论函数以何种方式退出，资源都会自动释放：

```cpp
void goodFunction() {
    IntArray arr(100);

    if (someCondition) {
        return;  // ✅ arr 的析构函数自动调用，释放内存
    }

    if (anotherCondition) {
        throw std::runtime_error("error"); // ✅ 栈展开时自动调用析构
    }

    // 正常结束时也会自动释放
}
```

**核心保证：C++ 标准规定，当局部对象的生命周期结束时，析构函数一定会被调用。** 即使抛出异常，也会发生“栈展开（stack unwinding）”，沿途的所有局部对象都会被正确析构。

---

## 3. 经典 RAII 实现：文件管理器

用 C 的文件 API 演示一个完整的 RAII 封装：

```cpp
#include <cstdio>
#include <stdexcept>

class File {
public:
    // 构造函数打开文件（获取资源）
    File(const char* filename, const char* mode) {
        handle_ = std::fopen(filename, mode);
        if (!handle_) {
            throw std::runtime_error("Failed to open file");
        }
    }

    // 析构函数关闭文件（释放资源）
    ~File() {
        if (handle_) {
            std::fclose(handle_);
        }
    }

    // 移动构造函数（转移所有权）
    File(File&& other) noexcept
        : handle_(other.handle_) {
        other.handle_ = nullptr;  // 防止析构时重复关闭
    }

    // 移动赋值运算符
    File& operator=(File&& other) noexcept {
        if (this != &other) {
            if (handle_) std::fclose(handle_); // 先释放当前资源
            handle_ = other.handle_;
            other.handle_ = nullptr;
        }
        return *this;
    }

    // 禁止拷贝（文件不能有两个独立所有者）
    File(const File&) = delete;
    File& operator=(const File&) = delete;

    // 写入内容
    void write(const char* data) {
        if (handle_) {
            std::fputs(data, handle_);
        }
    }

    // 获取原始句柄（尽量少暴露）
    std::FILE* get() const { return handle_; }

private:
    std::FILE* handle_;
};
```

使用示例：

```cpp
void processFile() {
    File file("data.txt", "w");       // 构造时打开
    file.write("Hello, RAII!\n");

    if (errorHappens) {
        throw std::runtime_error("Oops"); // 栈展开，file 的析构函数自动关闭文件
    }

    // 正常结束也会关闭
}
```

---

## 4. 处理对象拷贝与所有权

RAII 类通常会面临一个问题：对象被拷贝时，资源如何处理？

常见策略有：

| 策略 | 说明 | 示例 |
|------|------|------|
| **禁止拷贝** | 简单安全，用 `= delete` | `std::unique_ptr` (不可拷贝，可移动) |
| **深拷贝** | 创建资源的独立副本 | `std::vector`, `std::string` |
| **引用计数 / 共享所有权** | 多个对象共享同一资源，最后一个析构时释放 | `std::shared_ptr` |
| **移动语义** | 转移所有权，源对象不再拥有资源 | `std::unique_ptr` 的移动 |

**深拷贝示例**（修正之前的 IntArray）：

```cpp
IntArray(const IntArray& other)
    : data_(new int[other.size_]), size_(other.size_) {
    std::copy(other.data_, other.data_ + other.size_, data_);
}

IntArray& operator=(const IntArray& other) {
    if (this != &other) {
        delete[] data_;                     // 释放旧资源
        size_ = other.size_;
        data_ = new int[size_];
        std::copy(other.data_, other.data_ + size_, data_);
    }
    return *this;
}
```

**移动语义**（转移所有权，通常结合拷贝禁止使用）：

标准库中的 `std::unique_ptr` 就是最典型的例子：
```cpp
std::unique_ptr<int> p1(new int(42));
std::unique_ptr<int> p2 = std::move(p1); // p2 接管资源，p1 变为 nullptr
```

---

## 5. 标准库中的 RAII 应用

C++ 标准库大量应用了 RAII，你每天使用的很多类都是 RAII 思想的体现。

### 5.1 智能指针：`std::unique_ptr` / `std::shared_ptr`

```cpp
#include <memory>

// unique_ptr：独占所有权
void uniquePtrDemo() {
    auto p = std::make_unique<int>(42); // 构造获取资源
    // 离开作用域自动 delete
}

// shared_ptr：共享所有权，引用计数
void sharedPtrDemo() {
    auto sp1 = std::make_shared<std::string>("Hello");
    {
        auto sp2 = sp1;  // 引用计数变为 2
    } // sp2 析构，计数减为 1，不释放
} // sp1 析构，计数归零，释放字符串
```

### 5.2 互斥锁：`std::lock_guard` / `std::unique_lock`

多线程中管理互斥锁是最经典的 RAII 用例之一。

```cpp
#include <mutex>

std::mutex mtx;
int shared_data = 0;

void safeIncrement() {
    std::lock_guard<std::mutex> lock(mtx);  // 构造时加锁
    ++shared_data;
    // 无论函数如何退出（正常、异常、提前返回），析构时自动解锁
}
```

`std::unique_lock` 提供了更灵活的控制（可延迟加锁、提前解锁、转移所有权）：

```cpp
void flexibleLock() {
    std::unique_lock<std::mutex> lock(mtx, std::defer_lock); // 不加锁
    // ... 一些不需要锁的准备操作 ...
    lock.lock();        // 手动加锁
    // 临界区
    lock.unlock();      // 手动解锁（析构时如果还锁着也会自动解锁）
}
```

### 5.3 文件流：`std::fstream` 

```cpp
#include <fstream>

void writeToFile() {
    std::ofstream file("output.txt");  // 构造时打开文件
    file << "RAII in action!";
    // 离开作用域时 file 被销毁，自动关闭文件
}
```

### 5.4 容器与字符串：`std::vector`, `std::string`

它们管理堆内存，无需手动 `new` / `delete`。

```cpp
std::vector<int> vec = {1, 2, 3};
std::string str = "RAII";
// 退出时自动释放底层的堆内存
```

### 5.5 作用域守卫：`std::experimental::scope_exit` (C++17/20)

有时需要执行一段非资源管理的清理代码，可以使用 Scope Guard。C++23 起标准库将支持 `std::scope_exit`，或者你可以自己实现：

```cpp
#include <iostream>
#include <functional> // 用 std::function 演示

class ScopeGuard {
public:
    template<typename Func>
    ScopeGuard(Func&& f) : callback_(std::forward<Func>(f)), active_(true) {}

    ~ScopeGuard() { if (active_) callback_(); }

    void dismiss() { active_ = false; } // 取消执行

    ScopeGuard(const ScopeGuard&) = delete;
    ScopeGuard& operator=(const ScopeGuard&) = delete;

private:
    std::function<void()> callback_;
    bool active_;
};

// 使用
void scopeGuardDemo() {
    std::cout << "Enter function" << std::endl;
    ScopeGuard guard([] { std::cout << "Cleanup on exit!" << std::endl; });

    // ... 无论异常还是正常返回，都会打印 Cleanup on exit!
}
```

---

## 6. RAII 与异常安全

RAII 是实现**强异常安全保证**（strong exception safety）的关键手段。

经典示例：赋值操作中先复制再交换（Copy-and-Swap）

```cpp
#include <algorithm>

class Widget {
    int* data;
    size_t size;

public:
    Widget(size_t s) : data(new int[s]), size(s) {}
    ~Widget() { delete[] data; }

    // 拷贝构造（深拷贝）
    Widget(const Widget& other) : data(new int[other.size]), size(other.size) {
        std::copy(other.data, other.data + other.size, data);
    }

    // 拷贝赋值（强异常安全）
    Widget& operator=(const Widget& other) {
        if (this != &other) {
            Widget temp(other);      // 可能抛异常，但不影响 this
            swap(temp);              // 不会抛异常，接管资源
        }                           // temp 析构，释放旧资源
        return *this;
    }

    void swap(Widget& other) noexcept {
        std::swap(data, other.data);
        std::swap(size, other.size);
    }
};
```

核心思路：先用 RAII 创建成功的副本，再用非抛异常的 swap 进行交换，旧资源在临时对象析构时自动释放。整个过程要么完全成功，要么失败后原对象状态不变。

---

## 7. 现代 C++ 中的 RAII 最佳实践

1. **永远不要在普通代码中直接使用 `new`/`delete`**  
   需要动态内存时使用 `std::make_unique`、`std::make_shared`、`std::vector` 等。

2. **避免直接使用原始文件句柄、锁等**  
   优先使用 `std::fstream`、`std::lock_guard`、`std::unique_lock` 等标准 RAII 封装。

3. **当必须封装自己的 RAII 类时，遵守“Rule of Five”**（C++11 起）  
   如果定义了析构函数、拷贝构造或拷贝赋值中的任何一个，通常需要定义以下五个：  
   - 析构函数  
   - 拷贝构造函数  
   - 拷贝赋值运算符  
   - 移动构造函数  
   - 移动赋值运算符  
   
   不过很多时候可以更简单地应用“Rule of Zero”：**尽量不自己管理资源**，只用标准库组件组合，这样编译器自动生成的函数就是正确的。

4. **使用 `noexcept` 声明移动构造和移动赋值**  
   保证移动操作不抛异常，以便标准容器能高效使用。

5. **资源所有权要明确**  
   是独占（`unique_ptr`）还是共享（`shared_ptr`）？不允许拷贝但允许移动？清晰的设计能避免很多 bug。

6. **尽量缩小 RAII 对象的生命周期**  
   在需要资源的最小作用域内定义 RAII 对象，及时释放资源。

---

## 8. 常见陷阱与注意事项

- **忘记禁止拷贝或实现移动**：导致重复释放（double-free）或者所有权混乱。
- **在构造函数中抛出异常**：如果构造函数抛出异常，对象构造未完成，析构函数**不会被调用**。因此必须保证在抛出异常前，已经获取的资源要自行清理。通常建议使用“Resource Manager”思想——使用已有的 RAII 成员来管理资源，这样每个成员的析构都会被调用。
  
  示例（不安全）：
  ```cpp
  class Bad {
      FILE* f1;
      FILE* f2;
  public:
      Bad(const char* a, const char* b) {
          f1 = fopen(a, "r");
          f2 = fopen(b, "r");   // 如果这里抛异常，f1 不会关闭
      }
      ~Bad() { fclose(f1); fclose(f2); }
  };
  ```
  改进（安全）：
  ```cpp
  class Good {
      File f1;  // 使用之前定义的 RAII File 类
      File f2;
  public:
      Good(const char* a, const char* b) : f1(a, "r"), f2(b, "r") {}
      // 如果 f2 构造抛异常，f1 已完成构造，其析构函数会被调用
  };
  ```

- **不要在不应该的地方引入开销**：`shared_ptr` 有额外控制块的开销，无必要不要滥用。

- **不要将智能指针的 `get()` 返回的裸指针传递给可能延长生命周期的逻辑**：避免悬空指针。

- **析构函数不应该抛出异常**：如果在析构中释放资源可能抛异常，必须捕获并处理，否则可能引发 `std::terminate`。

---

## 9. 总结

- **RAII 的本质**：用对象管理资源，构造函数获取资源，析构函数释放资源。
- **关键保障**：C++ 对象生命周期结束必然调用析构函数，即使发生异常。
- **表现形式**：智能指针、锁守卫、文件流、容器……几乎整个 C++ 标准库到处都是 RAII 的身影。
- **现代 C++ 建议**：尽量不亲手管理资源，组合使用标准 RAII 工具；如需自定义 RAII 类，遵循 Rule of Zero / Five，并保持异常安全。