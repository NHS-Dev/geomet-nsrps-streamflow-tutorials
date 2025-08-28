## Accessing layers from MSC GeoMet Web Coverage Service in Python

When accessing data from GeoMet Web Coverage Service (WCS) in Python, there have been updates to the secure layers as of June 6, 2025. 
Important to note is that these changes are only to the secure layers, and the non-secure layers remain the same. 
The tutorials within this folder (aside from watershed-averaging.ipynb) use the secure layers. 
Therefore, modifications to the tutorials may be needed if working with layers that are not secure. 
These differences are listed below, and further information about these can be found in the tutorials.

1. **Variable Names**

   For the secure hidden layers, the variable names are no longer called Band1 and are instead specific to the layername that was requested.
   This change was not made for the non-secure layers, which still have variables called Band1.
    
2. **reference_time**

    For analyses, `reference_time` is no longer included in the secure layers. However, this still exists in the secure forecast layers, which continue to need it specified in a WCS Get Coverage Request. 
   
3. **Grid Resolution**

    During a WCS Get Coverage request for a secure layer, the resolution now needs to be specified. This makes sure that there hasn't been any improper interpolation of the layer.
    For non-secure layers, the resolution shouldn't be specified.


   
