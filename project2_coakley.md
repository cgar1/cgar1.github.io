Garrett coakley

GES 486

In a continuation of my first project I created a temporal
display showing sold houses in Baltimore from 2000-2010 for
both independent and non-independent owners. When I say
independent owners I am talking about houses that were
sold by individual people that had their own name listed
as the owner of the property and non independent being
property that was owned and sold by a LLC or similar corporation.
The reason for this is to differentiate houses that are sold by
 development and rental companies and determine if there is any
 correlation between sold houses and race. Before I began this project
 I had this assumption in mind that a higher density of sold houses would
 happen following 2007 due to the recession that occurred after that point in
 time. What I observed was higher clusters occurring after 2007 but also
 in much denser clusters in predominately black communities. The process for creating these maps involved a series of sql querys that
 produced houses grouped by corporation or business type. I also had to remove properties owned by the
  state or local government as well as schools and churches. With these groups separated it was just a matter
  of running a second sql on my two groups of interest to separate by the date
  the property was sold. Below is the gifscreated from the resulting data.

![independent](https://imgur.com/a/wE5kZwB)

![non-independent](https://imgur.com/a/Iiz4rw2)

Below is code for a python selection and a save to drive function.
'''python

from PyQt5.QtGui import QColor

from PyQt5.QtCore import Qt

from qgis.utils import iface

housing=('C:/Users/garrett m coakley/Documents/Projects/486/project 2-20181108T042751Z-001/project 2/Project 2/Shape Files/housing2_fix.shp', 'housing', 'ogr')

iface.addVectorLayer('C:/Users/garrett m coakley/Documents/Projects/486/project 2-20181108T042751Z-001/project 2/Project 2/Shape Files/housing2_fix.shp', 'housing', 'ogr')

housing = iface.activeLayer()

expr = QgsExpression( "\"saledate\" LIKE '%2010'" )

selected_houses = housing.getFeatures( QgsFeatureRequest( expr ) )

ids = [i.id() for i in selected_houses]

QgsVectorFileWriter.writeAsVectorFormat(ids, r'C:/Users/garrett m coakley/desktop/ids.gpkg', 'utf-8', ids.crs(),'GPKG', True)
'''

The above python code is a simple selection of an active layer using QgsExpression and providing a like statement for values within the indicated column.
The code then saves the selected attributes directly to the local drive or wherever it is specified.
