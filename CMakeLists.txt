cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

set(LIBRARY_NAME parson)

set(CMAKE_C_FLAGS "-g -Wall")

set(SOURCE_FILES parson.h parson.c)

add_library(${LIBRARY_NAME} ${SOURCE_FILES})

target_include_directories(${LIBRARY_NAME} PUBLIC
   $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
   $<INSTALL_INTERFACE:.>
)
