cmake_minimum_required(VERSION 3.10.0)
project(helloworld VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()

file(GLOB source_dir
     "./src/*.cpp"
)

include_directories("${CMAKE_CURRENT_SOURCE_DIR}/headers")
add_executable(helloworld ${source_dir})

set_property(TARGET helloworld PROPERTY CXX_STANDARD 17)

