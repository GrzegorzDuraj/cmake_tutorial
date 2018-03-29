cmake_minimum_required(VERSION 3.11)

message("Before project:")
message("	Source: ${PROJECT_SOURCE_DIR}")
message("	Binary: ${PROJECT_BINARY_DIR}")
message("	Verision ${PROJECT_VERSION}")
message("	Version (alt): ${PROJECT_VERION_MAJOR}.${PROJECT_VERION_MINOR}.${PROJECT_VERSION_PATCH}")

project(Foo VERSION 1.2.7)

message("After project:")
message("	Source: ${PROJECT_SOURCE_DIR}")
message("	Binary: ${PROJECT_BINARY_DIR}")
message("	Version:${PROJECT_VERSION}")
message("	Version (alt): ${PROJECT_VERION_MAJOR}.${PROJECT_VERION_MINOR}.${PROJECT_VERSION_PATCH}")


