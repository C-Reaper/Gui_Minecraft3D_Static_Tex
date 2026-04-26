# Project README

## Overview
- This project includes a collection of C/C++ header files and source code intended for building various components of a software application. The main entry point is `Main.c`, which serves as the starting point for the application.

## Features
- **Mathematical Operations**: Basic vector and plane operations.
- **Triangle Clipping**: Clipping triangles against planes to determine their visibility based on a given plane.
- **Build System**: Support for multiple build systems including Linux, Windows, Wine, and WebAssembly using Emscripten or wasmtime.

## Project Structure
```
<Project>/
├── build/              # .exe files produced by Main.c
├── bin/                # .so / .dll produced by *.c in libs
├── libs/               # *.c for bin
├── lib/                # librarys for my own languages
├── code/               # scripts from my custom languages for example .rex, .ll, .omml
├── data/               # Datafile for example .txt or dumped files
├── assets/             # images and sound files
├── src/                # source code
│   ├── Main.c          # Entry point
│   └── *.h             # stand alone Header-based C-files, without *.c files that implement it
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
└── README.md           # This file
└── LICENCE
└── .gitignore
```

## Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools

## Build & Run
- **Build Process**:
  - Navigate to the project directory.
  - Execute `make -f Makefile.(os) all` where `(os)` is either `linux`, `windows`, `wine`, or `web`.
  
- **Clean Rebuild**:
  - To clean and rebuild, execute `make -f Makefile.(os) clean; make -f Makefile.(os) all`.

- **Build Libraries**:
  - If there are `./bin` and `./libs` directories, build the libraries with `make -f Makefile.(os) cleanlib; make -f Makefile.(os) lib`.

- **Execution**:
  - The executable can be run using `make -f Makefile.(os) exe`.