cmake_minimum_required(VERSION 3.16)

project(calculator C)

enable_testing()

add_executable(calculator
    src/main.c
    src/lib/calculator.c
)

target_include_directories(calculator PRIVATE
    include
)

add_test(NAME t1 COMMAND calculator add 2 3)
add_test(NAME t2 COMMAND calculator sub 3 -2)
add_test(NAME t3 COMMAND calculator mul 5 5)
add_test(NAME t4 COMMAND calculator div 1 5)
add_test(NAME t5 COMMAND calculator car 5)