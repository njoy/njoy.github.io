---
layout: page
title: Obtaining and Installing NJOY
permalink: /Build/index.html
---

Both [NJOY21](https://github.com/njoy) and [NJOY2016](https://github.com/njoy) use the same configuration and build process.

## Prerequisites
Development for NJOY uses the latest published language standards that are widely supported by compiler vendors, *at the start of development*. Therefore, the minimum language standards are

 - C++14 or higher
 - Fortran 2003 or higher
 - [Python 3.4+](https://python.org/)

Additionally, we use [CMake](https://cmake.org/) to configure the build system and [git](https://git-scm.com)

 - [CMake 3.2+](https://cmake.org/) 
 - [git 2.1+](https://git-scm.com)

### C++14 Complian Compiler
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

