cmake_minimum_required(VERSION 3.10.0)
project(helloworld VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()

file(GLOB source_dir
     "./src/*.cpp"
)
file(GLOB header_dir
     "./headers/*.h"
)

set(HEADER_FILES ${header_dir})

add_executable(helloworld ${source_dir} ${header_dir})
include_directories()

set_property(TARGET helloworld PROPERTY CXX_STANDARD 17)
target_include_directories(helloworld PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/headers")
