This repository holds the CMakeList.txt file for compiling the [AES implementation by BrianGladman](https://github.com/BrianGladman/aes).

How to use:

1. Download the source code of both repositories, e.g.:

```
git clone https://github.com/madwyn/aes-gladman-cmake.git
git clone https://github.com/BrianGladman/aes.git
```

```
/aes_gladman_cmake
/aes
CMakeLists.txt
```

2. In the `CMakeLists.txt`

```
set(AES_GLADMAN_ROOT ${CMAKE_CURRENT_LIST_DIR}/aes)
add_subdirectory(aes_gladman_cmake)
```

3. Link the target

```
target_link_libraries(example_app aes_Gladman)
```
