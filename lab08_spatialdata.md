# Mapping / Data

There is an expansive set of approaches and tools for mapping. 
The fields of geography and cartography offer many important methods and critiques to draw on when engaging in spatial analysis and mapping. Richard White's work is an exciting and necessary [read](https://web.stanford.edu/group/spatialhistory/cgi-bin/site/pub.php?id=29) for historians. While by no means exhaustive, I find it helpful to think about this area of inquiry as characterized by 
several broad categories:

1. Interactive Mapping: Flexible interactive visualizations served over the web. 
Platforms include [CARTO](https://carto.com/) and [MapBox](https://www.mapbox.com/).  
DH Projects like [Photogrammar](http://photogrammar.yale.edu) (project) 
and [Mapping Inequality](https://dsl.richmond.edu/panorama/redlining/) use Carto.

2. Narrative Mapping: Maps used to tell a story. They tend to support primarily linear story telling.  
Platforms include StoryMap.js, [Odysessy](https://cartodb.github.io/odyssey.js/), 
[ESRI Story Maps](https://storymaps.arcgis.com/en/). An example 
is [Renewing Inequality](http://dsl.richmond.edu/panorama/renewal/).

3. Classic Cartography and Geographical Data: The study and practice of making maps.  
This often involves the use of rastor (set of pixels representing real world features 
such as an aerial photograph or land elevations) and vector (set of x,y coordinates 
that create points, lines, polygons, which represent features such as county borders and streets) 
data to create maps. This is often what people mean what they say they want a GIS system. 
They are often necessary for georectifying maps. The main platform is ESRI's ArcGIS and open source QGIS for Mac.


4. Spatial Analysis:  While this term is sometimes applied more broadly, it commonly is used 
for computational analysis of spatial data. This most often is in the form of predictive 
modeling such as tracking population movement or the the spread of a disease across a community. 
Platforms such as ArcGIS have specialized in this area. Programming languages like R and python also 
allow for this. Web-based interactive mapping tools like Carto continue to build this kind of functionality. 
For an example, see [Forced Migration of Enslaved Peoples](https://dsl.richmond.edu/panorama/forcedmigration/).


We are going to use *ESRI StoryMaps* and *ESRI ArcGIS Online* to build our maps.  
In order to build a map, we need to use a **geographic coordinate system**, 
which "is a coordinate system used in geography that enables every location on Earth 
to be specified by a set of numbers, letters or symbols. 
The coordinates are often chosen such that one of the numbers represents a vertical position, 
and two or three of the numbers represent a horizontal position. 
A common choice of coordinates is latitude, longitude 
and elevation" [(Wikipedia, "Geographic coordinate system")](https://en.wikipedia.org/wiki/Geographic_coordinate_system).

For our purposes, we will using:
- latitude: specifies the north–south position of a point on the Earth's surface
- longitude: specifies the east–west position of a point on the Earth's surface

For example, Gottwald is Latitude: 37.5741928 and Longitude: -77.5403352, or 
most commonly represented as "37.5741928,-77.5403352".

We can get this information using systems like [Google Maps](https://maps.google.com) 
or [Latlong.net](https://www.latlong.net/)


## Spreadsheet
One way to keep track of your locations is to build a custom data set using a spreadsheet. Here is a [template](https://docs.google.com/spreadsheets/d/19K4ENdnGEhR-GNa7LTJlGOoOdqAzbWZrDcJGCuXB3E8/edit?usp=sharing). What are the columns and rows?

- Save your own copy. Log into your google account using your @richmond account. Then select 'File' -> 'Make a Copy'. This will save a copy in your Google Drive, which you can edit. 
- Let's take a look at row "2018-11-05 15:00". Copy and paste the lat/long in Google Maps. What happens? 

Note: You'll notice that the precision of the lat/long matters. A slight change in the number will move the point on the map. Let's compare "37.574298,-77.5421208" vs "37.5744531,-77.5401856" vs "37.574231,-77.5402788". What happens?

- Fill in row "2018-11-05 8:00" through row "2018-11-05 14:00". 

