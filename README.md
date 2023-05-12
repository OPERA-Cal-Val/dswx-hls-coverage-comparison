# A Comparison of HLS and DSWx Coverage

HLS tiles are used to generate DSWx inputs. This repository compares the coverage of the two collections using Common Metadata Repository (CMR) and gdal tags in the actual product.
DSWx only considers a subset of HLS inputs (those acquired by Landsat 8 and Sentinel-2 constellation, *not* Landsat 9).
HLS can overwrite tiles and this creates issue with DSWx coverage relative to the apparent input HLS dataset (an overwritten dataset often adds coverage).

Analyses:

1. Comparison of MGRS tiles of HLS and DSWx tag labeled "spatial_coverage"
2. Inspection of the input SAFE files recorded in DSWx and HLS from sentinel-2 derived HLT tiles
3. Missing DSWx tiles depending on availability of HLS tiles in CMR

These analysis are restricted using the previous week of available data.

# Notebooks

The `A*` take all available DSWx data in the previous week, link HLS and perform the anlaysis 1 - 2. The notebooks `B*` take all the available HLS ids in the previous week, and use regex to find the associated DSWx product in CMR to capture the analysis associated to 3.

Note:

It is imperative to read the data effectively that the gdal configuration variables are correctly set depending on whether LP DAAC or PO DAAC is being used. Currently, this is done very haphazardly.