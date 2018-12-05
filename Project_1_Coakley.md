# Does the sale of Properties Correlate to Social Factors
Using Census Data to identify racial density in neighborhoods in Baltimore, MD I was able to correlate the sale of properties to having a greater impact on those in poverty and in most cases the black population of Baltimore. I was able to further link this to the current developments in Baltimore and how these specific areas are targeted by corporations and developers. The data is focussed around 2010 with supporting information that shows demographic information for baltimore neighborhoods. The SQL I preformed selected lots that were sold only in 2010 and projected those properties onto my map.

![White Population 3D](https://i.imgur.com/s8KpxXF.png)

![Black Population 3D](https://i.imgur.com/nRc3tSu.png)

![SQL](https://i.imgur.com/p5B9Azs.png?1)

![Poverty Density VS Project Density](https://i.imgur.com/3NwAGkp.png)

![Racial Density and Houses sold](https://i.imgur.com/ja5FDWB.png)

Applications: QGIS utilizing SpatiaLite

Projection: NAD83(2011) / Maryland (ftUS)

Data Sources:

Census data was obtained from the US census website in the form of a TIGER/Line shapefile named Consolidated Cities under the 2010 demographic profile. https://www.census.gov/geo/maps-data/data/tiger-data.html

Dillon Mahmoudi provided the Real_Property Data which includes shapefiles of properties with information including tax and saledates of specific lots.
Poverty data was aquired from Dillon Mahmoud's github on gentrifiedtracts.
https://github.com/dillonma/gentrifiedtracts

I obtained a polygon of Baltimore city as well as the water feature and current economic projects from  http://gis-baltimore.opendata.arcgis.com/
