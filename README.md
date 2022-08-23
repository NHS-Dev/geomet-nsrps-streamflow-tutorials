Readme - work in progress

## Guides/assistance for Authentication-protected GeoMet datasets
#### Last updated 2022-08-23 by Natalie

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
* Although WCS is gradually being replaced by *OGC API - Coverages* in GeoMet, the authentication component and
  consequently the prediction products are not yet available through that protocol.
* The 'hidden', authentication-protected layers cannot be listed through a programmed or user interface
  command; the user must request the specific layer by name. A list of available layers will be included at the end
  of this file.
  
### List of available hidden layers

* DHPS_1km_CorrectedFlowDir
* DHPS_1km_DeepReservoirStorage_PT24H
* DHPS_1km_DrainageArea
* DHPS_1km_Evap-SpatialAvg12h_PT12H
* DHPS_1km_Precip-SpatialAvg12h_PT12H
* DHPS_1km_RiverChannelStorage_PT24H
* DHPS_1km_RiverDischarge
* DHPS_1km_TotalRunoff-Avg12h_PT12H
* DHPS_1km_WaterbodyID
* DHPS-Analysis_1km_RiverDischarge
* DHPS-Analysis_1km_DeepReservoirStorage
* DHPS-Analysis_1km_Evap-SpatialAvg12h
* DHPS-Analysis_1km_Precip-SpatialAvg12h
* DHPS-Analysis_1km_RiverChannelStorage
* DHPS-Analysis_1km_TotalRunoff-Avg12h
*
* EHPS_1km_CorrectedFlowDir
* EHPS_1km_DrainageArea
* EHPS_1km_WaterbodyID
* EHPS_1km_RiverDischarge_Mem01
* EHPS_1km_RiverDischarge_Mem..
* EHPS_1km_RiverDischarge_Mem21
* EHPS_1km_DeepReservoirStorage_PT24H_Mem01
* EHPS_1km_DeepReservoirStorage_PT24H_Mem..
* EHPS_1km_DeepReservoirStorage_PT24H_Mem21
* EHPS_1km_RiverChannelStorage_PT24H_Mem01
* EHPS_1km_RiverChannelStorage_PT24H_Mem..
* EHPS_1km_RiverChannelStorage_PT24H_Mem21
* EHPS_1km_Evap-SpatialAvg12h_PT12H_Mem01
* EHPS_1km_Evap-SpatialAvg12h_PT12H_Mem..
* EHPS_1km_Evap-SpatialAvg12h_PT12H_Mem21
* EHPS_1km_Precip-SpatialAvg12h_PT12H_Mem01
* EHPS_1km_Precip-SpatialAvg12h_PT12H_Mem..
* EHPS_1km_Precip-SpatialAvg12h_PT12H_Mem21
* EHPS_1km_TotalRunoff-Avg12h_PT12H_Mem01
* EHPS_1km_TotalRunoff-Avg12h_PT12H_Mem..
* EHPS_1km_TotalRunoff-Avg12h_PT12H_Mem21
* EHPS-Analysis_1km_RiverDischarge
* EHPS-Analysis_1km_DeepReservoirStorage
* EHPS-Analysis_1km_Evap-SpatialAvg12h
* EHPS-Analysis_1km_Precip-SpatialAvg12h
* EHPS-Analysis_1km_RiverChannelStorage
* EHPS-Analysis_1km_TotalRunoff-Avg12h
*
* WCPS-Rivers_1km_CorrectedFlowDir
* WCPS-Rivers_1km_DeepReservoirStorage_PT24H
* WCPS-Rivers_1km_DrainageArea
* WCPS-Rivers_1km_Evap-SpatialAvg12h_PT12H
* WCPS-Rivers_1km_Precip-SpatialAvg12h_PT12H
* WCPS-Rivers_1km_RiverChannelStorage_PT24H
* WCPS-Rivers_1km_RiverDischarge
* WCPS-Rivers_1km_TotalRunoff-Avg12h_PT12H
* WCPS-Rivers_1km_WaterbodyID
* WCPS-Rivers-Analysis_1km_RiverDischarge
* WCPS-Rivers-Analysis_1km_DeepReservoirStorage
* WCPS-Rivers-Analysis_1km_Evap-SpatialAvg12h
* WCPS-Rivers-Analysis_1km_Precip-SpatialAvg12h
* WCPS-Rivers-Analysis_1km_RiverChannelStorage



