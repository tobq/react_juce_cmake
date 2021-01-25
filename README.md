# [react_juce](https://github.com/nick-thompson/blueprint/tree/master/react_juce) with cmake integration

## Usage

### 1. Load in the project
```cmake
# load downloaded project
add_subdirectory(react_juce)
```
or...

```cmake
# declare github project 
FetchContent_Declare(react_juce
        GIT_REPOSITORY https://github.com/tobq/react_juce_cmake.git
        GIT_TAG main)
# fetched / load project
FetchContent_MakeAvailable(react_juce)
```
### 2. Link to react_juce
```cmake
target_link_libraries(${TARGET_NAME} PRIVATE react_juce)
```
