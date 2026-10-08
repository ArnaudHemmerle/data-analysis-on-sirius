# Batch analysis

If you have multiple scans to analyze, you can use the `batch_giwaxs_analysis_pyfai.ipynb` notebook. This notebook follows the same processing steps as the one used in the previous sections and requires the same input parameters.

However, there are some key differences:

## 1. Specifying the list of scans

You need to define the list of scans to be processed, using **pairs of scan numbers** corresponding to the two detector angles (`gamma_A` and `gamma_B`).

```python
# List of image pair scan numbers corresponding to (gamma_A, gamma_B)
scan_list = [
    (5151, 5152),
    (5153, 5154),
]
```

## 2. Performing azimuthal integration on multiple domains

You can specify multiple integration regions for different azimuthal scans. The integration domains should be listed in the following format:

```python
# ==================== AZIMUTHAL SLICE DOMAINS ====================
# List of integration domains (for multi-slice evaluation)
azimuthal_domain_list = [
    (3.7 - 0.2, 3.7 + 0.2, 45.0, 90.0),
    (5. - 0.2, 5. + 0.2, 0.0, 90.0),
]
```

## Running the batch processing
Once all the parameters are set, you can run the entire notebook. The processed data will be automatically exported into individual subfolders within the `processed_data/` directory.
