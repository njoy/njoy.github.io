---
layout: page
title: Obtaining and Installing NJOY - Quick
permalink: /Build/index.html
---
* TOC
{:toc}

Both [NJOY21](https://github.com/njoy/NJOY21) and [NJOY2016](https://github.com/njoy/NJOY2016) use the same configuration and build process. Additionally, all of the supporting [projects](/Projects.html) use the same process. 

Prerequisites for building (i.e. - compilers, build programs) are found [here](/Build/prerequisites.md).

Detailed instructions for building NJOY are available for [Windows, Mac, and Linux](/Build/build.md).

More detailed information on compatible compilers for Windows, Mac, and Linux are found [here](/Build/compilers.md).

Finally, some commonly encountered issues and their respective solutions can be found [here](/Build/faq.md).

#### Option A (git):
```bash
# Download the source code
git clone https://github.com/njoy/NJOY2016.git

# Configure the build process
cd NJOY2016
mkdir bin
cd bin
cmake ../

# Build NJOY16
make

# Test NJOY16
make test
```

#### Option B (Docker):
```bash
# Download the Dockerfile
wget https://github.com/njoy/NJOY2016/blob/docker/Dockerfile

# Build the Docker image
# (image installs dependencies and builds NJOY2016 as shown above)
docker build -t local:NJOY2016 .

# Run the image in interactive mode
docker run -ti local:NJOY2016

# Test NJOY21
$docker~ cd NJOY2016/build
$docker~ make test
```
