# Assessing building damage after a seismic event
# by unsupervised multitemporal change detection

The omnibus likelihood ratio test statistic offers several advantages: it is unsupervised, accounts for the statistical properties of speckled data, incorporates the multilooking process inherent to SAR imagery and allow to control the false positive rate.

A sequence of omnibus tests is used to determine where and when a change has occurred in our Sentinel-1 time series. We obtain temporal change maps that allow to represent the timeline of occurrences of change. We infer the cause of the change related to the disaster event using our building datasets to obtain metrics. At last, we compared these outputs at the building level with their corresponding temporal signatures across various parameters.

## Getting Started

The project uses Google Earth Engine Python API to process Sentinel-1 imagery. 
From Colaboratory Notebook, access to a Google Earth Engine account with necessary permissions:

Update the project placeholder to ee.Initialize() line in first cell 
`ee.Initialize(project='ee-augustinmartinet')`.

Replace `'ee-with your GEE project ID'` .

**Datasets** are to be downloaded and added in `'/content/'`.


## Inputs

1. **AOI and Footprint datasets** are provided in shapefiles format, to be added in `'/content/'`, and in Geojson format to allow autonomous run if necessary.

2. **Sentinel-1 Image Collection** are fetched directly from Google Earth Engine's image archive.


## Run

Computing time is of 3 min to obtain temporal change maps + 8 minutes to obtain metrics. 


## Outputs and Results
- Image Collections imprints.
 
  <img src="https://github.com/Augustin-Ma/AssessingDamage/blob/6394272c1c23fc889875d8391780b277cd5a4370/unsupervised-CD-SAR/fig/Imprints_Frames.jpg" alt="aois"  height="500">
  
- Temporal Signatures: interactive chart displaying the mean intensity for each building footprint over time, with distinct polarization types and relative orbits.

 <img src="https://github.com/Augustin-Ma/AssessingDamage/blob/a30e94f5ea5a27df352e0b2f33c59c811bdc49a5/unsupervised-CD-SAR/fig/signatures2.png" alt="signatures"  height="500">

- Z-scores results for temporal signatures.
- Histograms of values from omnibus tests: performed simultaneously for all pixels of both our building footprint datasets and the whole AOIs, simultaneously for entire sequences of images pre- and during event, compared with the theoretical chi-square distribution.
- Change maps for single polarization (not included in paper).
- Change maps for dual polarization.
- Number of buildings containing changes within their footprint.

N.B. Ancillary informations are displayed throughout the process to ensure results reliability.
