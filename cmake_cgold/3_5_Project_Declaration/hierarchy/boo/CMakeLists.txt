cmake_minimum_required(VERSION 3.11)

project(boo)

message("From subdirectory: 'boo'")
message("	Source (general): ${PROJECT_SOURCE_DIR}")
message("	Source (foo) ${foo_SOURCE_DIR}")
message("	Source (boo) ${boo_SOURCE_DIR}")

