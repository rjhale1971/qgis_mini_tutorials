Software: QGIS 3.x

OS: Any

As of 2014 – ESRI has placed in it’s Terms Of Service that you MUST be an ESRI ArcGISOnline customer to use this data. As I’m not – I will no longer be using the service. If you ARE – please proceed. 

This tutorial is going to use some freely available WMTS services at ESRI.

Go to http://services.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer

![mapserver](/images/mapserver_hl.png) 


If you notice at the top this service is published in several different forms – one of these is a WMTS (highlighted). Click on the WMTS link for this service:

http://services.arcgisonline.com/arcgis/rest/services/World_Imagery/MapServer/WMTS/1.0.0/WMTSCapabilities.xml

Copy the URL from your web browser to your clipboard. 

Open QGIS. Select the Open Data Source Manager icon. 

![data_manager](/images/open_data_manager_toolbar_hl.png) 

Once the WMS/WMTS menu open Click New. 

![wmts](/images/wmts_menu.png) 

Give the service a name and copy the URL into URL Text Box

![wmts_new](/images/new_wmts.png)

Click OK. Click Connect.

There are two versions of the service. Click one and click add.

![tilesets](/images/tilesets.png)

Enjoy your new Image Service

![qgis](/images/qgis_world_imagery.png) 


 
