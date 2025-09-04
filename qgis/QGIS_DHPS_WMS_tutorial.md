# MSC Geomet Example - Connecting to Authenticated WMS with QGIS (tested on V3.16.7)

This example shows how to connect QGIS to the username/password authenticated Web Map Service (WMS) layers on the Meteorological Service of Canada (MSC) GeoMet platform.

## Connect to WMS
First, connect to the Geomet data source by selecting "Layer -> Data Source Manager" and select WMS/WMTS from the sidebar.

![Connect to WMS data source](images/01_add_wms_data_source.PNG)

Unlike the non-authenticated Geomet layers, all authenticated layers are hidden such that they can't be discovered from the tree available through a connection to the top level of GeoMet. Rather, each layer needs to be added individually as a separate WMS connection. To do this, under "Layers" select "New".

![Add WMS data source](images/02_add_wms_data_source.PNG)

Then, to view, for example, the 1km river discharge output from the Deterministic Hydrologic Prediction System (DHPS), enter a name of your choosing for the connection (e.g., "DHPS_1km_RiverDischarge") then enter the URL to the WMS layer, complete with the "LAYERS" parameter and name of layer you wish to connect to. For the DHPS River Discharge example:

https://geo.weather.gc.ca/geomet?LAYERS=DHPS_1km_RiverDischarge

![Enter connection info](images/03_connect_create_connection.PNG)

Then under "Authentication", choose the "Basic" tab and add your username and password to authenticate. If you wish, click "Convert to configuration" to save these credentials to a re-usable authentication configuration that is stored in an encrypted database, and can be selected from the Configurations tab for future connections. QGIS may request a new or existing password for the authentication database at this point. You also probably want to rename the converted configuration by selection from the drop-down and clicking the pencil button.

![Add authentication info](images/04_connect_add_authentication.PNG)

Select "OK" and then in Data Source Manager ensure the new layer is selected and hit "Connect".

## Add Layers to Map

You can now use the browser window to drill down in the newly added data source and add the individual layer to the project.

![Add layer](images/05a_add_layer_default_style.PNG)

![Add layer](images/05b_default_dhps_layer.png)

This opens up the default style DHPS and shows us the extent of the layer. However, this may not be the style wanted. The DHPS river discharge WMS layer includes multiple styles to address wide variations in flow magnitude across Canada.

To view additional styles, you can add each style as a separate layer. Select "Layer -> Add Layer -> Add WMS/WMTS Layer...".

![Add layer from data source](images/06_add_layer_from_data_source.PNG)

In the Data Source Manager dialog box, select the data source of interest from the drop down list at the top and click "Connect". Drill down in the data source you added previously until you see several style options. These have different legends to display different flow magnitudes more effectively, ranging (for the DHPS discharge example) from smaller rivers "RiverDischarge_S" to very large rivers "RiverDischarge_XL".

![Select layer with style](images/07_add_wms_layer_with_style.PNG)

Choosing "RiverDischarge" is the default style that is already open. To support the "Identify Features" function in this tutorial, let's set "Maximum Number of GetFeatureInfo Results" to 1. Click "Add".

![River discharge true default](images/08_river_discharge_true_default.PNG)

Zoom in to see a better example of the river discharge output from DHPS.

![River discharge true default zoomed on Ontario and Quebec](images/09_river_discharge_true_default_ONQC.PNG)

## View Data

Finally, while the WMS is suited more for raster imagery, you can also view the underlying values by selecting a grid cell using "Identify Features". Select it in from the "View" menu, or from the Attributes toolbar, highlighted below.

![Identify features to view data](images/10_identify_features.PNG)

Then zoom in to carefully click on a grid cell. The results will show in the "Idenfify Features" side bar or pop-up box. If the box shows multiple entries, this is due to the "Feature limit for GetFeatureInfo" setting mentioned earlier, but can be worked around by zooming close enough that the user can click near the centre of a cell.

Here's Ottawa River at Brittania, as an example.

![Selecting grid cell to view data](images/11_identify_features_select.PNG)

## View 'Time-enabled' Data

Many datasets available on the GeoMet platform include data for a range of times. In the case of DHPS, a 12-hour assimilation cycle is followed by a 6-day forecast. When DHPS is loaded into a GIS package, it is possible to step or animate through the forecast period. To view the time range for DHPS, first activate the Temporal Controller Panel:

![Select Temporal Controller Panel from toolbar](images/12_QGIS_Time_1.png)

This will open the control panel for time-enabled layers with time navigation disabled. Click the button with a small green 'play' triangle to activate 'Animated temporal navigation' and the settings for the time range and step.

![Activate time animation from Temporal control panel](images/13_QGIS_Time_Panel.png)

In the control panel, the time/date range should correspond to the range of the forecast, and for DHPS, a time step in hours makes sense. From here, the user can experiment with settings and the play/animate controls. To change the playback speed, click the yellow gear button in the top-right of the panel. One note to add, the author found that the time range for the layer only seems correct at the time of loading and updating the range did not seem to work if, say, the user returns to the project the next day.

## View Stations

Within this GitHub repository is a file called nsrps_model_stn_locs.json. This contains all the model-world station locations. We can import this into our project to view the stations by selecting "Layer -> Add Layer -> Add Vector Layer...".

![Add vector data](images/14_add_vector_data.png)

In the window that pops up, select the "..." box to browse to the file location. Select the wanted file and then click "Add".

![Search file](images/15_select_vector_data.png)

In the image below, you can see the stations added as grey dots. The user can adjust the transparency of the RiverDischarge layer as they see fit to assist in viewing the stations. This can be done by right clicking on the layer and selecting "Properties...".

![Select vector](images/16_stations_added.png)

Select the Transparency tab on the left-side menu, modify the Global Opacity and select "OK". In this example, it is being modified to 50%.

![Change transparency](images/17_change_transparency.png)

To make the stations easier to see, double click on the station layer, go to Symbology, and select the type of marker of interest. Once selected, click "OK".

![Station symbology](images/18_change_station_symbology.png)

Now we can easily view stations, the DHPS layer, and our base map!

![View station](images/19_view_station.png)

