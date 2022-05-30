# MSC Geomet Example - Connecting to Authenticated Layers with ArcMap

This example shows how to connect ArcMap to the username/password authenticated Web Map Service (WMS) layers on the Meteorological Service of Canada (MSC) GeoMet platform.

## Connect to WMS
First, connect to the Geomet data source by selecting 'Add Data', then if necessary click 'Up One Level' until this level is shown. Double-click 'GIS Servers', then 'Add WMS Server'. We then need to supply a geomet path complete with hidden layer name, e.g. https://geo.weather.gc.ca/geomet?LAYERS=DHPS_1km_RiverDischarge and add User and Password credentials at the bottom. Click OK.

This will take you back to the file/folder dialog. Select the newly added 'MSC GeoMet' entry and drill down to the layer name ("DHPS - Streamflow discharge [m^3/s]" for this example) and click 'Add'.

Unfortunately the default styling applied to the DHPS image is biased towards very large streamflow, so the loaded image is mostly black. We'll need to apply a better style but fortunately there is one ready to use. Expand the MSC GeoMet entry in the 'Table of Contents', right-click on DHPS - Streamflow discharge [m^3/s] and open the layer properties. On the Styles tab, under 'Select layer style', there is a drop down list of available styles; select 'RiverDischarge' and ok. Now we have a much more useful range of colours.








![Connect to WMS data source](images/01_add_wms_data_source.PNG)
