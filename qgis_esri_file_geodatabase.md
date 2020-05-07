Software: QGIS 3+

Platform: Any 

QGIS can open ESRI's File Based Geodatabase. In past tutorials I used to walk you through editing. In this one I'm going to advocate moving this to a Geopackage for editing and if you need to deliver it to an ESRI based organization you can deliver the geopackage and ArcGIS Software can open it. 

The first way to view the geodatabase is to add it using the Open Data Source Manager Icon on the Data Source Manager Toolbar. 

![odsm_image](/images/open_data_manager_toolbar_hl.png) 

Click that icon and the Open Data Source Manager opens. Be sure to check Directory as the source type (since ESRI Files Based Geodatabase aren't files) and be sure to select OpenFileGDB As the Type. 

![data_source_manager](/images/data_source_manager_hl.png) 

Once you select the Geodatabase click **Add** and you will be able to add your layers from the geodatabase to QGIS. 

![select_vector](/images/select_vector_layers_to_add.png) 

The second way to view the layers in a geodatabase is to use the Browser. In 3.x the browser is built into QGIS as a panel and as a part of the Open Data Source Manager. Use the Brower to locate ESRI's Files Based Geodatabase and you'll see that it's already recognized and you can drag and drop your layer onto the map canvas. 

![browser](/images/browser.png)

