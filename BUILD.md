# Building clipper2c

C bindings for Clipper2, built with CMake. Clipper2 itself is the git submodule
`vendor/Clipper2`.

## External dependencies

| What | Debian/Ubuntu | Fedora | Alpine | macOS | Windows |
|---|---|---|---|---|---|
| CMake ≥ 3.18 | `cmake` | `cmake` | `cmake` | `brew install cmake` | CMake installer / `winget install Kitware.CMake` |
| C++17 compiler + build tool | `build-essential` | `gcc-c++ make` | `build-base` | Xcode Command Line Tools | Visual Studio 2022 "Desktop development with C++" |

## Build

```bash
git submodule update --init --recursive
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build
```

Rust users normally don't build this directly: `clipper2-sys` (fork-rust-clipper2-sys)
compiles these sources itself through its own `build.rs`.
