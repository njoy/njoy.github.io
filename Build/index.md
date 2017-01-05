---
layout: page
title: Obtaining and Installing NJOY
permalink: /Build/index.html
---

Both [NJOY21](https://github.com/njoy) and [NJOY2016](https://github.com/njoy) use the same configuration and build process. Additionally, all of the supporting [projects](/Projects.html) use the same process. 

### For the impatient

```bash
# Download the source code
git clone https://github.com/njoy/NJOY21.git

# Configure the build process
cd NJOY21
mkdir bin
cd bin
cmake ../

# Build NJOY21
make

# Test NJOY21
make test
```

## Prerequisites
Development for NJOY uses the latest published language standards that are widely supported by compiler vendors, *at the start of development*. Therefore, the minimum language standards are

 - C++14 or higher
 - Fortran 2003 or higher
 - [Python 3.4+](https://python.org/)

Additionally, we use [CMake](https://cmake.org/) to configure the build system and [git](https://git-scm.com) for version control.

 - [CMake 3.2+](https://cmake.org/) 
 - [git 2.1+](https://git-scm.com)


## Build Process
### Downloading
To download NJOY21, simply `git clone` the repository. First move into the directory where you want the source code

```bash
git clone https://github.com/njoy/NJOY21.git
```
Similarly for NJOY2016

```bash
git clone https://github.com/njoy/NJOY2016.git
```
    
### Configuring
The configuration and build is performed in a directory (`bin`) inside the source directory

```bash
cd NJOY21
mkdir bin
cd bin
cmake ../
```

Note this will require a connection to the internet as `cmake` command will download (`clone`) the necessary dependencies. These will be placed in the `dependencies` directory.

### Compiling/Building

```bash
make
```
You can provide the command-line option `-j n` (where `n` is the number of concurrent/parallel "jobs") to speed up the compilation step.

### Testing

```bash
make test
```
Like for the compiling step, you can pass the `-j` command-line option here as well.

If all the tests pass, you should see something that looks like:

```
100% tests passed, 0 tests failed out of 90
```

### C++14 Compliant Compiler
We have tested NJOY2016 and NJOY21 with the following compilers

  - **Mac:**

    - apple clang 7.1+ (OS X 10.10, XCode 7.2.1 or higher)

  - **Linux:**

    - [gcc 6.2](https://gcc.gnu.org) 

  - **Windows:**

    - [clang 3.7](http://llvm.org)
    - [gcc 6.2](https://gcc.gnu.org) 

    Note that in Windows we currently currently test and support NJOY2016 and NJOY21 only under the Cygwin environment.

### Fortran 2003 Compliant Compiler

 - **Linux:**

   - [gfortran](https://gcc.gnu.org/fortran/) This is included as part of the standard [gcc](https://gcc.gnu.org) suite of compilers

