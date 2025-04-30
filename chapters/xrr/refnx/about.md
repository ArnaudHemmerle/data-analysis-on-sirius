# Analyzing XRR with refnx

## What is refnx?

refnx is a Python library for curve fitting analysis, specifically neutron and X-ray reflectometry data. The official documentation is available [here](https://refnx.readthedocs.io/en/latest/).

## Why use refnx?

refnx is a scientific library using several scipy.optimize algorithms for data analysis either interactively—such as in Jupyter Notebooks—or via scripts. Unlike GUI-based software, it offers significant advantages when processing hundreds of files or implementing custom analyses.

This tutorial aims to help SIRIUS users efficiently use refnx to find an accurate model for fitting their XRR data. It is based on the notebooks available on [this](https://gitlab.synchrotron-soleil.fr/sirius-beamline/notebooks/tutorial_xrr_refnx) repository. You should first download the whole repository to follow the tutorial.

## Prerequisites
To follow this tutorial, you should have:
- a working Jupyter environment,
- the repository aforementioned,
- basic knowledge of Python programming,
- the ability to install required packages.

## Please cite refnx!

The SIRIUS beamline is not involved in the development of refnx; we are simply users, just like you. However, it is clear that a significant amount of time and effort has gone into creating this powerful tool. If you use refnx to analyze your data, please cite the following paper {cite:p}`nelson2019`.

