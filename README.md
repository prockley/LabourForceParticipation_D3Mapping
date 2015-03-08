# Getting started with mapping in D3.js

### Idea

The idea for this post came from a piece in the New York Times - ['Where working women are most common'](http://www.nytimes.com/interactive/2015/01/06/upshot/where-working-women-are-most-common.html?_r=2&abt=0002&abg=1#/5/38.5/-90).

### Map Data

- The shapefile containing the geographic information for the areas was downloaded from the CSO website:-
	http://census.cso.ie/censusasp/saps/boundaries/ED_SA%20Disclaimer1.htm
- mapshaper.org was used to reduce the detail in the shapefile to give a much smaller file size for quicker loading.
- QGIS was used to reduce the number of attributes held to reduce the file size further. Also projection changed from TM65 to WGS84.
- The shapefile was then converted to GeoJSON and then TopoJSON. These are datastores that can be read by JavaScript in user's browsers. This was a very useful tutorial:-
	http://bost.ocks.org/mike/map/

### Labour Force Projection Data
- This was taken from the CSO website:-
	http://www.cso.ie/px/pxeirestat/Statire/SelectVarVal/Define.asp?maintable=CD307&PLanguage=0
- 

### Creation of responsive D3.js choropleth chart
- This tutorial gave the basis of the image that I finally produced:-
	http://www.cartographicperspectives.org/index.php/journal/article/view/1278/1359
- After some degree of faffage the various files making up the chart were combined into one html file. This was displayed in an iframe in the actual blog post.