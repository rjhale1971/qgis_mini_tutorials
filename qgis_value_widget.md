Software: 3.x 

Platform: Any 

In this case I am inputting data and I don't want to keep typing the same attributes into QGIS. Plus - it's nice to not worry with spelling and other things. So we are going to build a very simple dropdown list for your data.  

So I have point data. 
![qgis](/images/qgis_with_points.png) 

If you right click on the point layer in QGIS you can go to properties and in the properties dialog you will see "attributes form" on the left hand side. 

You want to select that and pick the field you want to build the value widget for. In this case I want to build a value widget for point_type. I select point_type and set the widget type to Value Map. 

![properties](/images/qgis_properties.png) 

I have a list of values that I want to build a dropdown list. Enter those values in the Value and Description. Note the Value is what is assigned and the description is what you see. So be Careful 

![widget](/images/making_the_widget.png) 

Finally - I have a dropdown list to help with data input. 

![final](/images/attributes.png) 


