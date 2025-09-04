## Accessing layers from MSC GeoMet Web Coverage Service in Python

** Update, Summer 2025: Changes to secure layer access through the Web Coverage Service

Note that these tutorials were updated in Summer 2025 taking into account the recent updates 
that were put in place with the most recent GeoMet update on June 6, 2025 (v.2.36).

Please note is that these changes are only to the secure layers, and the non-secure layers remain the same. The tutorials within this folder (aside from watershed-averaging.ipynb) use the secure layers. These differences are listed below, and further information about these can be found in the tutorials.

1. **Variable Names**

   For the secure hidden layers, the variable names are no longer called "Band1" and are instead specific to the layername that was requested.
   This change was not made for the non-secure layers, which still have variables called Band1.
    
2. **reference_time**

    For analyses, `reference_time` is no longer included in both secure and non-secure layers. However, `reference_time` metadata still applies to forecast layers, and must be specified in WCS Get Coverage Requests for forecast layers. 
   
3. **Grid Resolution**

    During a WCS Get Coverage request for a secure layer, the horizontal grid resolution now needs to be specified. This ensures that there hasn't been any improper interpolation of the layer. For non-secure layers, the resolution shouldn't be specified.


   
