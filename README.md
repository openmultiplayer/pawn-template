 open.mp Pawn Component Template
=================================

This is a simple component start point template.  It demonstrates how to declare pawn functions using the *pawn-natives* derived syntax (old methods are still available) and add per-player data managed by the server.

## UID

Since this is a template, i.e. a start point for new components, it needs a Unique ID adding.  Don't forget to get a new one from here:

https://open.mp/uid

## Required Tools

* [CMake 3.19+](https://cmake.org/)
* [Conan 1.53+](https://conan.io/)
* [Visual Studio 2019+](https://www.visualstudio.com/) (on Windows)
* Clang (on Linux)

Visual Studio needs the `Desktop development with C++` workload with the `MSVC v142`, `Windows 10 SDK`, and `C++ Clang tools for Windows` components.

## Sources

```bash
# With HTTPS:
git clone --recursive https://github.com/openmultiplayer/basic-template
# With SSH:
git clone --recursive git@github.com:openmultiplayer/basic-template
```

Note the use of the `--recursive` argument, because this repository contains submodules.

## Building on Windows

```bash
mkdir build
cd build
cmake .. -A Win32 -T ClangCL
```

Open Visual Studio and build the solution.

## Building on Linux

```bash
mkdir build
cd build
# May need to configure this line.
export CC=/usr/lib/llvm/13/bin/clang CXX=/usr/lib/llvm/13/bin/clang++
cmake .. -G Ninja -DCMAKE_C_FLAGS=-m32 -DCMAKE_CXX_FLAGS=-m32 -DCMAKE_BUILD_TYPE=Debug \
cmake --build . --config Debug
```

Change `Debug` to `Release` for final versions.

