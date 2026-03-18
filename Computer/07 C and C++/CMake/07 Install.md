---
title: CMake Install 与 find_package 实战
date: 2024-01-15
tags:
  - cmake
  - cpp
  - install
  - find_package
aliases:
  - CMake Install 教程
  - CMake 库安装
cssclasses:
  - tutorial
---
在前面我们学习了如何 [编写 CMakeLists.txt](04%20Write%20CMakeLists.md) 和 [构建项目](06%20Build.md)，掌握了如何将源码编译成库文件和可执行文件。但是，编译完成后的产物只存在于 `build` 目录中，如果我们想让其他人也能使用我们的库，就需要将库安装到系统中。本教程将详细讲解 `install` 命令的用法，并教你如何维护一个库，使其能被 `find_package()` 找到。

> [!info] 本教程前置知识
> - 建议先阅读 [[04 Write CMakeLists]] 了解 CMake 基本语法
> - 建议先阅读 [[06 Build]] 了解项目的构建过程
> - 本教程以动态库为例进行讲解

---

# 01 install 命令概述

## 1.1 什么是 install 命令？

`install` 命令是 CMake 中用于 **指定文件安装规则** 的指令。它告诉 CMake 在执行 `cmake --install`（或 `make install`）时，应该将哪些文件复制到系统的哪个位置。通过 install 命令，我们可以：

- 将编译好的 **库文件** 安装到系统目录（如 `/usr/local/lib`）
- 将 **头文件** 安装到系统目录（如 `/usr/local/include`）
- 将 **配置文件** 安装到系统目录（如 `/usr/local/cmake`）
- 将 **可执行文件** 安装到系统目录（如 `/usr/local/bin`）

## 1.2 install 命令的工作原理

当我们执行以下命令时：

```bash
# Linux/macOS
cmake --install <build-dir> --prefix /usr/local
# or make install

# Windows
cmake --install <build-dir> --prefix C:\Program Files\MyProject
```

CMake 会读取 `CMakeLists.txt` 中的 `install` 指令，将指定的目标、文件或目录安装到 `${CMAKE_INSTALL_PREFIX}` 所指定的目录下。

> [!tip] CMAKE_INSTALL_PREFIX
> - 默认情况下，`CMAKE_INSTALL_PREFIX` 在 Linux 上为 `/usr/local`
> - 在 Windows 上为 `C:/Program Files/${PROJECT_NAME}`
> - 可以通过 CMake 选项 `-D CMAKE_INSTALL_PREFIX=/custom/path` 或设置改变量进行覆盖

## 1.3 install 命令的类型

`install` 命令主要有以下几种形式：

| 类型                     | 用途              |
| ---------------------- | --------------- |
| `install(TARGETS)`     | 安装目标文件（库、可执行文件） |
| `install(FILES)`       | 安装普通文件          |
| `install(PROGRAMS)`    | 安装可执行脚本         |
| `install(DIRECTORY)`   | 安装整个目录          |
| `install(EXPORT)`      | 导出目标供其他项目使用     |
| `install(SCRIPT/CODE)` | 执行脚本代码          |

基本语法如下：

```cmake
install(TARGETS <target>... [<target-variant>...]
        [EXPORT <export-name>]
        [RUNTIME DESTINATION <dir>]
        [LIBRARY DESTINATION <dir>]
        [ARCHIVE DESTINATION <dir>]
        [OBJECTS DESTINATION <dir>]
        [INCLUDES DESTINATION <dir>...]
        [PRIVATE_HEADER DESTINATION <dir>]
        [PUBLIC_HEADER DESTINATION <dir>]
        [RESOURCE DESTINATION <dir>]
        [<option>...]
)
```

---

# 02 install(TARGETS) - 安装目标文件

## 2.1 基本语法

```cmake
install(TARGETS <target>... [<target-variant>...]
        [RUNTIME DESTINATION <dir>]
        [LIBRARY DESTINATION <dir>]
        [ARCHIVE DESTINATION <dir>]
        [INCLUDES DESTINATION <dir>...]
)
```

其中：
- `<target>` 是通过 `add_executable()` 或 `add_library()` 创建的目标
- `RUNTIME` 用于可执行文件和 DLL
- `LIBRARY` 用于动态库 (.so/.dylib)
- `ARCHIVE` 用于静态库 (.a/.lib)
- `INCLUDES` 用于头文件目录（仅传递信息，不会实际安装）

