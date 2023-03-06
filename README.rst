*********
CFU Count
*********

CFU Count is a program for inferring the density of cells growing in a culture 
from the number of colonies observed in each spot of a serial dilution.  This 
is useful for knowing:

- How many cells were transformed, e.g. after a library-scale electroporation
- How OD600 values correspond to cell densities.  Note that it's good practice 
  to report cell densities instead of OD600 values, because OD600 values drift 
  over time and vary between different instruments.

This program takes a sophisticated statistical approach to calculating cell 
densities.  Briefly, it calculates the probability that the observed data could 
have been produced by every possible cell density, and then reports whichever 
density has the highest likelihood.  It also reports the standard deviation of 
this distribution.  This approach makes it possible to integrate the 
observations from multiple spots of a serial dilution (or from multiple 
independent dilutions).

.. image:: https://img.shields.io/pypi/v/cfu_count.svg
   :alt: Last release
   :target: https://pypi.python.org/pypi/cfu_count

.. image:: https://img.shields.io/pypi/pyversions/cfu_count.svg
   :alt: Python version
   :target: https://pypi.python.org/pypi/cfu_count

.. image:: 
   https://img.shields.io/github/actions/workflow/status/kalekundert/cfu_count/test.yml?branch=master
   :alt: Test status
   :target: https://github.com/kalekundert/cfu_count/actions

.. image:: https://img.shields.io/codecov/c/gh/kalekundert/cfu_count.svg
   :alt: Test coverage
   :target: https://app.codecov.io/gh/kalekundert/cfu_count

.. image:: https://img.shields.io/github/last-commit/kalekundert/cfu_count?logo=github
   :alt: Last commit
   :target: https://github.com/kalekundert/cfu_count

Installation
============
CFU Count is available from PyPI::

  $ pip install cfu_count

Version numbers follow `semantic versioning <https://semver.org/>`_.

Usage
=====
Use the ``-h`` flag to get detailed usage information::

  $ cfu-count -h

