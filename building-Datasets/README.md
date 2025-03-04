# Assessing building damage after a seismic event

## Context
This work explores an unsupervised multitemporal change detection method using Sentinel-1 imagery to assess building damage after the 2023 seismic event in Turkey. A dataset of destroyed buildings was prepared and shared here, alongside with a set of non-destroyed buildings selected randomly, and their 20m buffer. A time series of the mean backscatter intensity from return signal within the footprint of each destroyed building is evaluated to assess the change of trend after event. Then, an omnibus test is used to assess changes across the time series: polarimetric SAR data are represented by complex variance-covariance matrices, whose homogeneity is evaluated through a factorization of multiple independent likelihood ratio tests in the time series. To determine where and when a change has occurred in our time series, we implemented a sequential omnibus tests algorithm assessing the overall differences between distributions at multiple times. We obtain temporal change maps that allow to represent the timeline of occurrences of change.

## Description
This repository hosts the materials and workflow prepared for the master’s thesis available here [Thesis_unsupervised_CD_SAR.pdf](https://github.com/Augustin-Ma/AssessingDamage/blob/c4b3684e43d7ef0a3073fcd298918a7df92f28cc/Thesis_unsupervised_CD_SAR.pdf). 

The process is developed on Google Earth Engine via Colaboratory Notebook, which online version is available here https://colab.research.google.com/drive/1f4f8smWhSSeURFhs04Qw5z7bDVZf5dJO?usp=sharing.

The outputs of our analysis are displayed via an interactive HQ Observable tool available here https://observablehq.com/@ulgeovisualization/damage-assessment-using-sar, offering insights into the strengths and limits of the approach at the building level accross various parameters. HQ Observable is a collaborative data visualization and analysis platform using JavaScript. It allows to share data inractively with dynamic visualizations and computational notebooks.


## Author
Augustin Martinet
