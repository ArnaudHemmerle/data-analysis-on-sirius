# Beam parameters

In this section, we'll review the various parameters that need to be configured to work in q-space. **To adapt the notebook to your own experiment, we assume that you've collected all the necessary information from your beamline scientist (wavelength, PONI, sample-detector distance, etc.). However, you can also find these details in the PDF electronic notebook.**

The first cell contains all the beamline parameters. Run it.

```python
# Modify with the beam parameters

# Geometry convention:
# PONIx / PONIy : direct beam position in detector pixels
# delta         : detector in-plane rotation angle (deg)
# gamma         : detector out-of-plane angle (deg)
# incidence_angle: grazing-incidence angle (deg)

wavelength = 1.24 # Angstrom
sample_detector_distance = 292 # mm
PONIx = 564 # pixel
PONIy = 1018 # pixel
delta = -10.56 # deg
incidence_angle = 0.12 # deg
pixel_size = 0.172 # mm
detector_dimensions = (1043,981) # pixels

# Out-of-plane angle for each image
gamma_A = -0.75 # deg
gamma_B = -1.4 # deg

# Modify with the path to your images
# img_A measured at gamma_A
path_A = "raw_data/SIRIUS_2025_10_25_0429_pilatus_sum.tiff"
# img_B measured at gamma_B
path_B = "raw_data/SIRIUS_2025_10_25_0430_pilatus_sum.tiff"
```

Additional information on specific parameters:
- **PONIx/PONIy**: The position of the direct beam on the detector, sometimes called PONIx and PONIy (Point Of Normal Incidence). Check the info relevant to your own experiment in the PDF electronic notebook.
- **delta**: In-plane angle of the detector, in degrees.
- **incident_angle**: The incident angle on the sample, in degrees. It is written in the PDF notebook as ```thetai```.
- **gamma_A/gamma_B**: The two out-of-plane angles of the detector, in degrees, corresponding here to scans ```429``` at $\gamma=-0.75$ and ```430``` at $\gamma=-1.4$.

All this information can be found in the PDF electronic notebook.

## Special case of a single GIWAXS image
This tutorial is based on a GIWAXS measurement with two detector positions, which helps eliminate the horizontal dead zones of the detector. If your experiment includes **only one GIWAXS image per sample**, you can duplicate the same values for `gamma_A` and `gamma_B`, and use the same image for both `path_A` and `path_B`.

