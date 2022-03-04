Example Client/Server project showing how to use gRPC, Conan and CMake

# Build C++ project

## Prerequisites 

* [Conan](https://conan.io/) (tested with 1.45.0)
* [Cmake](https://cmake.org/) (tested with 3.20 - the one shipped with MSVC 2019)
* Working build tools (tested with MSVC 2019)

```
cmake -S . -B build
cmake --build build --parallel 12 --config Release
```

# Run server
```
./build/bin/server
```

# Run client
```
./build/bin/client
```

# Docker server
```
docker build -t grpctest .
docker run --rm -it -p 50051:50051 grpctest build/bin/server
```
