# Convert to q Space

Select the file `5151` from the file list. This file was acquired at an angle of ${\rm gamma} = -0.75$ degrees. Choose the correct `Beamtime` (e.g., `Tutorial.mat`) and the corresponding `Experimental Setup` (e.g., `gamma -0.75`).

## Configure the `Toolbox` window

1. In the `Toolbox` window, select the entry `q` in the `Space` frame.
2. Click the `Full` button to automatically rescale the x and y axes.
3. Change the `Intensity Scaling` to `Log`.

In the `Parameters` frame, enter the angle of incidence (referred to as $\rm thetai$ in the notebook) in the field labeled `omega`. For this file, input the value **$0.12$**.

You may notice thin black lines appearing on the image when switching to q space. To remove these lines without affecting the image quality, adjust the `Horizontal` parameter in the `Regridding` frame. A value of **1000** works well for this dataset. Your result should resemble the following:

![](images/convert-q-space-5151.png)

## Note on the correction factors

GIDVis provides various correction factors. If you wish to apply them, refer to the GIDVis manual and ensure you fully understand the physical meaning of each factor. Generally, if you are not comparing peak intensities but focusing solely on peak positions, these corrections are unnecessary.

## Change the experimental setup for each file

For file `5152`, acquired on the same sample but at an out-of-plane angle of ${\rm gamma} = -1.4$ degrees, you need to use the appropriate `Experimental Setup`.

1. In the `Load File` window, click on the scan `5152`.
2. Select the `Experimental Setup` named `gamma -1.4`.
3. In the `Toolbox` window, click `Full` to rescale the axes.

The processed result should look like this:

![](images/convert-q-space-5152.png)
