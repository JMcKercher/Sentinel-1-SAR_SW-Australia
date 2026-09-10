# Sentinel-1-SAR_SW-Australia
This Jupyter notebook, utilising Google Earth Engine, manipulates Sentinel 1 SAR imagery from the Copernicus data repository to generate seasonal S1 SAR indices from the entire Sentinel 1 mission for the south-west Western Australia region. 
This notebook will create Sentinel C-band Synthetic Aperture Radar (SAR) seasonal averages for the 4 seasons of the year over 9 years of available data. S1 SAR project data available within GEE is provided from 2014 onwards.
The idea is to calculate the seasonal average for each season of every year back to 2014 or the extent of data availability and then find the average of each season for the extent of the data period.
Less technically, an average of the each years season averages.

### Some details on the data and it's use
***Polarisation***: The process of confining the vibrations of the magnetic, or electric field, vector of light or other radiation to one plane.

The Google Earth Engine Collection contains all of the GRD scenes. Each scene has one of 3 resolutions (10, 25 or 40 meters), 4 band combinations (corresponding to scene polarization) and 3 instrument modes. Use of the collection in a mosaic context will likely require filtering down to a homogeneous set of bands and parameters. Each scene contains either 1 or 2 out of 4 possible polarization bands, depending on the instrument's polarization settings. The possible combinations are single band VV or HH, and dual band VV+VH and HH+HV:
1. VV: single co-polarization, **vertical transmit/vertical receive**
2. HH: single co-polarization, **horizontal transmit/horizontal receive**
3. VV + VH: dual-band cross-polarization, **vertical transmit/horizontal receive**
4. HH + HV: dual-band cross-polarization, **horizontal transmit/vertical receive**
5. The primary conflict-free modes are IW, with VV+VH polarisation over land, and WV, with VV polarisation, over open ocean. EW mode is primarily used for wide area coastal monitoring including ship traffic, oil spill and sea-ice monitoring. SM mode is only used for small islands and on request for extraordinary events such as emergency management. Having the Interferometric Wide swath mode as the one main operational mode satisfies most current service requirements, avoids conflicts and preserves revisit performance, simplifies mission planning, decreases operational costs and builds up a consistent long-term archive.
IW acquires data with a 250 km swath at 5 m by 20 m spatial resolution (single look). IW mode captures three sub-swaths using Terrain Observation with Progressive Scans SAR (TOPSAR). With the TOPSAR technique, in addition to steering the beam in range as in ScanSAR, the beam is also electronically steered from backward to forward in the azimuth direction for each burst, avoiding scalloping and resulting in homogeneous image quality throughout the swath

To learn more about the Sentinel 1 SAR data available in the Google Earth Engine Repository please see the following resources:
- https://sentinel.esa.int/web/sentinel/user-guides/sentinel-1-sar/acquisition-modes
- https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S1_GRD#colab-python
- https://sentinels.copernicus.eu/web/sentinel/user-guides/sentinel-1-sar/definitions
