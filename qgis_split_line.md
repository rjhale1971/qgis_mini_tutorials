Software: 3.x

Platform: Any

I have a line that I need to split into equal lengths. In this case the split will be 1000 foot segments.  
![qgis](/images/qgis_screenshot.png)

Open your processing tool box and search for ***v.split***. ***v.split*** is a tool in the GRASS toolset in QGIS. 

![tool](/images/grass_processing.png)

Be sure to put 1000 in the maximum segment length. If you do not adjust the file location it will be written to a temporary file location. There are several other options you can adjust but for this example I left them default. 

![tool](/images/vsplit.png)

After the processing tool runs you will have a new feature that has been split into 1000 foot segments.o

![tool](/images/qgis_split_by_length.png)
 
