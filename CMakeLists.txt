cmake_minimum_required(VERSION 3.16)
project(Attractor)

set(CMAKE_CXX_STANDARD 20)

set(CMAKE_EXE_LINKER_FLAGS "-static")

add_compile_options(-Wall -Wextra -Wconversion -Werror)
add_compile_options(-D_GLIBCXX -g)
add_compile_options(-O3 -march=native)

file(GLOB_RECURSE SOURCES RELATIVE ${CMAKE_SOURCE_DIR} "src/*" )

add_executable(
    attractor
    main.cpp
    ${SOURCES}
)