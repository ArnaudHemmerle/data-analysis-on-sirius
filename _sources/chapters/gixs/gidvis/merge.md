# Merge images to remove dead zones

The purpose of collecting diffraction patterns at two different detector angles is to merge the images and eliminate the horizontal dead zones that may obscure a peak.

## Steps to merge images

1. In the `Load File` window, select the files you want to merge. For this example, choose scans `5151` and `5152` (hold **Ctrl** to select multiple files).
2. Right-click on the selected files and choose `Merge Selected Images.

## Assign setups

In the new window that appears, assign the appropriate `Experimental Setup` to each file:
- **5151**: Set to `gamma -0.75`
- **5152**: Set to `gamma -1.4`

Ensure the other parameters are correctly filled in. If they were previously set, you can leave them as is.

![](images/merge-ready.png)

## Save the merged file

1. Click `Merge and Save`.
2. Name the merged file `5151_5152.GIDDat` and save it in the same folder as your raw data.

You can now select the merged file in the `Load File` window for further analysis.

![](images/merge-done.png)
