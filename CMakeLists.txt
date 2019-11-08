cmake_minimum_required(VERSION 3.1)
project(
  pystring
  VERSION 0.1
  LANGUAGES C CXX)

set(PYSTRING_SOURCE_DIR "${CMAKE_CURRENT_SOURCE_DIR}")

add_library(pystring "${PYSTRING_SOURCE_DIR}/pystring.cpp")
target_include_directories(pystring PUBLIC "${PYSTRING_SOURCE_DIR}")

add_library(pystring::pystring ALIAS pystring)
