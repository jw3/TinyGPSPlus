cmake_minimum_required(VERSION 3.0)
project(tinygps++ CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_VERBOSE_MAKEFILE ON)

set(GCC_ARM_PATH /usr/local/gcc-arm/bin)
set(GCC_ARM_PREFIX arm-none-eabi-)

set(CMAKE_CXX_COMPILER ${GCC_ARM_PATH}/${GCC_ARM_PREFIX}g++)

add_subdirectory(src)
