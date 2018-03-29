#CMakeLists.txt
#cmake -Htoolchain -B_builds -DCMAKE_TOOLCHAIN_FILE=toolchain.cmake
#cmake -Htoolchain -Bbin\ninja -G"Ninja" -DCMAKE_TOOLCHAIN_FILE=toolchain.cmake

cmake_minimum_required(VERSION 3.11)

message("Processing CMakeLists.txt")


message("Before 'project':")
message("	c: '${CMAKE_C_COMPILER}'")
message("	C++ '${CMAKE_CXX_COMPILER}'")

project(Foo)

message("After 'project':")
message("	C: '${CMAKE_C_COMPILER}'")
message("	C++ '${CMAKE_CXX_COMPILER}'")

add_library(foo foo.cpp)

