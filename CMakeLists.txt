#Project nay su dung lib
cmake_minimum_required(VERSION 3.0.0) 

project(App)

add_subdirectory(Lib_1)
add_subdirectory(Lib_2)

add_executable(App Test_App/main.cpp)
include_directories(App PUBLIC Lib_1 Lib_2)
target_link_libraries(App PUBLIC Adder Print)