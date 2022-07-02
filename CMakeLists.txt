cmake_minimum_required(VERSION 3.0.0)
project(router VERSION 0.1.0)

include(CTest)
enable_testing()

file(GLOB_RECURSE SOURCE_FILES src/*.c)
add_executable(router main.c ${SOURCE_FILES})

target_include_directories(router PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
