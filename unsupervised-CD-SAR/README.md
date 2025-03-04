# Getting Started

From Colaboratory Notebook, access to a Google Earth Engine account with necessary permissions:

Update the project placeholder to ee.Initialize() line in first cell 
`ee.Initialize(project='ee-augustinmartinet')`

Replace `'ee-with your GEE project ID'` .

**Datasets** are to be downloaded and added in `'/content/'`.


# Inputs

1. **AOI and Footprint datasets** are provided in shapefiles format, to be added in `'/content/'`, and in Geojson format to allow autonomous run if necessary.

2. **Sentinel-1 Image Collection** are fetched directly from Google Earth Engine's image archive.


# Run

Computing time is of 3 min to obtain temporal change maps + 8 minutes to obtain metrics. 


# Outputs
- Image Collections imprints.
- Temporal Signatures: interactive chart displaying the mean intensity for each building footprint over time, with distinct polarization types and relative orbits.
- Z-scores results for temporal signatures.
- Histograms of values from omnibus tests: performed simultaneously for all pixels of both our building footprint datasets and the whole AOIs, simultaneously for entire sequences of images pre- and during event, compared with the theoretical chi-square distribution.
- Change maps for single polarization (not included in paper).
- Change maps for dual polarization.
- Number of buildings containing changes within their footprint.

N.B. Ancillary informations are displayed throughout the process to ensure results reliability.
