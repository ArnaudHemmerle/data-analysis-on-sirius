# Powder plot

You can easily get a powder plot, that is the intensity as a function as the q vector (with $q=\sqrt{q_{xy}^2+q_z^2}$), that can be then compared to powder diffractogramm obtained elsewhere.

Select the image, here the merged image of 5151 and 5152, and click on the icon `Line` (LineScan over whole image). This opens a new window `Powder Plot`. You can choose the binning of the plot by tunning the `number of x-axis data points`, for comparison between different plots leave it as it is. You can choose whether you want to get the value as a function of $q$ or $2\times\theta$ obtained with the wavelength of the x-ray emission line Cu Ka1, that is useful for comparison with powder diffractogramm. Select the data points with $q_z>0$ and $q_{xy}<0$, to avoid loosing resolution in $q_{xy}$, or peak splitting if the direct beam is not perfectly centered at $q_{xy}=0$.

![](images/powder-plot-config.png)

You can fit the peak positions using GIDVis tools, but it may be easier to export the data and use your own fitting software. Click on `File>Export Line Data...`, and then on `Export and Close`. The text file contains the powder plot as a two column file.

