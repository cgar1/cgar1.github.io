##Heatmap and Statistical Analysis of Sold Property in Baltimore City

For the final Iteration of my GES 486 research into sold property and if there
 is a relationship to racial density within census tracts in Baltimore City.
 For this project I utilized QGIS and GeoDa in order to get the data ready for 
 analysis and to determine if there is a statistical relationship between race
  and density of sold property.

  My process involved the separated independent/ non independent property shapefiles
  I created in my previous project. With these files created a series of gifs in my 
  previous project but what resulted was hard to decipher any significance involved.
  To revise this I used the sold property data sets to create a series of heatmaps
  over a period of 2000-2010 for both independent/ non independent property. The result 
  was a easily interpretable gif of the change in sold property density in Baltimore City


  Independent Property Heatmap

 [Independent Heatmap](https://i.imgur.com/CdEAEI2.gifv)

  Non Independent Property Heatmap

  [Non Independent Heatmap](https://i.imgur.com/dQ25zSR.gifv)


  Although you are able to identify some correlation from the new gifs and previous 
  figures, however it was necessary to see if there is a statistical significance between
  race and sold property. A Moran's I analysis was preformed on the census data in GeoDa. In QGIS
  centroids were created in each property shape after a point count inside polygon 
  was preformed then preformed. with a count added to the individual shapefiles they were now ready
  for analysis in GeoDa. The black population in each census tract is used as a weight for each year in GeoDa.
  The univariable analysis was then run against the point count that represents the sold property in each 
  block. The resulting values showed a low Moran's I but with an increase over a period 
  from 2000-2010.

  2000

  ![2000 Moran's I Analysis](https://i.imgur.com/NW7NhBW.png)

  2002

  ![2002 Moran's I Analysis](https://i.imgur.com/lxB2An0.png)

  2004

  ![2004 Moran's I Analysis](https://i.imgur.com/umxeUSj.png)

  2006

  ![2006 Moran's I Analysis](https://i.imgur.com/tfV8PNi.png)

  2008

  ![2008 Moran's I Analysis](https://i.imgur.com/4CJVyvk.png)

  2010

  ![2010 Moran's I Analysis](https://i.imgur.com/32WNkKd.png)

  The resulting information leads me to believe there is very little relationship
  between locations of property sold and density of black population within these
  neighborhood blocks.


  Data:
  Tiger Census Data
  Real Property Dataset
  
