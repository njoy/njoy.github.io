---
layout. page
title: Obtaining and Installing NJOY - Compilers
permalink: /Build/compilers.md
---
* TOC
{:toc}

## Compliant Compilers
We have tested NJOY2016 and NJOY21 with the following compilers. Note we don't support using the Intel compiler on any platform. It has some issues when using the Fortran and C++ compilers together.

### C++14 Compliant Compiler

  - **Mac:**

    - apple clang 7.1+ (OS X 10.10, XCode 7.2.1 or higher)

  - **Linux:**

    - [gcc 6.2](https://gcc.gnu.org) 

  - **Windows:**

    - [clang 3.7](http://llvm.org)
    - [gcc 6.2](https://gcc.gnu.org) 

    Note that in Windows we currently test and support NJOY2016 and NJOY21 only under the Cygwin environment.

### Fortran 2003 Compliant Compiler

 - **Linux:**

   - [gfortran](https://gcc.gnu.org/fortran/) This is included as part of the standard [gcc](https://gcc.gnu.org) suite of compilers.


 - **Mac:**

   - [gfortran](https://gcc.gnu.org/fortran/) A binary can be downloaded from [hpc.sourceforge.net](http://hpc.sourceforge.net). Alternatively, installing gcc 6.3 via [homebrew](https://brew.sh) works quite well. Note, the build for gcc 6.2 provided by homebrew does not work.

 - **Windows:**

   - [gfortran](https://gcc.gnu.org/fortran/) This is included as part of the standard [gcc](https://gcc.gnu.org) suite of compilers.
