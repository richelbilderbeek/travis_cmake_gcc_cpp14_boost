cmake_minimum_required (VERSION 2.6)
add_executable(travis_cmake_gcc_cpp14_boost main.cpp)

# C++14
set_property(TARGET travis_cmake_gcc_cpp14_boost PROPERTY CXX_STANDARD 14)
set_property(TARGET travis_cmake_gcc_cpp14_boost PROPERTY CXX_STANDARD_REQUIRED ON)

# Boost
find_package(Boost) 
include_directories(${Boost_INCLUDE_DIRS}) 
