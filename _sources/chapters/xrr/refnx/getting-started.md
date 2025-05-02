# Getting started

In this tutorial, we use first data acquired on a simple water-helium interface, and then on a Langmuir monolayer of a phospholipid deposited at the water-helium interface.

## Download the tutorial repository

Download the repository if it is not already done : [here](https://gitlab.synchrotron-soleil.fr/sirius-beamline/notebooks/tutorial_xrr_refnx). We will start with the notebook named `xrr_analysis_refnx.ipynb`. Open it in Jupyter, and check that you have all the right packages installed by running the first code cell. Install the missing packages.

```python
import numpy as np
import matplotlib.pyplot as plt
import refnx as refnx

from refnx.dataset import Data1D
from refnx.util import refplot
from refnx.reflect import SLD, Slab, ReflectModel
from refnx.analysis import Transform, CurveFitter, Objective, Model, Parameter

print("Using refnx version: ", refnx.version.version)
```

This tutorial was done using pyFAI version ```0.1.38```.
