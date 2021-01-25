# react_juce with cmake integration

## Usage

```cmake
# load downloaded project
add_subdirectory(react_juce)

#### or...

# fetch project from github 
FetchContent_Declare(react_juce
        GIT_REPOSITORY https://github.com/tobq/react_juce_cmake.git
        GIT_TAG master)
# load fetched project
FetchContent_MakeAvailable(react_juce)
```
Then 
```cmake
target_link_libraries(${TARGE_NAME} PRIVATE react_juce)
```
