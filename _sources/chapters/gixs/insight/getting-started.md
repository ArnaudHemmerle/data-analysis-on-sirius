# Getting started

## Raw data & link to the electronic notebook

In this tutorial, we use GIWAXS data acquired on a thin film of block copolymers deposited on a silicon wafer, and GISAXS data on nanostructured bi-metallic nanocluster {cite:p}`alvarez-fernandez2020`. All the raw data required for this tutorial can be downloaded [here](../../../_static/gixs/raw_data.zip). We will first focus on GIWAXS.

It consists of TIFF files that are the integrated images output from our 2D detector. To know the details of each file from your experiment, you need to refer to the electronic notebook. Below is a screenshot of the notebook corresponding to scan 429:

![](images/getting-started-notebook.png)
![](images/getting-started-notebook-image.png)

You see several pieces of information that will be useful for the conversion to q-space:
- The full file name: `SIRIUS_2025_10_25_0429`
- The script that launched this scan: `scan_giwaxs.ipy`. You need to look inside the script to determine the total integration time (here, 110 s).
- The starting and ending time of the scan.
- The value of the out-of-plane angle of the detector, `gamma`.
- The value of the in-plane angle of the detector, `delta`.
- The value of the incidence angle, `thetai`.
- A 2D image of the integrated image in an **approximate** q-map.

It is important to note that some approximations are made to display the image in reciprocal space (in particular, the missing wedge at small $q_{xy}$ values is not accounted for, see {cite:p}`werzer2024`). **The map cannot be used as such for peak extraction or publication purposes.**

Also, note the white lines on the image. These are the dead zones of the 2D detector, originating from the gaps between its 10 modules. We typically take two images at two out-of-plane angles to eliminate the horizontal dead zones after reconstruction.

Additional useful information will be required from the notebook, which we will address step by step in the following sections.

## Download the tutorial repository

Download the repository if it is not already done : [here](https://gitlab.synchrotron-soleil.fr/sirius-beamline/notebooks/tutorial_insight). We will start with the notebook named `giwaxs_analysis_insight.ipynb`. Open it in Jupyter, and check that you have all the right packages installed by running the first code cell. Install the missing packages.

```python
import insight_scatter as ins
import pandas as pd
import xraydb as xraydb
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.colors as colors
import matplotlib.cm as cmx
import itertools
import tifffile as tiff
import os
from typing import cast
```

This tutorial was done using insight version ```0.2.2```.