## 2.2 安装动态库

假设我们有一个库项目 `MyLibrary`，CMakeLists.txt 如下：

```cmake
cmake_minimum_required(VERSION 3.10)
project(MyLibrary VERSION 1.0.0)

add_library(mylib SHARED src/mylib.cpp)
target_include_directories(mylib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
```

添加 install 命令后：

```cmake
cmake_minimum_required(VERSION 3.10)
project(MyLibrary VERSION 1.0.0)

add_library(mylib SHARED src/mylib.cpp)
target_include_directories(mylib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

# 安装动态库到 lib 目录
install(TARGETS mylib
        RUNTIME DESTINATION bin
        LIBRARY DESTINATION lib
)

# 安装头文件
install(DIRECTORY include/ DESTINATION include)
```

执行安装：

```bash
cd build
cmake ..
make
cmake --install . --prefix /usr/local
# 或 make install DESTDIR=/usr/local
```

安装后的目录结构：

```
/usr/local/
├── bin/
│   └── libmylib.so      # 动态库（Linux）
├── lib/
│   └── libmylib.so      # 动态库（部分系统）
└── include/
    └── mylib.h
```

> [!warning] RUNTIME vs LIBRARY
> - 在 Windows 上：`.dll` 文件属于 RUNTIME
> - 在 Linux 上：`.so` 文件通常属于 LIBRARY
> - 为跨平台兼容性，最好同时指定 RUNTIME 和 LIBRARY

## 2.3 安装静态库

如果需要安装静态库，使用 `ARCHIVE` 目标类型：

```cmake
add_library(mylib STATIC src/mylib.cpp)

install(TARGETS mylib
        ARCHIVE DESTINATION lib
)
```

## 2.4 同时安装动态库和静态库

有时我们需要同时提供动态库和静态库：

```cmake
# 生成动态库
add_library(mylib SHARED src/mylib.cpp)

# 生成静态库（使用 OBJECT 库）
add_library(mylib_static STATIC src/mylib.cpp)
set_target_properties(mylib_static PROPERTIES OUTPUT_NAME "mylib")

install(TARGETS mylib mylib_static
        RUNTIME DESTINATION bin
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib
)
```

## 2.5 安装可执行文件

```cmake
add_executable(myapp src/main.cpp)

install(TARGETS myapp
        RUNTIME DESTINATION bin
)
```

---

# 03 install(FILES/PROGRAMS) - 安装文件

## 3.1 install(FILES) - 安装普通文件

`install(FILES)` 用于安装普通文件，如头文件、配置文件等：

```cmake
# 安装头文件
install(FILES
        include/mylib.h
        include/mylib_export.h
        DESTINATION include
        )

# 安装配置文件
install(FILES
        config/config.json
        config/default.conf
        DESTINATION etc/myproject
        )
```

## 3.2 install(PROGRAMS) - 安装可执行脚本

`install(PROGRAMS)` 用于安装可执行脚本或程序，与 `FILES` 的区别是它 **会设置可执行权限**：

```cmake
# 安装脚本
install(PROGRAMS
        scripts/setup.sh
        scripts/cleanup.sh
        DESTINATION bin
        )

# 安装工具脚本
install(PROGRAMS
        tools/mytool
        DESTINATION bin
        )
```

## 3.3 权限设置

可以通过 `PERMISSIONS` 选项设置文件权限：

```cmake
install(FILES config.conf
        DESTINATION etc
        PERMISSIONS OWNER_READ OWNER_WRITE GROUP_READ WORLD_READ
        )

install(PROGRAMS myscript
        DESTINATION bin
        PERMISSIONS OWNER_READ OWNER_EXECUTE GROUP_READ GROUP_EXECUTE WORLD_READ WORLD_EXECUTE
        )
```

---

# 04 install(DIRECTORY) - 安装目录

## 4.1 基本用法

`install(DIRECTORY)` 用于安装整个目录：

```cmake
# 安装 include 目录下的所有内容到 include 目录
install(DIRECTORY include/ DESTINATION include)

# 安装 docs 目录
install(DIRECTORY docs/ DESTINATION share/doc/myproject)
```

## 4.2 通配符匹配

可以使用通配符过滤要安装的文件：

