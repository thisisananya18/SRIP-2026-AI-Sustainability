# SRIP-2026-AI-Sustainability
SRIP 2026 AI-based audit of Delhi land use patterns

This repository contains my submission for the Land Cover Classification assignment under SRIP 2026 under project ID IP0NB0000021.
The assignment focuses on building a complete AI pipeline to analyze land-use patterns in the Delhi-NCR region using satellite imagery and ESA WorldCover data

**#Q1. Spatial Reasoning & Data Filtering**
Plotted the Delhi-NCR shapefile
Created a 60×60 km uniform grid (CRS: EPSG:32644)
Filtered Sentinel-2 RGB image patches based on center coordinates inside the region
Reported image counts before and after filtering

**#Q2. Label Construction & Dataset Preparation**
Extracted 128×128 land-cover patches from ESA WorldCover 2021 raster "worldcover_bbox_delhi_ncr_2021.tif"
Assigned labels using dominant (mode) class
Mapped ESA classes to simplified categories of Cropland(40), Built-up(50), vegetation(10,20,30), Water(80) and Others.
Performed 60/40 train-test split
Visualized class distribution

**#Q3. Model Training & Supervised Evaluation**
Trained a CNN model for land-use classification
Evaluated using Accuracy and F1-score
Generated and interpreted confusion matrix
