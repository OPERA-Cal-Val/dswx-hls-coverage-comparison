# A Comparison of HLS and DSWx Coverage

HLS tiles are used to generate DSWx inputs. This repository compares the coverage of the two using CMR and some DAAC rasters.
DSWx only considers a subset of HLS inputs (those acquired by Landsat 8 and Sentinel-2 constellation, *not* Landsat 9).
HLS can overwrite tiles and this creates issue with DSWx availability.

Analyses:

1. Comparison of MGRS tiles of HLS and DSWx nodata areas (to understand coverage)
2. The update cadence of an HLS tiles (i.e. how frequently are tiles overwritten)

This is done using the previous week of data.