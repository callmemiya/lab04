cmake_minimum_required(VERSION 3.4)
project(formatter_exlib)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories(../formatter_lib)
add_subdirectory(../formatter_lib formatter)
add_library(formatter_ex STATIC formatter_ex.cpp formatter_ex.h)

target_link_libraries(formatter_ex formatter)
