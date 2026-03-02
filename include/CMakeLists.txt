cmake_minimum_required(VERSION 3.10)

project(calculator C)

enable_testing()

include_directories(include)

add_executable(calculator
    src/main.c
    src/lib/calculator.c
)

# Tests automatiques
add_test(NAME TestAdd COMMAND calculator add 2 3)
add_test(NAME TestSub COMMAND calculator sub 5 3)
add_test(NAME TestMul COMMAND calculator mul 4 3)
add_test(NAME TestDiv COMMAND calculator div 10 2)
add_test(NAME TestCar COMMAND calculator car 5)