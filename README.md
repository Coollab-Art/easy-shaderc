# easy-shaderc

This is a wrapper for [*shaderc*](https://github.com/google/shaderc) and its dependencies. Its aim is to make it easy to build *shaderc* from source and include it in your own project.

Add this repository as a submodule and in your *CMakeLists.txt* do:
```cmake
add_subdirectory(path/to/easy-shaderc)
target_link_libraries(YourTargetName PUBLIC easy_shaderc::shaderc)
```

And that should be it!