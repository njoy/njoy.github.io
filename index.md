---
layout: home
title: NJOY—Nuclear Data Processing Code
---

This is the home page for NJOY, the nuclear data processing code developed at [Los Alamos National Laboratory](http://www.lanl.gov).

Two versions of NJOY are currently managed and distributed:
 - [NJOY2016](https://njoy.github.io/NJOY2016) The main NJOY workhorse version, still maintained in Fortran.
 - [NJOY21](https://njoy.github.io/NJOY21) A C++ version wrapping regular NJOY2016 along with an input parser.

While it was initially intended to modernise NJOY on a module-by-module basis within NJOY21, the modernisation of NJOY has now gone in the direction of a component-based modernisation. As a result, NJOY21 will continue to use NJOY2016 for the foreseeable future.

## NJOY modernisation
The monolithic structure of NJOY is most useful when processing full evaluations into application libraries. However, for some fringe applications and a lot of day-to-day work where nuclear data users have specific questions (e.g., what is the cross section value at this energy), the monolithic structure of NJOY does not allow a user to get to that answer quickly or efficiently. In addition, some of the intermediate results produced during processing are not available to a user. An example here would be to obtain the elements of the R-matrix or T-matrix during resonance reconstruction.

Developing or redeveloping a module requires first developing the underlying components that do the work (which may include a component to handle file formats) before these components can be integrated into the final module. As indicated above, some or all of these components can be useful to end users as well as the final monolithic modules. As such, by focusing on deploying these components sooner rather than later, we can more quickly respond to user demands.

By moving away from the module structure of legacy NJOY to a component-based toolkit for a modern NJOY, we can allow for faster deployment of tools and integration in other tools. Providing both a C++ and Python interface at the same time will also help in deploying these tools more quickly. Once all necessary components are developed in this way, creating a modern equivalent of any legacy NJOY module will be relatively trivial to achieve (from a pure coding point of view, excluding the required V&V efforts). Prototypes can even be developed in Python before considering their implementation in C++.

Examples of these components that are now available to users are our [ENDFtk](https://github.com/njoy/ENDFtk) and [ACEtk](https://github.com/njoy/ACEtk) format components. Future components will include resonance reconstruction and data interpretation and manipulation tools.

## Open Source Availability
NJOY2016, NJOY21 and our modern NJOY components are freely available under the BSD 3-clause license. Both NJOY versions and any modern NJOY components are **free to use**, but the copyright and license must remain with the code.

### Getting NJOY
Instructions for obtaining, compiling, and testing NJOY can be found [here](https://docs.njoy21.io/install.html). Installation instructions for the modern NJOY components can be found on their respective repository on GitHub.

## Support or Contact
Technical support for both versions of NJOY can be obtained with an email to: [njoy@lanl.gov](mailto:njoy@lanl.gov).
