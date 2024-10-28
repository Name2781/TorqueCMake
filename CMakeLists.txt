cmake_minimum_required(VERSION 3.8)

project("torque")

add_definitions(-DUNICODE -D_UNICODE)
add_subdirectory("engine")
target_include_directories(engine PUBLIC "engine")