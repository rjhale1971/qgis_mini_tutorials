Software: QGIS 3.x 

Platform: Any

In this example you have a polygon and you want the area for that feature. We'll do this three different ways in QGIS. 

The first thing that one needs to do is set up the project properties. To do this you need to know your data's projection. If you're dealing with a geographic coordinate system areas are always a bit harder. My example will be dealing with a projected coordinate system: EPSG 2274.

On QGIS 3.x you will need to go to Project -> Properties and set the Measurement Values. For EPSG:2270 I know the Spheroid is GRS 1980 and the Units are in feet. I will set the distance measurements for feet and the area units for square feet. 

![project_properties](/images/project_properties_32.png)

First: **Identify Features**

Once you have set the Project Properties above you can click using the identify features (Blue **I**) and you can get derived measurements. In 3.2 there is also an added attribute for ellipsoid measurements. 

![attribute_toolbar](/images/attributes_toolbar_32.png)

Once you click a feature with this tool you will get derived area (and several other derived measurements). 

![Derived Area](/images/derived_area_32.png)

Second: **Field Calculator**

Once you have a layer added to QGIS you can open the Attribute table

![attribute_table](/images/attribute_table_32.png)

One you have opened the attribute table you can add a field. There are a couple of different ways to go about this but to me this is more straight forward. Edit your table by add a field called acres: 

![add_field](/images/add_field_32.png)

You will add a field that will allow decimal places. Click OK when done. 

Once the field has been added click on the field calculator: 

![field_calculator](/images/fieldcalculator_32.png)

Once that is open you will click "update existing field" and select acres as the field. Field Calculator will also add fields to your data. For the expression you will use **$area**. The expression **$area** will add your distance units added in the Project Properties. So if your area units are **square feet** - this will add square feet. If square meters - then **square meters**. I am converting the square feet to acres so **$area/43560**. Click OK. 

Third: **Database manager**

Click on the database manager 

![database manager](/images/dbmanager_32.png)

Once the Database Manager is open click on Virtual layers. Drive down to the layer that you need to know the area. 

![database manager](/images/database_manager_32.png)

Click on the SQL Script icon and type the following: 

***select st_area(geometry)/43560 from tracts_2274***

This will give you an area for each of the features in the layer. This ignores project properties and uses the units from the projection. You may need to add a **where clause** at the end to narow down the returned area measurements. 

