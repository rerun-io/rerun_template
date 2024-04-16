cmake_minimum_required(VERSION 3.16...3.27)

project(rerun_template LANGUAGES CXX) # TODO

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

if(NOT DEFINED CMAKE_CXX_STANDARD)
    set(CMAKE_CXX_STANDARD 17)
endif()

# Rerun:
include(FetchContent)
FetchContent_Declare(rerun_sdk URL https://github.com/rerun-io/rerun/releases/download/0.15.1/rerun_cpp_sdk.zip)
FetchContent_MakeAvailable(rerun_sdk)

add_executable(rerun_template src/main.cpp) # TODO
target_link_libraries(rerun_template rerun_sdk) # TODO
target_include_directories(rerun_template PRIVATE src) # TODO
