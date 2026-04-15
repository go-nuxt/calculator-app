cmake_minimum_required(VERSION 3.10)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

project(CalculatorApp C)

set(CMAKE_C_STANDARD 11)

# Module
add_subdirectory(src/calc)
add_subdirectory(src/io)

# Main
add_executable(app src/main.c)

# Link Module
target_link_libraries(app calc io)
