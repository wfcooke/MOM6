NOAA-GFDL MOM6
==============

The Modular Ocean Model, MOM6.

This branch (gh-pages) is used for storing the source code documentation which can be viewed at http://commercegov.github.io/NOAA-GFDL-MOM6/.

The generated API documentation can be viewed http://commercegov.github.io/NOAA-GFDL-MOM6/APIs.

Updating the generated API documentation
========================================

The workflow for re-generating the API documentation with doxygen (http://www.doxygen.org/) is:

    git checkout dev/master
    git clone https://github.com/doxygen/doxygen
    (cd doxygen/; ./configure)
    (cd doxygen/; make -j 4)
    ./doxygen/bin/doxygen .doxygen
    ./doxygen/bin/doxygen .doxygen
    mv APIs tmp
    git checkout gh-pages
    rm -rf APIs
    mv tmp APIs
    git add APIs
