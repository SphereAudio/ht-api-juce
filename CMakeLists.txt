cmake_minimum_required(VERSION 3.16)
project(headtracker)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(PROJECT_CODE_DIR "supperware")

add_library(${PROJECT_NAME} "")

file(GLOB_RECURSE PROJECT_CPP_FILES "${PROJECT_CODE_DIR}/*.cpp")
file(GLOB_RECURSE PROJECT_H_FILES "${PROJECT_CODE_DIR}/*.h")

target_sources(${PROJECT_NAME} 
            PRIVATE
                ${PROJECT_H_FILES}
                ${PROJECT_CPP_FILES}
)

target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_LIST_DIR})