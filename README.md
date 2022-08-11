# learn-cmake
## 内置变量
### CMAKE_BUILD_TYPE
`CMAKE_BUILD_TYPE`，是CMake中内置变量，用于控制构建类型
* Debug，调试模式，完全不优化，生成调试信息，方便调试程序。
* Release，发布模式，优化程度最高，性能最佳，编译比Debug慢。
* MinSizeRel，最小发布，生成文件币Release小，不完全优化，减少二进制大小。
* RelWithDebInfo，带调试信息发布，生成文件币Release大，因为带有调试信息。  
若不指定CMAKE_BUILD_TYPE，按Debug模式构建。   
### 让用户默认按Release构建
```cmake
if (NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE Release)
endif()
```
### PROJECT_SOURCE_DIR
### PROJECT_BINARY_DIR
### CMAKE_CURRENT_SOURCE_DIR
`CMAKE_CURRENT_SOURCE_DIR`，指当前源码目录。
### CMAKE_CURRENT_BINARY_DIR
`CMKAE_CURRENT_BINARY_DIR`，指当前输出目录。
### PROJECT_IS_TOP_LEVEL
### CMAKE_PROJECT_NAME
### CMAKE_CXX_STANDARD
```cmake
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)
project(hello LANGUAGES C CXX)
```










