---
layout: page
title: Modern NJOY Components
---

## Overview

By moving away from the module structure of NJOY2016 to a component-based toolkit for a modern NJOY, we can allow for faster deployment of tools and integration in other tools. Providing both a C++ and Python interface at the same time will also help in deploying these tools more quickly. Once all necessary components are developed in this way, creating a modern equivalent of any legacy NJOY module will be relatively trivial to achieve (from a pure coding point of view, excluding the required V&V efforts). Prototypes can even be developed in Python before considering their implementation in C++.

For these components, we can distinguish two types: format components and processing components. A format component obviously provides an interface to read, write and manipulate data in a given format (for example ENDF, GNDS or ACE) while processing components provide a specific processing operation (such as resonance reconstruction). Formatting components will never provide processing operations since most processing operations are essentially format agnostic (for example: we can linearise a cross section whether it comes from ENDF or GNDS).

In what follows we will give an overview of our available modern NJOY components.

## Formatting components

[ENDFtk](https://github.com/njoy/ENDFtk) is our toolkit for reading and interacting with ENDF-6 formatted files. This toolkit provides a full C++ library along with python bindings.

[ACEtk](https://github.com/njoy/ACEtk) is our toolkit for reading and interacting with ACE formatted files (the main nuclear data format used by MCNP). This toolkit provides a full C++ library along with python bindings.
