cmake_minimum_required(VERSION 3.25)

project(
  work
  VERSION 0.1.0
  LANGUAGES C CXX)

set(CMAKE_C_STANDARD 17)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_C_EXTENSIONS OFF)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable(work src/main.cpp)
target_compile_options(work PRIVATE -fno-exceptions -fno-rtti)