```cmake
# 只安装 .h 文件
install(DIRECTORY include/ DESTINATION include
        FILES_MATCHING PATTERN "*.h")

# 排除特定模式
install(DIRECTORY data/ DESTINATION share/myproject/data
        FILES_MATCHING PATTERN "*.dat"
        PATTERN ".git" EXCLUDE
        PATTERN "*.tmp" EXCLUDE)
```

## 4.3 目录权限设置

可以为目录中的文件设置默认权限：

```cmake
install(DIRECTORY scripts/ DESTINATION bin
        PERMISSIONS
            OWNER_READ OWNER_WRITE OWNER_EXECUTE
            GROUP_READ GROUP_EXECUTE
            WORLD_READ WORLD_EXECUTE
        )
```

> [!note] 
> **注意**：在使用 `install(DIRECTORY <src> DESTINATION <target>)` 时，不同的 `<src>` 写法由不同的结果：
> - 当 `<src>` 为 `include/` ，带 `/` 时，会将 `include/*` 安装到 `<target>` ，即把 `include/` 目录下的所有内容安装到 `<target>` 目录下
> - 当 `<src>` 为 `include` ，不带 `/` 时，会将 `include/` 目录安装为 `<target>` ，即复制 `include/` 到安装位置并重命名为 `<target>`
>   
> 推荐使用第一种

---

# 05 install(EXPORT) - 导出目标

## 5.1 什么是导出目标？

`install(EXPORT)` 允许我们将目标导出到一个「导出组」，生成一个供其他项目使用的 CMake 文件。这个导出的文件包含了目标的定义，使得其他项目可以通过 `find_package()` 或 `target_link_libraries()` 来使用我们的库。

## 5.2 基本语法

```cmake
install(EXPORT <export-name>
        FILE <file>.cmake
        [NAMESPACE <namespace>::]
        [DESTINATION <dir>]
        [PRIVATE_HEADER DESTINATION <dir>]
        [PUBLIC_HEADER DESTINATION <dir>]
        [RESOURCE DESTINATION <dir>]
        )
```

## 5.3 完整示例

```cmake
cmake_minimum_required(VERSION 3.10)
project(MyLibrary VERSION 1.0.0)

# 生成动态库
add_library(mylib SHARED src/mylib.cpp)
target_include_directories(mylib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

# 安装库文件
install(TARGETS mylib
        RUNTIME DESTINATION bin
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib
        )

# 安装头文件
install(DIRECTORY include/ DESTINATION include)

# 导出目标到 MyLibraryTargets.cmake
install(EXPORT mylibTargets
        FILE MyLibraryTargets.cmake
        NAMESPACE MyLibrary::
        DESTINATION lib/cmake/MyLibrary
        )
```

这会生成一个名为 `MyLibraryTargets.cmake` 的文件，其中包含目标 `MyLibrary::mylib` 的定义。

> [!tip] NAMESPACE 的作用
> `NAMESPACE MyLibrary::` 前缀允许使用者通过 `MyLibrary::mylib` 来引用目标，这是现代 CMake 的推荐做法。

---

# 06 GNUInstallDirs - 标准的安装目录

## 6.1 什么是 GNUInstallDirs？

`GNUInstallDirs` 是 CMake 提供的一个模块，定义了符合 GNU 标准 的安装目录变量。使用它可以让我们的项目遵循 Linux 系统的标准目录布局：

```cmake
include(GNUInstallDirs)

# 使用标准变量
install(TARGETS mylib
        RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
        LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
        ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
        )

install(DIRECTORY include/ DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})
```

## 6.2 常用变量

| 变量 | 默认值（Linux） | 用途 |
|------|-----------------|------|
| `CMAKE_INSTALL_BINDIR` | `bin` | 可执行文件 |
| `CMAKE_INSTALL_LIBDIR` | `lib` 或 `lib64` | 库文件 |
| `CMAKE_INSTALL_INCLUDEDIR` | `include` | 头文件 |
| `CMAKE_INSTALL_DATADIR` | `share/${PROJECT_NAME}` | 数据文件 |
| `CMAKE_INSTALL_DOCDIR` | `share/doc/${PROJECT_NAME}` | 文档 |
| `CMAKE_INSTALL_SYSCONFDIR` | `etc` | 配置文件 |

> [!info] 64位系统注意
> 在 64 位 Linux 系统上，库目录通常是 `lib64` 而非 `lib`。`GNUInstallDirs` 会自动处理这个差异。

---

# 07 完整的库安装配置

## 7.1 项目结构

假设我们有一个完整的库项目：

