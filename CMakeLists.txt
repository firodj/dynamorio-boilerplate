cmake_minimum_required(VERSION 3.9)

# set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

option(test "Build all tests." OFF)

project(dynamorio-boilerplate)

find_package(DynamoRIO)

if (NOT DynamoRIO_FOUND)
    message(FATAL_ERROR "DynamoRIO package required to build")
endif(NOT DynamoRIO_FOUND)

add_library(bbbuf SHARED src/bbbuf.c)

configure_DynamoRIO_client(bbbuf)
use_DynamoRIO_extension(bbbuf drmgr)
use_DynamoRIO_extension(bbbuf drreg)
use_DynamoRIO_extension(bbbuf drx)
# use_DynamoRIO_extension(bbbuf drwrap)
# use_DynamoRIO_extension(bbbuf drutil)
# use_DynamoRIO_extension(bbbuf drcontainers)

