cmake_minimum_required(VERSION 2.8)
project(HelloSlam)
set (CMKE_BUILD_TYPE "Debug")
add_executable(helloSlam helloSLAM.cpp)

add_library(hello_shared SHARED libHelloSLAM.cpp)

add_executable(useHello useHello.cpp)

target_link_libraries(useHello hello_shared)
