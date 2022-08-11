# 指定cmake版本
cmake_minimum_required(VERSION 3.16.3)

# 设置项目名
project(HelloWorld
        LANGUAGES CXX
        VERSION 0.2.3
        DESCRIPTION "A cmake hello world."
        HOMEPAGE_URL https://github.com/DeepinBlocks/learn-cmake)

message("PROJECT_VERSION: ${PROJECT_VERSION}")
message("PROJECT_VERSION_MAJOR: ${PROJECT_VERSION_MAJOR}") # 主版本号
message("PROJECT_VERSION_MINOR: ${PROJECT_VERSION_MINOR}") # 次版本号
message("PROJECT_VERSION_PATCH: ${PROJECT_VERSION_PATCH}") # 补丁版本号

message("PROJECT_VERSION: ${${PROJECT_NAME}_VERSION}")
message("PROJECT_SOURCE_DIR: ${PROJECT_SOURCE_DIR}")
message("PROJECT_SOURCE_DIR: ${${PROJECT_NAME}_SOURCE_DIR}")

# 相关变量
# PROJECT_NAME：值是project里面的内容
# 取变量的值(解引用)：使用“${var}”, "${PROJECT_NAME}"

# 设置可执行程序
# 第1个参数：可执行文件名字
# 第2个参数：源文件
add_executable("${PROJECT_NAME}" main.cpp)

# bin: ${CMAKE_INSTALL_PREFIX}/bin
install(TARGETS "${PROJECT_NAME}" DESTINATION bin)

# src: ${CMAKE_INSTALL_PREFIX}/src
install(FILES main.cpp DESTINATION src)
