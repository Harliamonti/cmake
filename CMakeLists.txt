# Order actually matters!
cmake_minimum_required(VERSION 3.14)

project(test)

add_library(Hello STATIC ./src/hello.cpp)
add_executable(${PROJECT_NAME} main.cpp)

target_link_libraries(${PROJECT_NAME} PUBLIC Hello)
