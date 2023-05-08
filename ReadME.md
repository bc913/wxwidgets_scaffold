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
### Links
- [Can't find the shared library in Ubuntu issue](https://stackoverflow.com/questions/32469953/why-is-cmake-designed-so-that-it-removes-runtime-path-when-installing)

### Books
- [Cross-Platform GUI Programmingwith wxWidgets](https://www.wxwidgets.org/docs/book/Cross-Platform%20GUI%20Programming%20with%20wxWidgets.pdf)


### Sample Repos
- [PBfordev](https://github.com/PBfordev)
- [Audacity](https://github.com/audacity/audacity)
- [Tonetyrant (Non Cmake cross platform deployment)](https://github.com/michgz/tonetyrant)
