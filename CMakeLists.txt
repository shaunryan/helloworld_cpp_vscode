cmake_minimum_required(VERSION 3.10.0)
project(helloworld VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()

file(GLOB helloworld_SRC
     "./src/*.h"
     "./src/*.cpp"
)
add_executable(helloworld ${helloworld_SRC})

set_property(TARGET helloworld PROPERTY CXX_STANDARD 17)