```
MyLibrary/
├── CMakeLists.txt
├── LICENSE
├── README.md
├── src/
│   └── mylib.cpp
├── include/
│   └── mylib.h
└── cmake/
    └── MyLibraryConfig.cmake.in
```

## 7.2 主 CMakeLists.txt

```cmake
cmake_minimum_required(VERSION 3.10)
project(MyLibrary VERSION 1.0.0)

# 设置 C++ 标准
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

# 生成动态库
add_library(mylib SHARED src/mylib.cpp)
target_include_directories(mylib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

# 设置版本信息
set_target_properties(mylib PROPERTIES
        VERSION ${PROJECT_VERSION}
        SOVERSION 1
        )

# 使用 GNUInstallDirs 定义标准目录
include(GNUInstallDirs)

# 安装库文件
install(TARGETS mylib
        RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
        LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
        ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
        )

# 安装头文件
install(DIRECTORY include/ DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})

# 导出目标
install(EXPORT mylibTargets
        FILE MyLibraryTargets.cmake
        NAMESPACE MyLibrary::
        DESTINATION ${CMAKE_INSTALL_LIBDIR}/cmake/MyLibrary
        )
```

## 7.3 构建和安装

```bash
# 创建构建目录
mkdir build && cd build

# 配置（指定安装路径）
cmake -DCMAKE_INSTALL_PREFIX=/usr/local ..

# 编译
make

# 安装
sudo cmake --install .
```

> [!warning] 安装权限
> 安装到系统目录（如 `/usr/local`）通常需要 root 权限，需要使用 `sudo`。

## 7.4 链接

通过这种方式安装的库，可以直接通过 `target_link_libraries()` 和 `target_include_libraries()` 定位到具体的安装目标来使用，如 

```cmake
target_link_libraries(myexe /usr/local/lib/mylib.so)
```

---

# 08 target_include_directories() 与生成器表达式

## 8.1 问题背景

在使用 `target_include_directories()` 时，我们经常会遇到一个问题：**构建时**和**安装后**需要使用不同的 include 路径。

例如：
- **构建时**：需要使用 `${CMAKE_CURRENT_SOURCE_DIR}/include`（源代码目录）
- **安装后**：需要使用 `${CMAKE_INSTALL_PREFIX}/include`（安装目录）
- **被其他项目作为依赖链接时**：需要使用安装目录

## 8.2 生成器表达式

CMake 提供了**生成器表达式**（Generator Expressions）来解决这个问题。生成器表达式是在生成构建系统时才会被求值的表达式，语法为 `$<...>`。

### 常用生成器表达式

| 表达式 | 说明 |
|--------|------|
| `$<BUILD_INTERFACE:path>` | 构建时（build）使用的路径 |
| `$<INSTALL_INTERFACE:path>` | 安装时（install）使用的路径（会自动添加 `${CMAKE_INSTALL_PREFIX}` 前缀） |
| `$<INSTALL_PREFIX>` | 安装前缀 |
| `$<TARGET_PROPERTY:target,prop>` | 获取目标属性 |
| `$<BOOL:value>` | 转换为布尔值 |
| `$<IF:condition,true_value,false_value>` | 条件表达式 |

## 8.3 使用示例

### 基本用法

```cmake
target_include_directories(mylib PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
        $<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}>
        )
```

解释：
- 当**构建当前项目**时，使用 `${CMAKE_CURRENT_SOURCE_DIR}/include`
- 当**安装后**被其他项目使用时，使用 `${CMAKE_INSTALL_INCLUDEDIR}`（会自动添加 `${CMAKE_INSTALL_PREFIX}` 前缀）

### 完整示例

```cmake
cmake_minimum_required(VERSION 3.10)
project(MyLibrary VERSION 1.0.0)

include(GNUInstallDirs)

# 定义库
add_library(mylib SHARED src/mylib.cpp)

# 使用生成器表达式设置 include 目录
target_include_directories(mylib PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
        $<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}>
        )

# 安装
install(TARGETS mylib
        LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
        )

install(DIRECTORY include/ DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})

install(EXPORT mylibTargets
        FILE MyLibraryTargets.cmake
        NAMESPACE MyLibrary::
        DESTINATION ${CMAKE_INSTALL_LIBDIR}/cmake/MyLibrary
        )
```

### 等价的简化写法

在使用 `PUBLIC_HEADER` 时，CMake 会自动处理这个转换：

