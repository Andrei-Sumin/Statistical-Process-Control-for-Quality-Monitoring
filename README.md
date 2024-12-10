<div align="center">
  <img src="Figs/Logo.png" alt="Logo" width="700">
</div>

# Statistical Process Control for Quality Monitoring

## Project Overview

This project is part of the **Quality Data Analysis** course at Politecnico di Milano. The primary objective is to design and evaluate statistical methods for detecting defects in 3D-printed Voronoi filters. The study focuses on real-time quality control through in-situ image analysis during a simulated production process.


## Data Acquisition

The dataset was collected using a mock **Flexible Manufacturing System (FMS)** setup at the MADE Competence Center I4.0 laboratory. The system consisted of trays carrying parts along a rail. When positioned under a centrally located camera, the system captured an image of the tray. The setup is depicted in the figure below:

<div align="center">
    <img src="Figs/Fig_FMS.png" alt="Flexible Manufacturing System Setup" width="600">
</div>

Each tray contains four parts, positioned in the four corners. The images captured represent defect-free parts, as shown below:

<div align="center">
    <img src="Figs/Fig_phase1ex.png" alt="Defect-Free Parts Example" width="600">
</div>

In the second phase, images of parts with defects were introduced into the dataset. An example of such defects is highlighted below:

<div align="center">
    <img src="Figs/Fig_phase2ex.png" alt="Parts with Defects" width="600">
</div>



## Objectives

1. Implement **Statistical Process Control (SPC)** charts to monitor quality and identify anomalies in real-time.
2. Validate the performance of the SPC charts using a manually acquired list of actual faulty parts.



## Methodology

### Phase 1: Establishing Baseline Control
- Data from defect-free parts was used to develop SPC techniques.
- Key variables such as area, perimeter, and number of voids were analyzed.
- **Principal Component Analysis (PCA)** was applied to reduce noise and highlight patterns in the data.

### Phase 2: Fault Detection
- Control charts developed in Phase 1 were applied to a dataset with faulty parts.
- Faulty parts were identified based on control limits derived from the SPC charts.



## Statistical Analysis

The analysis utilized the following techniques:
- **Hotelling's T² control chart** for multivariate analysis.
- **Individual-Moving Range (I-MR)** charts for monitoring key variables and PCA scores.
- **Seasonal ARIMA modeling** to address observed periodicity in specific variables.



## Results and Conclusions

- Control charts successfully identified faulty parts in the Phase 2 dataset.
- PCA and Hotelling's T² control charts provided robust fault detection capabilities, outperforming traditional univariate methods.
- The methodology established a reliable framework for real-time quality monitoring in 3D printing applications.

---

## File Structure

root/ ├── Image_analysis_function.py # Function to transform images into CSV datasets. ├── qda.py # Useful SPC-related functions provided by the department. ├── CSV.ipynb # Main analysis file in Jupyter Notebook format. ├── Figs/ # Folder containing figures for the analysis report and README. │ ├── Fig_FMS.png │ ├── Fig_phase1ex.png │ ├── Fig_phase2ex.png ├── dataset_phase1/ # Phase 1 data: initial images, processed results, and CSV file. │ ├── initial_images/ │ ├── Result/ │ └── image_statistics.csv ├── dataset_phase2/ # Phase 2 data: initial images, processed results, and CSV file. │ ├── initial_images/ │ ├── Result/ │ └── image_statistics_phase2.csv


## Acknowledgments

Special thanks to the **MADE Competence Center I4.0** laboratory and the Department of Mechanical Engineering for their support and for providing essential tools and data.
