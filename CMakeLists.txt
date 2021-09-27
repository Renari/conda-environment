cmake_minimum_required(VERSION 3.20)
project(conda_environment)

set(CMAKE_CXX_STANDARD 14)

#*****************************************************************
#*** Enforce GCC version 10                                    ***
#*****************************************************************
if(CMAKE_CXX_COMPILER_VERSION VERSION_LESS 10
        OR CMAKE_CXX_COMPILER_VERSION VERSION_GREATER_EQUAL 11)
  message(FATAL_ERROR "Please use GCC10 to compile.")
endif()

add_executable(conda_environment main.cpp)
