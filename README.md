NOAA-GFDL MOM6
==============

The Modular Ocean Model, MOM6.

This branch (gh-pages) is used for storing the source code documentation which can be viewed at http://commercegov.github.io/NOAA-GFDL-MOM6/.

Updating the generated API documentation
========================================

The workflow for re-generating the API documentation with doxygen (http://www.doxygen.org/) is:
    git checkout dev/master
    (cd tools; git clone https://github.com/doxygen/doxygen)
    ./tools/doxygen/bin/doxygen .doxygen
    ./tools/doxygen/bin/doxygen .doxygen
    mv APIs tmp
    git checkout gh-pages
    rm -rf APIs
    mv tmp APIs
    git add APIs
