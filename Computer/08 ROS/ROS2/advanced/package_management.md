ROS2 使用 `colcon` 对包进行管理，当使用 `ament_cmake/ament_python` 进行编译时，每个功能包都需要由对应的 `package.xml` 来描述包。

# 01 install

当使用 `colcon` 对 ROS2 的功能包进行编译的时候，会自动为 `CMake` 传递一些参数：

- `CMAKE_INSTALL_PREFIX=install` - 管理安装的位置
- ...

因此我们需要了解安装目录的结构，以此来了解如何在 ROS2 的开发中管理外部依赖。

```
install/
├── _local_setup_util_ps1.py
├── _local_setup_util_sh.py
├── COLCON_IGNORE
├── local_setup.bash
├── local_setup.ps1
├── local_setup.sh
├── local_setup.zsh
├── mpcl/
│   ├── include
│   ├── lib
│   └── share
├── serial/
│   ├── include
│   ├── lib
│   └── share
├── setup.bash
├── setup.ps1
├── setup.sh
├── setup.zsh
└── test_lib/
    ├── lib
    └── share
```

`install` 目录分为 `packages` 和 `config_scripts` ，各种脚本都是用于配置环境的。而每一个包的目录结构才需要我们注意。

与 GNU 标准不同的是，GNU 标准将所有的包合并安装，只有 `lib/` ， `include/` ， `share/` ， `bin/` 等目录，而 ROS2 则将每一个包隔离开来，每个包都有自己的目录，最后通过脚本来管理环境。

我们先看 `serial/` :

```
serial/
├── include/
│   └── serial/
│       ├── impl/
│       │   ├── unix.h
│       │   └── win.h
│       ├── serial.h
│       └── v8stdint.h
├── lib/
│   └── libserial.a
└── share/
    ├── ament_index/
    │   └── resource_index/
    │       ├── package_run_dependencies/
    │       │   └── serial
    │       ├── packages/
    │       │   └── serial
    │       └── parent_prefix_path/
    │           └── serial
    ├── colcon-core/
    │   └── packages/
    │       └── serial
    └── serial/
        ├── cmake/
        │   ├── ament_cmake_export_dependencies-extras.cmake
        │   ├── ament_cmake_export_include_directories-extras.cmake
        │   ├── ament_cmake_export_libraries-extras.cmake
        │   ├── serialConfig-version.cmake
        │   └── serialConfig.cmake
        ├── environment/
        │   ├── ament_prefix_path.dsv
        │   ├── ament_prefix_path.sh
        │   ├── library_path.dsv
        │   ├── library_path.sh
        │   ├── path.dsv
        │   └── path.sh
        ├── hook/
        │   ├── cmake_prefix_path.dsv
        │   ├── cmake_prefix_path.ps1
        │   └── cmake_prefix_path.sh
        ├── local_setup.bash
        ├── local_setup.dsv
        ├── local_setup.sh
        ├── local_setup.zsh
        ├── package.bash
        ├── package.dsv
        ├── package.ps1
        ├── package.sh
        ├── package.xml
        └── package.zsh

```

其中，我们需要关注的是 `share/serial/cmake` 目录。这个目录配置了 `serialConfig.cmake` ，用于 `find_package()` 来找到当前的库。

> [!note] 
> 因此，当我们需要将外部库和ROS2的功能包统一管理时，需要配置其 `CMakeLists.txt` 中的 `install` 功能，使最终的安装结果与ROS2一致。

举个简单的例子，我们有如下的第三方库：

```
mpcl/
├── cmake/
│   └── mpclConfig.cmake.in
├── CMakeLists.txt
├── include/
│   └── mpcl/
│       ├── converter.hpp
│       ├── filter.hpp
│       ├── projector.hpp
│       └── types.hpp
├── main.cpp
├── README.md
└── src/
    ├── converter.cpp
    ├── filter.cpp
    └── projector.cpp
```

我们可以这样配置 `CMakeLists.txt` ：

