cmake_minimum_required(VERSION 3.10)

project(DuckProto LANGUAGES C)
set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED ON)

include_directories(${PROJECT_SOURCE_DIR}/include)


find_package(PkgConfig REQUIRED)
pkg_check_modules(SODIUM REQUIRED libsodium)
include_directories(${SODIUM_INCLUDE_DIRS})
link_directories(${SODIUM_LIBRARY_DIRS})

set(SOURCES
    src/duckproto.c
    src/encrypt.c
)


add_library(duckproto STATIC ${SOURCES})

add_executable(demo examples/demo.c)

target_link_libraries(demo PRIVATE duckproto)