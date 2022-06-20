cmake_minimum_required(VERSION 3.0)
project(BLOCKS)

add_library(shared SHARED source/block.c headers/block.h)
add_library(static STATIC source/block.c headers/block.h)

add_executable(dynamic_block program.c)
target_link_libraries(dynamic_block shared)

add_executable(static_block program.c)
target_link_libraries(static_block static)
