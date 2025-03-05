
we make use of an unsupervised multitemporal change detection method taking in account the statistical properties of speckled data and the multilooking process.  We prove the the omnibus likelihood ratio test statistic ability to apply to our case by comparing, with the theoretical chi-square distribution, the results of the omnibus tests for both our building footprint dataset (Destroyed and Non-Destroyed), as well as the whole AOIs for reference as urban area. We do so for both the 10 first images of our collection and the 3 last, which are one before and
two after the event, and for each single polarization channel (section 5.3.1). Then, a sequence of omnibus tests is used to determine where and when a change has occurred
in our time series (section 5.3.2). This produces temporal change maps of the most recent change, the first change, and the frequency of changes. We measure the disaster impact with
counts related to our building datasets to obtain metrics. At last, we will compare these outputs at the building level with their corresponding temporal signatures across various parameters.


we implemented the omnibus test to assess changes across the time series for the entire study area and within both Destroyed and Non-destroyed building footprints. Changes were effectively detected within the Destroyed footprints accross the event sequence. Subsequently, a sequential algorithm of omnibus tests is used to determine where and when a change has occurred. This produces temporal change maps of the interval of change, the most recent, the first, and the frequency.


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


## Outputs
- Image Collections imprints.
- Temporal Signatures: interactive chart displaying the mean intensity for each building footprint over time, with distinct polarization types and relative orbits.
- Z-scores results for temporal signatures.
- Histograms of values from omnibus tests: performed simultaneously for all pixels of both our building footprint datasets and the whole AOIs, simultaneously for entire sequences of images pre- and during event, compared with the theoretical chi-square distribution.
- Change maps for single polarization (not included in paper).
- Change maps for dual polarization.
- Number of buildings containing changes within their footprint.

N.B. Ancillary informations are displayed throughout the process to ensure results reliability.
