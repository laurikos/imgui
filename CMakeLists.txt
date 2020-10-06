cmake_minimum_required(VERSION 3.16)

project(imgui)

FILE(GLOB imguiCpp ${PROJECT_SOURCE_DIR}/*.cpp)
FILE(GLOB imguiHeaders ${PROJECT_SOURCE_DIR}/*.h)

add_library(imgui STATIC
                 ${imguiHeaders}
                 ${imguiCpp}
                 )
                 
target_include_directories(imgui PUBLIC ${PROJECT_SOURCE_DIR}/imgui.h)
