---
layout: page
title: Getting started
permalink: /getting-started/
nav_order: 1
---

## Build Requirements

- Swift 5.4 or newer
- Windows SDK 10.0.107763 or newer
- CMake 3.16 or newer

## Building

This project requires Swift 5.4 or newer. You can use the the snapshot binaries from [swift.org](https://swift.org/download/), download the nightly build from [Azure](https://dev.azure.com/compnerd/swift-build), or build the Swift compiler from source.

### Recommended (CMake)

The following example session shows how to build with CMake 3.16 or newer.

```sh
cmake -B build -D BUILD_SHARED_LIBS=YES -D CMAKE_BUILD_TYPE=Release -D CMAKE_Swift_FLAGS="-sdk %SDKROOT%" -G Ninja -S .
ninja -C build SwiftWin32 UICatalog

%CD%\build\bin\UICatalog.exe
```

### Swift Package Manager

Building this project with swift-package-manager is supported although CMake is recommended for ease.  The Swift Package Manager based build is required for code completion via SourceKit-LSP.  It also allows for the use of Swift/Win32 in other applications using SPM.  In order to use SPM to build this project additional post-build steps are required to use the demo applications.

The following known limitations are known:

1. It is not possible to deploy auxiliary files which are required for Swift/Win32 based applications to function to the correct location.
2. It is not possible to build and run multiple demo projects as the auxiliary files collide.

```sh
swift build --product UICatalog
mt -nologo -manifest Examples\UICatalog\UICatalog.exe.manifest -outputresource:.build\x86_64-unknown-windows-msvc\debug\UICatalog.exe
copy Examples\UICatalog\Info.plist .build\x86_64-unknown-windows-msvc\debug\
.build\x86_64-unknown-windows-msvc\debug\UICatalog.exe
```