```cmake
add_library(mylib SHARED src/mylib.cpp)

# CMake 会自动生成对应的生成器表达式
set_target_properties(mylib PROPERTIES
        PUBLIC_HEADER "include/mylib.h"
        )

install(TARGETS mylib
        LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
        PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}
        )
```

## 8.4 三种使用场景详解

生成器表达式 `$<BUILD_INTERFACE:...>` 和 `$<INSTALL_INTERFACE:...>` 在以下三种场景下的行为：

### 场景1：构建当前项目

```
CMAKE_CURRENT_SOURCE_DIR/include  →  编译器的 -I 参数
```

### 场景2：安装到系统

```
${CMAKE_INSTALL_PREFIX}/include  →  安装到 /usr/local/include
```

### 场景3：被其他项目通过 find_package() 使用

```
${CMAKE_INSTALL_PREFIX}/include  →  消费者的编译参数
```

## 8.5 完整的 Config 模式示例

```cmake
cmake_minimum_required(VERSION 3.10)
project(MyLibrary VERSION 1.0.0)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

include(GNUInstallDirs)

# ========== 库目标定义（使用生成器表达式）==========
add_library(mylib SHARED src/mylib.cpp)

# 关键：使用生成器表达式区分 build 和 install
target_include_directories(mylib PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
        $<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}>
        )

set_target_properties(mylib PROPERTIES
        VERSION ${PROJECT_VERSION}
        SOVERSION ${PROJECT_VERSION_MAJOR}
        )

# ========== 安装规则 ==========
install(TARGETS mylib
        RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
        LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
        ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
        )

install(EXPORT mylibTargets
        FILE MyLibraryTargets.cmake
        NAMESPACE MyLibrary::
        DESTINATION ${CMAKE_INSTALL_LIBDIR}/cmake/MyLibrary
        )

# ========== Config 文件 ==========
include(CMakePackageConfigHelpers)

configure_package_config_file(cmake/MyLibraryConfig.cmake.in
        ${CMAKE_CURRENT_BINARY_DIR}/MyLibraryConfig.cmake
        INSTALL_DESTINATION ${CMAKE_INSTALL_LIBDIR}/cmake/MyLibrary
        )

write_basic_package_version_file(MyLibraryConfigVersion.cmake
        VERSION ${PROJECT_VERSION}
        COMPATIBILITY SameMajorVersion
        )

install(FILES
        ${CMAKE_CURRENT_BINARY_DIR}/MyLibraryConfig.cmake
        ${CMAKE_CURRENT_BINARY_DIR}/MyLibraryConfigVersion.cmake
        DESTINATION ${CMAKE_INSTALL_LIBDIR}/cmake/MyLibrary
        )
```

## 8.6 为什么需要生成器表达式？

> [!tip] 问题
> 为什么要这么麻烦地使用生成器表达式？直接使用 `${CMAKE_CURRENT_SOURCE_DIR}/include` 不行吗？

**答案**：不行，因为会出现以下问题：

### 问题1：安装后路径错误

```cmake
# 错误写法
target_include_directories(mylib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

# 安装后，Config 文件会包含：
# -I/home/user/MyLibrary/include   ← 这是源代码路径！
# 但实际安装后，头文件在 /usr/local/include
```

### 问题2：被其他项目引用时路径错误

当消费者通过 `find_package()` 使用你的库时：
- 如果直接写死 `${CMAKE_CURRENT_SOURCE_DIR}/include`
- 消费者会尝试从你的源代码目录找头文件
- 但消费者没有你的源代码目录！

### 生成器表达式的工作原理

```cmake
target_include_directories(mylib PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
        $<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}>
        )
```

- **构建时**：`$<BUILD_INTERFACE:...>` 会被替换为 `${CMAKE_CURRENT_SOURCE_DIR}/include`
- **安装时**：`$<INSTALL_INTERFACE:...>` 会被替换为 `${CMAKE_INSTALL_PREFIX}/${CMAKE_INSTALL_INCLUDEDIR}`

> [!warning] 注意
> `$<INSTALL_INTERFACE:...>` 中的路径是相对于 `${CMAKE_INSTALL_PREFIX}` 的，所以：
> - 写 `${CMAKE_INSTALL_INCLUDEDIR}` → 安装后会变成 `${CMAKE_INSTALL_PREFIX}/include`
> - 如果写绝对路径 `${CMAKE_INSTALL_PREFIX}/include` → 安装后会变成 `${CMAKE_INSTALL_PREFIX}/usr/local/include`（错误！）

