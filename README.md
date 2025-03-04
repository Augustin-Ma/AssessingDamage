# Assessing building damage after a seismic event using unsupervised change detection with Sentinel-1 imagery

## Context
This work explores an unsupervised and multitemporal change detection method using Sentinel-1 imagery to assess building damage after the 2023 seismic event in Turkey. A dataset of destroyed buildings was prepared and shared here, alongside with a set of non-destroyed buildings selected randomly, and their 20m buffer. A time series of the mean backscatter intensity from return signal within the footprint of each destroyed building is evaluated to assess the change of trend after event. Then, an omnibus test is used to assess changes across the time series: polarimetric SAR data are represented by complex variance-covariance matrices, whose homogeneity is evaluated through a factorization of multiple independent likelihood ratio tests in the time series. To determine where and when a change has occurred in our time series, we implemented a sequential omnibus tests algorithm assessing the overall differences between distributions at multiple times. We obtain temporal change maps that allow to represent the timeline of occurrences of change.

## Description
This repository hosts the materials and workflow prepared for the master’s thesis available here [Thesis_unsupervised_CD_SAR.pdf](https://github.com/Augustin-Ma/AssessingDamage/blob/c4b3684e43d7ef0a3073fcd298918a7df92f28cc/Thesis_unsupervised_CD_SAR.pdf). 

The process is developed on Google Earth Engine via Colaboratory Notebook, which online version is available here https://colab.research.google.com/drive/1f4f8smWhSSeURFhs04Qw5z7bDVZf5dJO?usp=sharing.

The outputs of our analysis are displayed via an interactive HQ Observable tool available here https://observablehq.com/@ulgeovisualization/damage-assessment-using-sar, offering insights into the strengths and limits of the approach at the building level accross various parameters. HQ Observable is a collaborative data visualization and analysis platform using JavaScript. It allows to share data inractively with dynamic visualizations and computational notebooks.


## Getting Started

From Colaboratory Notebook, access to a Google Earth Engine account with necessary permissions:

Update the project placeholder to ee.Initialize() line in first cell 
`ee.Initialize(project='ee-augustinmartinet')`

Replace `'ee-with your GEE project ID'` .

**Datasets** are to be downloaded and added in `'/content/'`.


## Inputs

1. **AOI and Footprint datasets** are provided in shapefiles format, to be added in `'/content/'`, and in Geojson format to allow autonomous run if necessary.

2. **Sentinel-1 Image Collection** are fetched directly from Google Earth Engine's image archive.


## Run

Computing time is of 3 min to obtain temporal change maps + 8 minutes to obtain metrics. 


## Outputs
- Image Collections imprints.
- Temporal Signatures: interactive chart displaying the mean intensity for each building footprint over time, with distinct polarization types and relative orbits.
- Z-scores results for temporal signatures.
- Histograms of values from omnibus tests: performed simultaneously for all pixels of both our building footprint datasets and the whole AOIs, simultaneously for entire sequences of images pre- and during event, compared with the theoretical chi-square distribution.
- Change maps for single polarization (not included in paper).
- Change maps for dual polarization.
- Number of buildings containing changes within their footprint.

N.B. Ancillary informations are displayed throughout the process to ensure results reliability.


## Author
Augustin Martinet
