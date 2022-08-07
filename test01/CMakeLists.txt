cmake_minimum_required(VERSION 3.16.3)
project(test01)
add_executable(${PROJECT_NAME} main.cpp)

add_subdirectory(math)

target_include_directories(${PROJECT_NAME} PUBLIC math)

target_link_directories(${PROJECT_NAME} PUBLIC /usr/local)
target_link_libraries(${PROJECT_NAME} adder sub)

