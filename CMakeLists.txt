cmake_minimum_required(VERSION 3.3)
project(rastertokpsl-re)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/bin")
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -std=c11")

set (SRC_DIR ${PROJECT_SOURCE_DIR}/src)
set (CUPS_SRC_DIR ${SRC_DIR}/cups-2.1.1)
set (UNICODE_SRC_DIR ${SRC_DIR}/unicode)

find_library(CUPS_LIB cups)
find_library(CUPSIMAGE_LIB cupsimage)

add_subdirectory(src)
add_subdirectory(tests)