---

# 09 find_package() 机制详解

## 9.1 find_package() 的作用

`find_package()` 是 CMake 中用于**查找并加载外部库**的命令。当我们想在一个项目中使用某个库时，需要先找到它，然后才能链接它。

## 9.2 两种查找模式

`find_package()` 支持两种模式：

| 模式 | 说明 | 搜索路径 |
|------|------|----------|
| **Module 模式** | 查找 `FindXXX.cmake` 模块 | `${CMAKE_MODULE_PATH}` |
| **Config 模式** | 查找 `XXXConfig.cmake` 文件 | 多种路径 |

CMake 会首先尝试 Module 模式，如果找不到则尝试 Config 模式。

### Module 模式（传统方式）

```cmake
# CMake 会查找 FindMyLibrary.cmake
find_package(MyLibrary REQUIRED)
```

搜索路径：
1. `${CMAKE_MODULE_PATH}`
2. `${CMAKE_ROOT}/Modules/`

### Config 模式（现代方式）

```cmake
# CMake 会查找 MyLibraryConfig.cmake
find_package(MyLibrary REQUIRED)
```

搜索路径：
1. `${CMAKE_PREFIX_PATH}`
2. `<prefix>/lib/cmake/<name>*/`
3. `<prefix>/<name>*/`
4. `<prefix>/lib/<name>*/`
5. `<prefix>/share`
6. 系统默认路径

## 9.3 搜索路径示例

假设我们安装到 `/usr/local`，Config 模式会搜索：

```
/usr/local/lib/cmake/MyLibrary/
/usr/local/MyLibrary/
/usr/local/lib/MyLibrary/
```

---

# 10 创建可被 find_package() 找到的库

## 10.1 Config 文件的核心作用

要让库能被 `find_package()` 找到，我们需要提供一个 **Config 文件**（`XXXConfig.cmake`）。这个文件告诉 CMake：
- 库的位置
- 头文件的路径
- 库的依赖项（如果有）
- 版本信息

## 10.2 创建 Config 模板文件

在项目根目录下创建 `cmake/MyLibraryConfig.cmake.in`：

```cmake
@PACKAGE_INIT@

include("${CMAKE_CURRENT_LIST_DIR}/MyLibraryTargets.cmake")

# 可以在此传递依赖
find_dependency(DEP REQUIRED)

check_required_components(MyLibrary)
```

