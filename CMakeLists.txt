
cmake_minimum_required(VERSION 3.5)
project(github-test C)

set(CMAKE_SHARED_LIBRARY_PREFIX "")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}")
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}")


set(BUILD_TESTS ON CACHE BOOL "Disable building tests.")


add_subdirectory(src)
if(BUILD_TESTS)
    enable_testing()
    add_subdirectory(tests)
endif()
