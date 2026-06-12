# Analyzing GIXS with INSIGHT

## What is INSIGHT?

INSIGHT is a Python library for processing and reducing 2D grazing-incidence wide-and small-angle X-ray scattering (GIWAXS/GISAXS) data. The official webpage is [here](https://www.ph.nat.tum.de/en/functmat/forschung-research/insight/).

## Why use INSIGHT?

INSIGHT is a script-based and object-oriented Python package containing several modules and classes. It provides a
comprehensive workflow customized for GISAXS/GIWAXS
data reduction that accompanies the scientist from visualizing
raw data to the final plotting or exporting of the reduced data.

This tutorial aims to help SIRIUS users efficiently use INSIGHT to convert detector images into reciprocal space and perform integration. It is based on the notebooks available on [this](https://gitlab.synchrotron-soleil.fr/sirius-beamline/notebooks/tutorial_insight) repository. You should first download the whole repository to follow the tutorial.

## Prerequisites
To follow this tutorial, you should have:
- a working Jupyter environment,
- the repository aforementioned,
- basic knowledge of Python programming,
- the ability to install required packages.

## Please cite INSIGHT!

The SIRIUS beamline is not involved in the development of INSIGHT; we are simply users, just like you. However, it is clear that a significant amount of time and effort has gone into creating this powerful tool. If you use INSIGHT to analyze your data, please cite the following paper {cite:p}`reus2024`.
