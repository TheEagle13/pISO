pISO
====

[![Build Status](https://travis-ci.org/ALSchwalm/pISO.svg?branch=master)](https://travis-ci.org/ALSchwalm/pISO)
[![pipeline status](https://gitlab.com/ALSchwalm/pISO/badges/master/pipeline.svg)](https://gitlab.com/ALSchwalm/pISO/commits/master)

First, clone the project with `git clone --recursive https://github.com/TheEagle13/pISO.git`

Building with docker
--------------------

Just have make and docker installed and run:

    make sdimage

Building without docker
-----------------------

Without docker, you will need to first ensure you have all of the appropriate
dependencies installed (see [this list](https://buildroot.org/downloads/manual/manual.html#requirement) ).

    cd buildroot
    cp configs/piso_defconfig .config
    make

Either approach should produce a file in `buildroot/output/images/sdcard.img`. This file can
be written directly to an SD card (e.x., with `dd`).

License
-------

The pISO source code and hardware designs are licensed under the terms of the GNU General Public
License 3.0. For additional information see the LICENSE file.
