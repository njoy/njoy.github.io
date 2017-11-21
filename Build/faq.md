---
layout: page
title: Obtaining and Installing NJOY - FAQ
permalink: /Build/faq.md
---
* TOC
{:toc}

## Potential Errors and Solutions

###Fortran compiler -- broken
When building on Windows with MinGW, you may get an error that includes `checking Fortran compiler -- broken`.  If this happens, ensure that the version of gfortran is correct using `gfortran.exe --version`.  If it is correct, check that you've added the directory in which gfortran.exe and mingw32-make.exe to the system Path.
***
### catch-adapter is not a subdirectory of ENDFtk

If, during the `cmake ..` step, you get an error that looks like:
```
ENDFtk/whatever
```
this can be fixed by regenerating the CMakeLists.txt file.  This is done by, from the base directory of the git repository, calling 
```bash
./metaconfigure/generate.py cmake
```
Once this is done, remove the contents of the `build` directory and repeat the build steps.
