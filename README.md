# The Wasatch Front Community Velocity Model (wfcvm)

<a href="https://github.com/sceccode/wfcvm.git"><img src="https://github.com/sceccode/wfcvm/wiki/images/wfcvm_logo.png"></a>

[![License](https://img.shields.io/badge/License-BSD_3--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)
![GitHub repo size](https://img.shields.io/github/repo-size/sceccode/wfcvm)
[![wfcvm-ci Actions Status](https://github.com/SCECcode/wfcvm/workflows/wfcvm-ci/badge.svg)](https://github.com/SCECcode/wfcvm/actions)
[![wfcvm-ucvm-ci Actions Status](https://github.com/SCECcode/wfcvm/workflows/wfcvm-ucvm-ci/badge.svg)](https://github.com/SCECcode/wfcvm/actions)

## Description

Wasatch Front Community Velocity Model. Currently,the model includes Cache, 
Weber/Davis, Salt Lake, and Utah basin.

## Table of Contents
1. [Software Documentation](https://github.com/SCECcode/wfcvm/wiki)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Contributing](#contributing)
5. [Credits](#credit)
6. [License](#license)

## Installation

This package is intended to be installed as part of the UCVM framework,
version 22.7.0 or higher. 

This package can also be build as a standalone program

<pre>
$ aclocal
$ autoconf
$ automake
$ ./configure --prefix=/path/to/install
$ make
$ make install
</pre>

## Usage

### UCVM

As part of [UCVM](https://github.com/SCECcode/ucvm) installation, use 'wfcvm' as the model.

### wfcvm_txt

ASCII query interface accepts points from stdin with format (lat, lon, dep (m)) and 
writes data material properties to std out with format (lat, lon, dep, 
vp, vs, density).

### wfcm_bin

Binary query interface reads a configuration file named 'cvm-input' with the following 
items:

<pre>
line 1: number of points
line 2: path to input lon file
line 3: path to input lat file
line 4: path to input dep file
line 5: path to output rho file
line 6: path to output vp file
line 7: path to output vs file
</pre>

The input and output files are in binary (float) format, with each
containing the number of points specified on line 1. 

## Support
Support for WFCVM is provided by the Southern California Earthquake Center
(SCEC) Research Computing Group.  Users can report issues and feature requests
using WFCVM's github-based issue tracking link below. Developers will also
respond to emails sent to the SCEC software contact listed below.
1. [WFCVM Github Issue Tracker](https://github.com/SCECcode/wfcvm/issues)
2. Email Contact: software@scec.usc.edu

## Credits
* Utah Geological Survey
* Harold Magistrale
* K.B. Olsen
* J.C. Pechmann

## Contributing
We welcome contributions to the WFCVM, please contact us at software@scec.usc.edu.

## License
This software is distributed under the BSD 3-Clause open-source license.
Please see the [LICENSE.txt](LICENSE.txt) file for more information.
