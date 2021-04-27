cmake_minimum_required(VERSION 1.9)
project(hello)
add_executable(hello hello.cpp)
install(TARGETS hello RUNTIME DESTINATION bin)