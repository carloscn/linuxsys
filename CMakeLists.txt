cmake_minimum_required(VERSION 3.17)
project(linuxsys C)

set(CMAKE_C_STANDARD 99)
AUX_SOURCE_DIRECTORY(src DIR_SRCS)
SET(SRC_PATH ${DIR_SRCS} src/ut.c src/main.c)
include_directories(./inc)
#include_directories(${openssl_dir}/lib ${mbedtls_dir}/library)
#link_libraries(
#        ${openssl_dir}/lib/libssl.lib
#        -lws2_32
#)

add_executable(${PROJECT_NAME} ${SRC_PATH})