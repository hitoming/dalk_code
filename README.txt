The code used in the following study:
“Observation of nearshore Icebergs in front of Dalk Glacier by UAV: dome correction and size distribution and area/volume relationship.”

This repository contains MATLAB scripts for processing and analyzing remote sensing data, particularly in relation to Digital Elevation Models (DEM) and land cover classification. The project is divided into three main modules:

Dome Effect Processing (dome/)

Land Cover Classification (classification/)

Iceberg Area-Volume Analysis (area_volume/)

Folder Structure and Code Descriptions

1. Dome Effect Processing (dome/)

This module focuses on fitting a Dome Effect in DEM data. The workflow includes:

Data processing

Surface fitting

Residual analysis

Output of results

2. Land Cover Classification (classification/)

This module provides MATLAB scripts for land cover classification using superpixel segmentation and machine learning.

Main Scripts:

main1.m: Superpixel segmentation and feature extraction

Uses DOM, DEM, and roi.shp (polygon data with land cover labels 1-6)

Performs superpixel segmentation to reduce computational complexity

Visualizes the boundaries of segmentation results

main2.m: Feature selection and Random Forest classification

Selects and normalizes key features from RGB and DEM data

Trains a Random Forest model for classification

Predicts land cover classes and maps them back to the segmentation results

Saves classification results

3. Iceberg Area-Volume Analysis (area_volume/)

This module examines the relationship between iceberg area and volume using log-log coordinate transformations.

Compares UAV measurements with model data

Uses two datasets: UAV-Dalk data and model data

Applies logarithmic transformation and linear regression

Computes slope (b), intercept (log(a)), R², and RMSE

Calculates a 95% confidence interval

Visualizes the results:

Blue: UAV data

Red: Model data

Requirements

MATLAB

Required toolboxes for image processing and machine learning

Data files: DOM, DEM, roi.shp, UAV-Dalk data, and model data

Usage

Clone the repository:

git clone https://github.com/your-repo-name.git

Open MATLAB and navigate to the cloned directory.

Run the respective script based on your analysis needs:

dome/: Run scripts to process Dome Effect in DEM data

classification/: Use main1.m for segmentation, then main2.m for classification

area_volume/: Run scripts to analyze iceberg area-volume relationships

License

This project is open-source under the MIT License.

Contact

For any questions or collaboration inquiries, please contact  nongmy@mail2.sysu.edu.cn .