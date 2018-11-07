---
layout: page
title: Obtaining and Installing NJOY&mdash;for Developers
permalink: /Build/developers.html
---
* TOC
{:toc}

The instructions for building the development version is very similar to that of the static version of NJOY21. The development requirements are the same as for the static version. 

# Downloading

```bash
git clone https://github.com/njoy/NJOY21.git
```

## Updating
Due to the convenience of using git, updating the local NJOY21 repository is simple:

```bash
git pull
```

# Configuring
```bash
cd NJOY21
mkdir bin
cd bin
cmake ../
```

## CMake options
There are a few options that can be given as command-line options to `cmake` that will produce a little different behavior. The definition of these options is done by adding `-D option_name=value`. 

- `CMAKE_BUILD_TYPE` This is how you can specify whether you want to build in debug or release mode. Available options:
  - `debug` (default) This will build non-optimized with all the debug symbols in the code. 
  - `release` This configures NJOY21 for fast, optimized code.
- `fetched_subprojects` This indicates whether or not the components (subprojects) have already been "fetched" or downloaded. This is important when building offline.
  - `true` Specifies that the components have already been downloaded. Available options:
  - `false` (default) Components will be downloaded (using `git`) during the configuration phase.
- `unit_tests` Specify where or not to build the unit tests. Available options:
  - `ON` (default)
  - `OFF`
- `static` Specify whether or not to build static libraries. Available options:
  - `ON`
  - `OFF` (default)
- `njoy21_strict` Compile time warnings are converted to errors. Available options:
  - `ON` (default)
  - `OFF`

There are many other options available from `cmake` that are not given here. One of particular interest is:

- `CMAKE_INSTALL_PREFIX` With this option, you can specify where you want NJOY21 installed, such as:
  ```bash
  cmake -D CMAKE_INSTALL_PREFIX=~/bin ../
  ```
  This will install the compiled binary and headers in the `bin` directory in your home directory.

Other `cmake` options can be found on their [website](https://cmake.org).
# Compiling/Building
```bash
make
```
You can provide the optional command-line option `-j n` where `n` is the number of concurrent/parallel "jobs. This can greatly speed up the compilation. 

# Testing
```bash
make test
```
or equivalently
```bash
ctest
```

Like for the compiling step, you can pass the `-j` command-line option here as well.

If all the tests pass, you should see something that looks like:

```
100% tests passed, 0 tests failed out of 90
```

# Installing
Installation of NJOY21 is done like most any other project:
```bash
sudo make install
```
By default this will install the compiled binary and associated headers into `/usr/local`. (This can be changed using the `CMAKE_INSTALL_PREFIX` option as discussed above.) **Note** that this will require sufficient permissions to write to the appropriate install directory (thus the use of `sudo`).

# Building Offline
The options for building offline are the same as shown in the [standard building process](index.html).
