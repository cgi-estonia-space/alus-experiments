cmake_minimum_required(VERSION 3.20)
project(alus-experiments CXX)

message(STATUS "CMake version: ${CMAKE_VERSION}")

set(CMAKE_CXX_STANDARD  17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -Werror -pedantic ")

add_executable(host-memory-allocation ${CMAKE_CURRENT_LIST_DIR}/src/host_memory_allocation.cc)

