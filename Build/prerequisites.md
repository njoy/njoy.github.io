---
layout: page
title: Obtaining and Installing NJOY - Prerequisites
permalink: /Build/prerequisites.md
---
* TOC
{:toc}

## Prerequisites
Development for NJOY uses the latest published language standards that are widely supported by compiler vendors, *at the start of development*. Therefore, the minimum language standards are
                                                                                 
 - C++14 or higher
 - Fortran 2003 or higher
 - [Python 3.4+](https://python.org/downloads/)

Additionally, we use [CMake](https://cmake.org/) to configure the build system and [git](https://git-scm.com) for version control.

 - [CMake 3.2+](https://cmake.org/download/) - Latest Release
 - [git 2.1+](https://git-scm.com/downloads/)

### On Linux
 - Use the package manager for your distribution to install the required packages.
   - Debian distros: `sudo apt install gcc`
   - Arch: `sudo pacman -Su gcc`
   - etc.
 - Ensure that the binaries are in your system path
   - `echo $PATH`
   - If not, add it using `export PATH=$PATH:/path/to/binary/directory`
 - Ensure that the packages have the right version
   - `[package-name] --version`
 - If all packages are installed correctly and meet the minimum requirements, you are ready to [build NJOY!](/Build/build.md)

### On Mac
Why are you using mac?  How does one even mac?  I think the word `brew` is involved?  Whatever.

### On Windows
Step 1 - Install [Linux](https://www.ubuntu.com/download/desktop).
Step 2 - ::sigh:: Fine.

When building on Windows, the compilers must be obtained separately. The following options are available:

#### MinGW-W64
 - Build in cmd using [MinGW-w64](http://mingw-w64.org/doku.php/download) (use *MingW-W64-builds*, **not** *Win-Builds*).  This will direct you to a sourceforge download page.
   - **Important: Add \[install directory\]\\mingw64\\bin to the system path**
   - Example: `set Path=%Path%;/path/to/bin/directory`
 - Install [Python3](https://python.org/downloads/)
 - Install [CMake](https://cmake.org/download/)
 - Install [Git](https://git-scm.com/downloads/)
 - Check versions
   - `git.exe --version` (minimum required: 2.1+)
   - `cmake.exe --version` (minimum required: 3.2+)
   - `python.exe --version` (minimum required: 3.4+)
   - `gcc.exe --version` (minimum required: 6.2+)
   - `gfortran.exe --version` (minimum required: 6.2+)
   - `g++.exe --version` (minimum required: 6.2+)
 - If all packages are installed correctly and meet the minimum requirements, you are ready to [build NJOY!](/Build/build.md)

#### Cygwin
[Cygwin](https://cygwin.com/install.html) is a unix-like environment for Windows, complete with a Bash shell.

 - During installation, be sure to install the required packages:
   - gcc-core - C compiler
   - gcc-g++ - C++ compiler
   - gcc-fortran - Fortran compiler
   - cmake - Build system
   - python3 - Python interpreter
   - git - version control system
 - Ensure the drop-down box in the top left (left of the search bar) is set to *Full*.
 - To install the packages, click on the word *Skip* until it shows a version number that meets the requirement.
 - Only the box under "*Bin?*" needs to be selected [x].
 - On the subsequent screen, ensure the box on the bottom is checked: `Select required packages(RECOMMENDED)`.
 - Installing the packages may require several minutes.
 - Once installed, the package version can be verified inside the Bash shell using:
   - `git --version` (minimum required: 2.1+)
   - `cmake --version` (minimum required: 3.2+)
   - `python --version` (minimum required: 3.4+)
   - `gcc --version` (minimum required: 6.2+)
   - `g++ --version` (minimum required: 6.2+)
   - `gfortran --version` (minimum required: 6.2+)
 - If all versions meet the minimum requirements, you are ready to [build NJOY!](/Build/build.md)

