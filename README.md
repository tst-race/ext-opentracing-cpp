# OpenTracing C++ API for RACE

This repo provides scripts to custom-build the
[OpenTracing C++ API library](https://github.com/opentracing/opentracing-cpp)
for RACE.

## License

The OpenTracing C++ API library is licensed under Apache 2.0.

Additionally the build scripts in this repo are licensed under Apache 2.0.

## Dependencies

OpenTracing C++ API has no dependencies on any custom-built libraries.

## How To Build

The [ext-builder](https://github.com/tst-race/ext-builder) image is used to
build OpenTracing C++ API.

```
git clone https://github.com/tst-race/ext-builder.git
git clone https://github.com/tst-race/ext-opentracing-cpp.git
./ext-builder/build.py \
    --target linux-x86_64 \
    ./ext-opentracing-cpp
```

## Platforms

OpenTracing C++ API is built for the following platforms:

* `linux-x86_64`
* `linux-arm64-v8a`
* `android-x86_64`
* `android-arm64-v8a`

## How It Is Used

OpenTracing C++ API is used directly by the RACE core. It is also a dependency
for the Jaeger Client library.
