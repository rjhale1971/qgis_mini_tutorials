Software: QGIS 3+

Platform: Any 

You can add csv files to QGIS if the CS has an X and Y coordinate. This example comes from https://earthquake.usgs.gov/earthquakes/feed/v1.0/csv.php

Open QGIS and go to the Data Source Manager Toolbar

![data_source_manager](/images/data_source_manager_toolbar.png)

Click on the Open Data Source Managear icon:  

![data_source_icon](/images/data_source_manager_toolbar_highlight.png)

Once that opens, go to Delimted Text. Add your file. In this case I am adding the month summarization of all the earthquakes from the USGS. I know the file is comma delimited and that it has a Longitude (X) and Latitude (Y) field. I also know that the data is in EPSG:4326. You do need to know what projection your data is in and what fields it contains. 

![add_csv_hl](/images/addcsv_highlighted.png) 

Once it is set up click Add. 

![qgis_data](/images/qgis_data.png) 

Once you reach this point You'll need to save this csv layer to  a file.  
