Software: QGIS 3+

Platform: Any 

You can store images in [Geopackage] (https://www.geopackage.org). In this case I'm going to take the image in my qgis session and save it to geoapckage. Later I can save vector data into this same geopackage. 

![qgis desktop](/images/qgis_with_image.png) 

In order for an image to go into a geopackage it has to be in byte format. In this case my image is float32 (NAIP). 

![layer_properties](/images/layer_properties.png)

Note the data type (almost in the middle) is float32. I need to convert it to byte. In order to convert it you need to use the gdal_translate tool in the Geoprocessing toolbox.  

![gdal_translate](/images/translate.png) 

When that runs you have a image that is named ***converted*** that is added to your layer panel. From there, Right click on your image in the layer panel and go to **Save As**

![save-as_geopackage](/images/save_as_geopackage.png) 

You have now saved a image to a geopackage. 
 
