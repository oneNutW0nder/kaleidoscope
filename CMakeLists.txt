# refer to the root source directory of the project as ${KALEIDOSCOPE_SOURCE_DIR} and
# to the root binary directory of the project as ${KALEIDOSCOPE_BINARY_DIR}.
cmake_minimum_required(VERSION 3.1...3.23)
project(
  KALEIDOSCOPE
  VERSION 0.1
  LANGUAGES CXX
)

# Enforce cpp20
# TODO: This is not a good way to enforce this. It should be done at the target level instead
set(CMAKE_CXX_STANDARD 20)
# add_compile_options(--std=c++20)

# Use llvm libc++ first instead of system
# TODO: THis is not good practice and makes this project not portable
#       Can I use some kind of cmake IF logic here?
add_link_options(-L /Users/onenutw0nder/.local/share/llvm/lib  -Wl,-rpath,/Users/onenutw0nder/.local/share/llvm/lib  -lc++)

# General compilation
add_subdirectory(./src/)
