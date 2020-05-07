Software: QGIS 3.x 

Platform: Any

If you want the x and y coordinates for point data it's fairly simple to do in QGIS 3.x. There's actually two ways you can go about doing this - with the first explanation being the easiest the second explanation being a bit more flexible. 

Add your data to qgis. 

![qgis](/images/qgis_data.png) 

Once it has been added go to the processing tools and search for the ***added geometry values*** tools.  

![geometry](/images/add_geometry_attributes.png) 

Execute the tool. It will create a new layer called ***Added Geometry Info***. That will add a Xcoord and ycoord to your data. 

![attributes](/images/added_geom_info.png)

The second way to derive X and Y is to use the ***Field Calculator***. Open the Attribute table and start editing. 

![attribute_edit](/images/edit_attribute_hl.png) 

Open the Attribute and you can add and calculate a new field at once. Add a field called ***xcoord*** and add $x into the expression builder. Click OK and you have a new field called xcoord that has been calculated. 

![field_calc](/images/xcoord.png) 

To repeat with the y coordinate just add a ***ycoord*** field and use $y in the expression builder. 
