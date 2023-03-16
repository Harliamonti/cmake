cmake_minimum_required(VERSION 3.14)
project(xyz)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_DEBUG "../../bin/debug")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_RELEASE "../../bin/release")

add_subdirectory(src)
add_subdirectory(app)

