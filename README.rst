Introduction
============
aimsgb is an efficient and open-source Python library for generating atomic coordinates in periodic grain boundary models. It is designed to
construct various grain boundary structures from cubic and non-cubic initial
configurations. A convenient command line tool has also been provided to enable
easy and fast construction of tilt and twist boundaries by assigining the degree
of fit (Σ), rotation axis, grain boundary plane and initial crystal structure.

We also provide a web-based GUI to access aimsgb framework: `aimsgb.org
<https://aimsgb.org/>`_

Install aimsgb
==============
Method 1: Use Pip
-----------------
The easiest way to install aimsgb is to simply run a one-liner in pip::

   pip install aimsgb

Method 2: Use Git to install
----------------------------
1. Clone the latest version from github::

    git clone https://github.com/ksyang2013/aimsgb.git

2. Navigate to aimsgb folder::

    cd aimsgb

3. Type in the root of the repo::

    pip install .

4. or to install the package in development mode::

    pip install -e .


Usage
==================
Refer to the `documentation
<https://aimsgb-docs.readthedocs.io/en/latest/>`_ for more details.

How to cite aimsgb
==================

If you use aimsgb in your research, please consider citing the following work:

    Jianli Cheng, Jian Luo, Kesong Yang. *Aimsgb: An algorithm and open-source python
    library to generate periodic grain boundary structures.* Computational Materials
    Science, 2018, 155, 92-103. `doi:10.1016/j.commatsci.2018.08.029
    <https://doi.org/10.1016/j.commatsci.2018.08.029>`_



