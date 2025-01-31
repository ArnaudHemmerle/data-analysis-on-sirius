# Analyzing GIWAXS with pyFAI

## What is pyFAI?

PyFAI is a Python library for the azimuthal integration of X-ray scattering data acquired with area detectors. It is particularly useful for analyzing grazing incidence diffraction images. The official documentation is available [here](https://www.silx.org/doc/pyFAI/latest/index.html#).

## Why use pyFAI?

PyFAI is a scientific library built around IPython and NumPy, designed for data analysis either interactively—such as in Jupyter Notebooks—or via scripts. Unlike GUI-based software, it offers significant advantages when processing hundreds of files or implementing custom analyses.

This tutorial aims to help SIRIUS users efficiently use pyFAI to convert detector images into reciprocal space and perform integration. It is based on {download}`this <../../../_static/giwaxs/pyfai/giwaxs_analysis_pyfai.ipynb>` Jupyter notebook, that you should download first (right-click, then `Save the link as`).

## Prerequisites
To follow this tutorial, you should have:
- a working Jupyter environment, and the notebook `giwaxs_analysis_pyfai.ipynb`,
- basic knowledge of Python programming,
- the ability to install required packages.

## Please cite pyFAI!

The SIRIUS beamline is not involved in the development of pyFAI; we are simply users, just like you. However, it is clear that a significant amount of time and effort has gone into creating this powerful tool. If you use pyFAI to analyze your data, please cite the following paper {cite:p}`ashiotis2015.
