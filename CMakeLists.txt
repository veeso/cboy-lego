cmake_minimum_required(VERSION 2.4)

project(cboy)

add_compile_options(-Wall -Wextra)

if(NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Debug)
endif()

set(CMAKE_C_FLAGS_DEBUG "-O1 -g -fsanitize=address")
set(CMAKE_C_FLAGS_RELEASE "-Ofast -DNDEBUG")

set(CMAKE_STATIC_LIBRARY_PREFIX "")

add_subdirectory(libcboy)
add_subdirectory(cboy)
