# Order actually matters!
cmake_minimum_required(VERSION 3.14)

project(test)

set(LIBRARY_SOURCES 
    "./src/hello.cpp")
set(LIBRARY_HEADERS
    "./include/hello.h")

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_DEBUG "../bin/debug")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_RELEASE "../bin/release")


add_library(Library STATIC ${LIBRARY_SOURCES} ${LIBRARY_HEADERS})
add_executable(${PROJECT_NAME} main.cpp)

target_link_libraries(${PROJECT_NAME} PUBLIC Library)
