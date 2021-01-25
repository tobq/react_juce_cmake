cmake_minimum_required(VERSION 3.15)
project(react_juce VERSION 0.1.0)
include(FetchContent)
set(CMAKE_CXX_STANDARD 17)

find_library(juce REQUIRED)

add_library(react_juce src/juce_react/react_juce.cpp)

target_include_directories(react_juce
        PUBLIC
        src

        private
        libs/duktape
        libs/duktape/duktape/src
        libs/yoga)
target_link_libraries(react_juce PUBLIC
        juce::juce_recommended_config_flags
        juce::juce_recommended_lto_flags
        juce::juce_recommended_warning_flags
        juce::juce_core
        juce::juce_audio_basics
        juce::juce_audio_devices
        juce::juce_audio_processors
        juce::juce_audio_utils
        juce::juce_graphics
        juce::juce_gui_basics)