> [!important] 
> - `@PACKAGE_INIT@` - 这是一个占位符，CMake 会将其替换为设置 `MyLibrary_*` 变量的代码。
> - `find_dependency()` - 具体可见 [[#12 依赖项管理]]

## 10.3 安装 Config 文件

更新主 `CMakeLists.txt`：

```cmake
cmake_minimum_required(VERSION 3.10)
project(MyLibrary VERSION 1.0.0)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

include(GNUInstallDirs)

# ========== 库目标定义 ==========
add_library(mylib SHARED src/mylib.cpp)
target_include_directories(mylib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

set_target_properties(mylib PROPERTIES
        VERSION ${PROJECT_VERSION}
        SOVERSION 1
        )

# ========== 安装规则 ==========
install(TARGETS mylib
        RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
        LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
        ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
        )

install(DIRECTORY include/ DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})

install(EXPORT mylibTargets
        FILE MyLibraryTargets.cmake
        NAMESPACE MyLibrary::
        DESTINATION ${CMAKE_INSTALL_LIBDIR}/cmake/MyLibrary
        )

# ========== 安装 Config 文件 ==========
include(CMakePackageConfigHelpers)

configure_package_config_file(
		cmake/${PROJECT_NAME}Config.cmake.in
	    ${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}Config.cmake
	    INSTALL_DESTINATION ${CMAKE_INSTALL_LIBDIR}/cmake/${PROJECT_NAME}
)

write_basic_package_version_file(
		${PROJECT_NAME}ConfigVersion.cmake
        VERSION ${PROJECT_VERSION}
        COMPATIBILITY SameMajorVersion
        )

install(FILES
        ${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}Config.cmake
	    ${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}ConfigVersion.cmake
        DESTINATION ${CMAKE_INSTALL_LIBDIR}/cmake/MyLibrary
        )
```

## 10.4 安装后的目录结构

安装完成后，系统目录结构如下：

```
/usr/local/
├── lib/
│   ├── libmylib.so
│   └── cmake/MyLibrary/
│       ├── MyLibraryConfig.cmake
│       ├── MyLibraryConfigVersion.cmake
│       └── MyLibraryTargets.cmake
├── include/
│   └── mylib.h
└── bin/
```

> [!seealso] 
> 如果是管理 ROS2 开发中的第三方库，可见 [[../../08 ROS/ROS2/advanced/package_management|package_management]] 。

---

# 11 消费者使用示例

## 11.1 基本使用

当库安装好后，其他项目可以这样使用：

```cmake
# CMakeLists.txt
cmake_minimum_required(VERSION 3.10)
project(MyApp)

find_package(MyLibrary REQUIRED)

add_executable(myapp main.cpp)
target_link_libraries(myapp MyLibrary::mylib)
```

## 11.2 可选依赖

如果库是可选的：

```cmake
find_package(MyLibrary)

if(MyLibrary_FOUND)
    message(STATUS "Found MyLibrary: ${MyLibrary_VERSION}")
    add_executable(myapp main.cpp)
    target_link_libraries(myapp MyLibrary::mylib)
else()
    message(STATUS "MyLibrary not found, building without it")
endif()
```

## 11.3 指定搜索路径

如果库安装在不标准的位置：

```cmake
find_package(MyLibrary REQUIRED
        PATHS /custom/install/path
        NO_DEFAULT_PATH
        )
```

---

# 12 依赖项管理

## 12.1 find_dependency()

如果你的库依赖其他库，需要在 Config 文件中使用 `find_dependency()`：

```cmake
# cmake/MyLibraryConfig.cmake.in
@PACKAGE_INIT@

include("${CMAKE_CURRENT_LIST_DIR}/MyLibraryTargets.cmake")

find_dependency(RequiredDependency)

check_required_components(MyLibrary)
```

## 12.2 传递依赖

当消费者链接你的库时，依赖项会自动传递：

```cmake
# 你的库
add_library(mylib SHARED src/mylib.cpp)
target_link_libraries(mylib PUBLIC some_dependency)

# 消费者
find_package(MyLibrary REQUIRED)
add_executable(myapp main.cpp)
target_link_libraries(myapp MyLibrary::mylib)
# some_dependency 会自动传递
```

---

# 13 版本兼容性

## 13.1 兼容性选项

`write_basic_package_version_file()` 支持以下兼容性模式：

| 模式 | 说明 |
|------|------|
| `ExactVersion` | 必须完全匹配版本 |
| `SameMajorVersion` | 主版本号必须相同 |
| `SameMinorVersion` | 主版本和次版本必须相同 |
| `GreaterOrEqual` | 大于或等于指定版本 |
| `AnyNewerVersion` | 任何更新的版本 |

## 13.2 示例

```cmake
write_basic_package_version_file(MyLibraryConfigVersion.cmake
        VERSION ${PROJECT_VERSION}
        COMPATIBILITY SameMajorVersion
        )
```

---

# 14 完整项目示例

## 14.1 项目结构

```
MyLibrary/
├── CMakeLists.txt
├── src/
│   └── mylib.cpp
├── include/
│   └── mylib.h
└── cmake/
    └── MyLibraryConfig.cmake.in
```

## 14.2 头文件 - include/mylib.h

```cpp
#ifndef MYLIB_H
#define MYLIB_H

#ifdef _WIN32
    #ifdef MYLIB_EXPORTS
        #define MYLIB_API __declspec(dllexport)
    #else
        #define MYLIB_API __declspec(dllimport)
    #endif
#else
    #define MYLIB_API
#endif

MYLIB_API int add(int a, int b);
MYLIB_API int subtract(int a, int b);

#endif
```

## 14.3 源文件 - src/mylib.cpp

```cpp
#include "mylib.h"

int add(int a, int b) {
    return a + b;
}

int subtract(int a, int b) {
    return a - b;
}
```

## 14.4 Config 模板 - cmake/MyLibraryConfig.cmake.in

```cmake
@PACKAGE_INIT@

include("${CMAKE_CURRENT_LIST_DIR}/MyLibraryTargets.cmake")

check_required_components(MyLibrary)
```

## 14.5 主 CMakeLists.txt

```cmake
cmake_minimum_required(VERSION 3.10)
project(MyLibrary VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)
set(CMAKE_CXX_VISIBILITY_PRESET hidden)
set(CMAKE_VISIBILITY_INLINES_HIDDEN ON)

include(GNUInstallDirs)

# ========== 库目标 ==========
add_library(mylib SHARED src/mylib.cpp)
target_include_directories(mylib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

set_target_properties(mylib PROPERTIES
        VERSION ${PROJECT_VERSION}
        SOVERSION ${PROJECT_VERSION_MAJOR}
        PUBLIC_HEADER "include/mylib.h"
        )

# ========== 安装规则 ==========
install(TARGETS mylib
        RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
        LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
        ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
        PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}
        )

install(EXPORT mylibTargets
        FILE MyLibraryTargets.cmake
        NAMESPACE MyLibrary::
        DESTINATION ${CMAKE_INSTALL_LIBDIR}/cmake/MyLibrary
        )

# ========== Config 文件 ==========
include(CMakePackageConfigHelpers)

configure_package_config_file(cmake/MyLibraryConfig.cmake.in
        ${CMAKE_CURRENT_BINARY_DIR}/MyLibraryConfig.cmake
        INSTALL_DESTINATION ${CMAKE_INSTALL_LIBDIR}/cmake/MyLibrary
        )

write_basic_package_version_file(MyLibraryConfigVersion.cmake
        VERSION ${PROJECT_VERSION}
        COMPATIBILITY SameMajorVersion
        )

install(FILES
        ${CMAKE_CURRENT_BINARY_DIR}/MyLibraryConfig.cmake
        ${CMAKE_CURRENT_BINARY_DIR}/MyLibraryConfigVersion.cmake
        DESTINATION ${CMAKE_INSTALL_LIBDIR}/cmake/MyLibrary
        )
```

## 14.6 使用库的项目

```cmake
cmake_minimum_required(VERSION 3.10)
project(MyApp)

find_package(MyLibrary 1.0 REQUIRED)

add_executable(app main.cpp)
target_link_libraries(app MyLibrary::mylib)
```

---

# 15 常见问题与解决方案

## 15.1 找不到 Config 文件

> [!bug] 问题
> `find_package(MyLibrary REQUIRED)` 报错找不到

**解决方案**：
1. 检查安装路径是否正确
2. 确认 Config 文件已安装到正确位置
3. 使用 `-DCMAKE_PREFIX_PATH` 指定搜索路径

```bash
cmake -DCMAKE_PREFIX_PATH=/custom/path ..
```

## 15.2 头文件路径问题

> [!bug] 问题
> 编译时报错找不到头文件

**解决方案**：
1. 确保 `target_include_directories()` 设置正确
2. 检查 Config 文件中的 `INTERFACE_INCLUDE_DIRECTORIES`

## 15.3 库版本问题

> [!bug] 问题
> `Found unsuitable version of MyLibrary`

**解决方案**：
1. 检查版本兼容性设置
2. 重新安装正确版本的库

## 15.4 Windows DLL 问题

> [!bug] 问题
> Windows 上运行时找不到 DLL

**解决方案**：
1. 将 DLL 所在目录添加到 PATH
2. 或将 DLL 安装到可执行文件同目录

---

# 16 最佳实践总结

1. **使用 GNUInstallDirs**：遵循系统标准的目录布局
2. **使用生成器表达式**：使用 `$<BUILD_INTERFACE:...>` 和 `$<INSTALL_INTERFACE:...>` 区分构建和安装路径
3. **使用 EXPORT 导出目标**：生成可重定位的安装文件
4. **创建 Config 文件**：让库能被 find_package() 找到
5. **设置 VERSION 和 SOVERSION**：便于版本管理
6. **使用 NAMESPACE**：推荐使用 `MyLibrary::target` 格式
7. **提供版本文件**：使用 `write_basic_package_version_file()`
8. **处理依赖项**：使用 `find_dependency()` 声明依赖

---

# 相关教程

- [[04 Write CMakeLists]] - CMakeLists.txt 编写基础
- [[06 Build]] - 项目构建过程
- [[CMake Commands]] - CMake 命令参考

---

# 参考资料

- [CMake Official Documentation](https://cmake.org/documentation/)
- [GNUInstallDirs — CMake Documentation](https://cmake.org/cmake/help/latest/module/GNUInstallDirs.html)
- [find_package — CMake Documentation](https://cmake.org/cmake/help/latest/command/find_package.html)
- [CMake Professional Tips](https://cmake.org/cmake/help/latest/guide/importing-exporting/index.html)
