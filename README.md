Readme - work in progress

## Guides/assistance for Authentication-protected GeoMet datasets
#### Last updated 2022-07-06

This repository contains a collection of guides and tutorials for connecting to prediction products on the 
GeoMet platform (https://eccc-msc.github.io/open-data/msc-geomet/readme_en/) that are currently protected by
authentication. At present these products are available as Web Map Service (WMS) and Web Coverage Service (WCS)
layers.

The files in this root folder of the repository are primarily Jupyter Notebooks demonstrating the process to
access and display WMS and WCS prediction layers. Subfolders contain a series of tutorials demonstrating how
to load and display authentication-protected WMS layers with ArcGIS Pro, ArcMap and QGIS using the example of
the Deterministic Hydrological Prediction System (DHPS).

Known limitations:
* WCS layers are not accessible through GIS packages - the GeoMet implementation is not compatible with QGIS or
  either Esri product.
* Although WCS is gradually being replaced by OGC API - Coverages in GeoMet, the authentication component and
  consequently the prediction products are not yet available through that protocol.
* The 'hidden', authentication-protected layers cannot be listed through a programmed or user interface
  command; the user must request the specific layer by name. A list of available layers is included at the end
  of this file.



