# Erizo, a C/C++ Multipoint Control Unit (MCU) Library for WebRTC 

Erizo is a project that aims to implement a library able to communicate with WebRTC (http://www.webrtc.org) browser clients in order to provide advanced communication services. Currently it is tested on Ubuntu 11.10 and above but it should be able to be compiled on other distributions.

## Directory structure

- /src -  The root source directory
- /src/erizo - The source of the main library
- /src/examples - Examples and tests

## Requirements

- libSRTP version >= 1.4.4
- Libnice version >= 1.10
- boost_threads >= 1.49
- boost_regex >= 1.49 (optional, only for examples)
- boost_asio >= 1.49 (optional, only for examples)

- CMake >= 2.8 for building

## Building Instructions

This project is built using CMake.

The easiest way to build it is to use the provided scripts:
- Run ./generateProject.sh to run cmake, test the dependencies and generate the Makefile.
- Run ./buildProyect.sh to build the project after generating the Makefile. It simply runs make in the build directory.
- Run ./generateEclipseProyect.sh to generate an Eclipse CDT project which can be imported and used to work with the code.

If doxygen is availabe a "doc" target is generated. HTML documentation can be built by running "make doc" in the build directory.

##Examples

As of now, the only application built using the library is a streaming application that connects via TCP to a server application built on top of node.js.

The node.js app is not released but the code should provide an example on how the SDP exchange is made.
In the current state, the examples are not compiled by default, however, they can be built by setting COMPILE_EXAMPLES to ON in src/CMakeLists.txt

In the future, we will include here tests and examples.

## License

The MIT License

Copyright (C) 2012 Universidad Politecnica de Madrid.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