```cmake
cmake_minimum_required(VERSION 3.5)
project(mpcl VERSION 1.0)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

find_package(OpenCV REQUIRED)
find_package(PCL REQUIRED)

find_package(OpenMP)
if(OpenMP_CXX_FOUND)
    message(STATUS "OpenMP found, parallel projection enabled")
    set(OMP_FLAGS ${OpenMP_CXX_FLAGS})
else()
    message(STATUS "OpenMP not found, using serial projection")
    set(OMP_FLAGS "")
endif()

aux_source_directory(./src MPCL_SOURCE)

add_library(mpcl SHARED ${MPCL_SOURCE})
target_include_directories(mpcl PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>    # 构建时用
    $<INSTALL_INTERFACE:include>                              # 安装后用
)

target_link_libraries(mpcl ${OpenCV_LIBRARIES})
target_include_directories(mpcl PUBLIC ${OpenCV_INCLUDE_DIRS})
target_link_libraries(mpcl ${PCL_LIBRARIES})
target_include_directories(mpcl PUBLIC ${PCL_INCLUDE_DIRS})

if(OpenMP_CXX_FOUND)
    target_compile_options(mpcl INTERFACE ${OpenMP_CXX_FLAGS})
    target_link_libraries(mpcl ${OpenMP_CXX_FLAGS})
endif()

add_executable(mpcl_test ./main.cpp)
target_link_libraries(mpcl_test mpcl)


# 配置 ${PROJECT_NAME}Config.cmake 供 find_package() 查找
include(CMakePackageConfigHelpers)

configure_package_config_file(
    ${CMAKE_CURRENT_SOURCE_DIR}/cmake/${PROJECT_NAME}Config.cmake.in
    ${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}Config.cmake
    INSTALL_DESTINATION share/${PROJECT_NAME}/cmake
)

write_basic_package_version_file(
    ${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}ConfigVersion.cmake
    VERSION ${PROJECT_VERSION}
    COMPATIBILITY SameMajorVersion
)

# 设置安装目录
set(
    CMAKE_INSTALL_PREFIX
    ${CMAKE_CURRENT_SOURCE_DIR}/../../install/${PROJECT_NAME}
)

# install lib
install(
    TARGETS ${PROJECT_NAME}
    EXPORT ${PROJECT_NAME}-targets
    LIBRARY DESTINATION lib/${PROJECT_NAME}
    ARCHIVE DESTINATION lib/${PROJECT_NAME}
    INCLUDES DESTINATION lib/${PROJECT_NAME}
)

# install include
install(
    DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/
    DESTINATION include
)

# export ${PROJECT_NAME}-targets.cmake for a lib
install(
    EXPORT ${PROJECT_NAME}-targets
    FILE ${PROJECT_NAME}-targets.cmake
    NAMESPACE ${PROJECT_NAME}::
    DESTINATION share/${PROJECT_NAME}/cmake
)

# install ${PROJECT_NAME}Config.cmake
install(
    FILES
    ${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}Config.cmake
    ${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}ConfigVersion.cmake
    DESTINATION share/${PROJECT_NAME}/cmake
)
```

需要有一个用于配置 `${PROJECT_NAME}Config.cmake` 的模板文件 `${PROJECT_NAME}Config.cmake.in` ：

```cmake
# ${PROJECT_NAME}Config.cmake.in
@PACKAGE_INIT@

# 添加 `${PROJECT_NAME}-targets.cmake`
include("${CMAKE_CURRENT_LIST_DIR}/mpcl-targets.cmake")

# 传递依赖
find_dependency(PCL REQUIRED)

check_required_components(mpcl)
```

这个时候设置完 `CMAKE_PREFIX_PATH` 后就可以通过 `find_package()` 来找到：

```cmake
list(APPEND CMAKE_PREFIX_PATH <install_dir>)
find_package(mpcl REQUIRED)
```

> [!note] 
> 使用 `list(APPEND VARIABLE VALUE)` 可以向变量追加值， `CMAKE_PREFIX_PATH` 通常包含许多默认路径，不能直接覆盖

# 02 build

构建的时候唯一需要注意的就是依赖关系的先后顺序，在 `package.xml` 中指明 `<depend>mpcl</depend>` ，那么这个包就会在 `mpcl` 之后构建，以保证依赖的正确传递。