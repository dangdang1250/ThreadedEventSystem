cmake_minimum_required(VERSION 3.12.0)
project(eventdriven VERSION 0.1.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

message(STATUS "[INFO]${PYTHON_EXECUTABLE}")

# example library
add_library(core 
    STATIC
    Subscriber.cpp
    Dispatcher.cpp
    GameThing.cpp
)

# main code
add_executable(app Main.cpp)

target_link_libraries(app core)