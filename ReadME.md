# WxWidgets Scaffold
A scaffold project to use `wxwidgets` as GUI library. It is consumed using `git submodules` as a subdirectory.

## Get sources
Clone the repository:
```bash
git clone --recurse-submodules https://github.com/bc913/wxwidgets_scaffold.git
```
- Update the submodules when required:
```bash
git submodule update --init --recursive
```
## Build
### Requirements
- CMake
- C/C++ Compiler
### Run
```bash
# Configure (wxwidgetds as shared library)
cmake -S . -B build -G "Visual Studio 16 2019" -DCMAKE_INSTALL_PREFIX=install
# Build and install
cmake --build build --config Release --target install
```

## References
- [Can't find the shared library in Ubuntu issue](https://stackoverflow.com/questions/32469953/why-is-cmake-designed-so-that-it-removes-runtime-path-when-installing)
