# Getting started

## Raw data & link to the electronic notebook

In this tutorial, we use data acquired on a thin film of nonfullerene acceptors deposited on a silicon wafer, of interest for the field of organic photovoltaics. All the raw data required for this tutorial can be downloaded [here](../../../_static/giwaxs/raw_data.zip).

It consists of TIFF files that are the integrated images output from our 2D detector. To know the details of each file from your experiment, you need to refer to the electronic notebook. Below is a screenshot of the notebook corresponding to scan 5151:

![](images/getting-started-notebook.png)

You see several pieces of information that will be useful for the conversion to q-space:
- The full file name: `SIRIUS_2024_11_22_5151`
- The script that launched this scan: `series_giwaxs.ipy`. You need to look inside the script to determine the total integration time (here, 330 s).
- The starting and ending time of the scan.
- The value of the out-of-plane angle of the detector, `gamma`.
- The value of the in-plane angle of the detector, `delta`.
- The value of the incidence angle, `thetai`.
- A 2D image of the integrated image in an **approximate** q-map.

It is important to note that some approximations are made to display the image in reciprocal space (in particular, the missing wedge at small $q_{xy}$ values is not accounted for, see {cite:p}`werzer2024`). **The map cannot be used as such for peak extraction or publication purposes.**

Also, note the white lines on the image. These are the dead zones of the 2D detector, originating from the gaps between its 10 modules. We typically take two images at two out-of-plane angles to eliminate the horizontal dead zones after reconstruction.

Additional useful information will be required from the notebook, which we will address step by step in the following sections.

## Download the tutorial repository

Download the repository if it is not already done : [here](https://gitlab.synchrotron-soleil.fr/sirius-beamline/notebooks/tutorial_giwaxs_pyfai). We will start with the notebook named `giwaxs_analysis_pyfai.ipynb`. Open it in Jupyter, and check that you have all the right packages installed by running the first code cell. Install the missing packages.

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.colors import SymLogNorm
import matplotlib.patches as patches
import pyFAI as pyFAI
from PIL import Image
import fabio
import os

import pyFAI.detectors
from pyFAI.method_registry import IntegrationMethod
from pyFAI.units import get_unit_fiber
from pyFAI.multi_geometry import MultiGeometry

print("Using pyFAI version: ", pyFAI.version)
```

This tutorial was done using pyFAI version ```2025.1.0```.
