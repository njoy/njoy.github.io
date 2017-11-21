---
layout: page
title: Obtaining and Installing NJOY - Building
permalink: /Build/build.md
---
* TOC
{:toc}

## Building

### Downloading
To download NJOY2016, simply `git clone` the repository. First move into the directory where you want the source code

```bash
git clone https://github.com/njoy/NJOY2016.git
```
Similarly for NJOY21

```bash
git clone https://github.com/njoy/NJOY21.git
```
When behind an http proxy (ex. inside LANL network), you must first inform git what the proxy is
```bash
git config --global http.proxy http://institution.proxy:port
```

### Updating NJOY to Incorporate Changes
If you already have NJOY cloned then you can easily update to the latest version with a simple command:

```bash
git pull
```
This will "pull" all the changes that have been made to your local machine. You can continue to follow the instructions for configuring and building.

    
### Configuring
The configuration and build is performed in a directory (`bin`) inside the source directory

```bash
cd NJOY21
mkdir bin
cd bin
cmake ../
```

Note this will require a connection to the internet as `cmake` command will download (`clone`) the necessary dependencies using git. These will be placed in the `dependencies` directory.

Note, when using Windows, the final command must include the option `-G "MinGW Makefiles"` or `-G "Unix Makefiles"` when using MinGW or Cygwin, respectively.

### Compiling/Building

#### On Linux, Mac, or Windows with Cygwin
```bash
make
```
#### On Windows with MinGW
```bash
mingw32-make.exe
```
You can provide the command-line option `-j n` (where `n` is the number of concurrent/parallel "jobs") to speed up the compilation step.

### Testing

#### Linux, Mac, Windows with Cygwin
```bash
make test
```
#### Windows with MinGW
```bash
mingw32-make.exe test
```
Like for the compiling step, you can pass the `-j` command-line option here as well.

If all the tests pass, you should see something that looks like:

```
100% tests passed, 0 tests failed out of 90
```

### Building Offline
For this configuration/build process, a connection to the internet is required as subprojects are are downloaded from GitHub. There are many instances when one would need to build NJOY on a machine that is not connected to the internet. To do that, please use these steps:

```bash
# Download the source code
git clone https://github.com/njoy/NJOY21.git

# Configure the build process
cd NJOY21
./metaconfigure/fetch_subprojects.py
rm -rf subprojects/

#### Transfer the NJOY21 directory to machine that is not connected 

cd NJOY21
./metaconfigure/collect_subprojects.py
mkdir bin
cd bin
cmake -Dfetched_subprojects=TRUE ../

# Build NJOY21
make

# Test NJOY21
make test
```
