# NeurIPS-Ariel Data Challenge 2024

This repository contains the code and analysis for the NeurIPS Ariel Data Challenge 2024. The solution focuses on processing and calibrating spectroscopic data from the Ariel space telescope.

Link for competition is below:
https://www.kaggle.com/competitions/ariel-data-challenge-2024

## Overview

The core component of the solution is implemented in the Jupyter Notebook `NeurIPS-Ariel Data Challenge 2024 (1).ipynb`. This notebook performs the following key steps:

1.  **Data Preprocessing:** Handles loading and cleaning the raw data, including applying corrections for linear effects, dark current, and flat field.  It also performs binning and CDS (Correlated Double Sampling).
2.  **Phase Detection and Calibration:** Implements a method to detect phases in the signal and calibrates the signal using polynomial fitting to correct for signal distortions.
3.  **Submission Generation:** Generates the final submission file in the required format.

## Dependencies

The code relies on the following Python libraries:

* `pandas`
* `matplotlib.pyplot`
* `numpy`
* `seaborn`
* `scipy.stats`
* `scipy.optimize`
* `sklearn.model_selection`
* `sklearn.linear_model`
* `sklearn.metrics`
* `tqdm`
* `itertools`
* `functools`
* `random`
* `os`
* `astropy.stats`

## Data

The notebook assumes that the necessary data files are located in the following directory structure (as it is in Kaggle):

* `/kaggle/input/ariel-data-challenge-2024/`
    * `test_adc_info.csv`
    * `axis_info.parquet`
    * `test/`
        * `{planet_id}/`
            * `AIRS-CH0_signal.parquet`
            * `FGS1_signal.parquet`
            * `AIRS-CH0_calibration/`
                * `dark.parquet`
                * `dead.parquet`
                * `flat.parquet`
                * `linear_corr.parquet`
            * `FGS1_calibration/`
                * `dark.parquet`
                * `dead.parquet`
                * `flat.parquet`
                * `linear_corr.parquet`

You may need to adjust the file paths if you are running the notebook in a different environment.

## Usage

1.  **Environment Setup:** Ensure you have Python 3 and the required libraries installed.  It is recommended to use a virtual environment or a package manager like `conda` or `pip`.
2.  **Data Placement:** Download the challenge data and place it in the directory structure expected by the notebook.
3.  **Notebook Execution:** Run the `NeurIPS-Ariel Data Challenge 2024 (1).ipynb` notebook.  You can use Jupyter Notebook, JupyterLab, or VS Code with the Jupyter extension.
4.  **Submission:** The notebook will generate the `submission.csv` file, which you can then submit to the competition.

## Key Concepts

* **Signal Processing:** Techniques for cleaning and correcting the raw detector signals.
* **Calibration:** Methods to remove instrumental effects from the data.
* **Phase Detection:** Identifying specific points in the signal related to the observation.
* **Polynomial Fitting:** Using polynomial functions to model and correct for signal distortions.

## Disclaimer

This solution was developed for the NeurIPS Ariel Data Challenge 2024.  The specific techniques and parameters may need to be adapted for other datasets or applications.
