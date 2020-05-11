cmake_minimum_required(VERSION 3.4)
project(solver)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(solver equation.cpp)
include_directories(../formatter-ex-lib)
add_subdirectory(../formatter_ex_lib formatter_ex)
add_library(solver_lib STATIC ../solver_lib/solver.cpp ../solver_lib/solver.h)
target_link_libraries(solver solver_lib formatter_ex)

