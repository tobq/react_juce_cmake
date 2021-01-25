cmake_minimum_required(VERSION 3.15)
project(react_juce VERSION 0.1.0)
include(FetchContent)
set(CMAKE_CXX_STANDARD 17)

find_library(juce REQUIRED)

add_library(react_juce src/react_juce/react_juce.cpp)

target_include_directories(react_juce
        PUBLIC
        src

        private
        libs/duktape
        libs/duktape/duktape/src
        libs/yoga)

target_link_libraries(react_juce PUBLIC juce::juce_core juce::juce_graphics)