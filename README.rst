Introduction
============
aimsgb is an efficient and open-source Python library for generating atomic coordinates in periodic grain boundary models. It is designed to
construct various grain boundary structures from cubic and non-cubic initial
configurations. A convenient command line tool has also been provided to enable
easy and fast construction of tilt and twist boundaries by assigining the degree
of fit (Σ), rotation axis, grain boundary plane and initial crystal structure.


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

Changelog
=========

v1.1.2
------
Performance improvements to reduce computation time for complex/high-sigma grain boundaries:

- **get_smallest_multiplier** (``utils.py``): replaced the linear scan (1 … 10 000
  iterations) with a Fraction-based LCM computation. The smallest integer multiplier
  is now derived directly from the denominators of each vector element, making the
  cost independent of the multiplier's magnitude.

- **GBInformation.get_gb_info** (``grain_bound.py``): replaced the nested Python
  ``for m / for n`` double loop with a fully vectorised NumPy implementation.
  All (m, n) pairs are built with ``np.meshgrid``; sigma values, co-prime filtering
  (``np.gcd``), and rotation angles are computed in a single array pass.

- **Grain.make_supercell** (``grain.py``): replaced the per-site, per-coordinate
  double loop with vectorised NumPy operations. Fractional coordinates for all sites
  are processed simultaneously via array slicing.

How to cite aimsgb
==================

If you use aimsgb in your research, please consider citing the following work:

    Jianli Cheng, Jian Luo, Kesong Yang. *Aimsgb: An algorithm and open-source python
    library to generate periodic grain boundary structures.* Computational Materials
    Science, 2018, 155, 92-103. `doi:10.1016/j.commatsci.2018.08.029
    <https://doi.org/10.1016/j.commatsci.2018.08.029>`_



