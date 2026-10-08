# Powder & cake plot

A powder plot represents the intensity as a function of the q vector, defined as $q=\sqrt{q_{xy}^2+q_z^2}$. This allows for comparison with powder diffractograms obtained from other sources.

You can adjust the **number of data points** in the powder plot (which directly affects its resolution), then run the cell.

```python
# Modify only the number of data points you want in the powder plots, and run the cell
npt_powder_plot = 600

...

```

Running the cell will generate the powder plot in q-space as well as in 2$\theta$.

Additionally, `dat` files containing the corresponding data for further analysis will be generated.

![](images/powder-plot-q.png)

![](images/powder-plot-tth.png)

It is sometimes more interesting to focus only on a wedge for the integration, and not on the whole image. This integration is often called a "cake" or "sector" plot.

You can adjust the **number of data points**, the **azimuthal range**, the **maximal q range** on which you wish to integrate, and then run the cell.

The azimuth is defined so that it is 0° along $q_{OOP}$, and +90° along $q_{IP}$.

```python
# ==================== User Parameters ====================
# Modify only the parameters below:
npt_cake_plot = 600
user_azimuth_range = (70, 90)  # User convention: 0° = out-of-plane (q_oop), 90° = in-plane (q_ip)
q_radius = 10  # in nm^-1

# =========================================================
...

```

![](images/powder-plot-image-cake.png)

![](images/powder-plot-cake-q.png)
