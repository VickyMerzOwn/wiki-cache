# HR-Cache

## Prerequisites

Before you build and run this project, ensure you have the following prerequisites installed on your system:

- **C++ Compiler**: A compiler that supports C++17 standards (e.g., GCC or Clang).
- **Git**: Required for cloning repositories, including LightGBM.
- **CMake**: Needed for building LightGBM from source.
- **pthread Library**: For multi-threading support.
- **cURL Library**: Necessary for network operations in the server component.
- **GNU Make**: For processing the Makefile.
- **LightGBM**: Our project depends on LightGBM, a gradient boosting framework. Instructions for building LightGBM are provided below.

## Building LightGBM
If LightGBM is not already installed and accessible by g++, follow these steps to build it from source:

```bash
mkdir -p builds
make build_lightgbm
```

This will build LightGBM from source.

## Building the Project

After installing LightGBM, you can compile the project using the following command:

```bash
mkdir -p builds
mkdir executables
make hr
```

This will compile the project and create the necessary executables.

## Trace Format:
Request traces are expected to be in a space-separated format with 3 columns:

* time (can be double)
* id should be a uint32, used to uniquely identify objects
* size should be uint32, this is object's size in bytes

| time | id | size |
|-----------------|-----------------|-----------------|
| 1  | 1  | 140  |
| 3  | 2  | 290  |
