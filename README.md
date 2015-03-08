# Labour Force Participation / Getting started with mapping in D3.js

### Idea

The idea for this post came from a piece in the New York Times - ['Where working women are most common'](http://www.nytimes.com/interactive/2015/01/06/upshot/where-working-women-are-most-common.html?_r=2&abt=0002&abg=1#/5/38.5/-90).

### Map Data

- The shapefile containing the geographic information for the areas was downloaded from the CSO website:-
	http://census.cso.ie/censusasp/saps/boundaries/ED_SA%20Disclaimer1.htm
- mapshaper.org was used to reduce the detail in the shapefile to give a much smaller file size for quicker loading.
- QGIS was used to reduce the number of attributes held in the file to reduce the size further. Also projection changed from TM65 to WGS84.
- The shapefile was then converted to GeoJSON and then TopoJSON. These are datastores that can be read by JavaScript in user's browsers. TopoJSON creates the smallest possible file size. This was a very useful tutorial:-
	http://bost.ocks.org/mike/map/

### Labour Force Projection Data
- This was taken from the CSO website:-
	http://www.cso.ie/px/pxeirestat/Statire/SelectVarVal/Define.asp?maintable=CD307&PLanguage=0
- This is the [raw data](https://github.com/prockley/LabourForceParticipation_D3Mapping/blob/master/data/150305_1_LFPR_Raw.csv).

- As the raw data contained participation rates for 3 age ranges (25-34, 35-44, and 45-54) this had to be combined into one value to suit the blog post. To avoid any bias caused by differing numbers of people in each range the weighted average was calculated.
- Population data for 2011 was taken from CSO table [CD204](http://www.cso.ie/px/pxeirestat/Statire/SelectVarVal/Define.asp?maintable=CD204). The population data is [here](https://github.com/prockley/LabourForceParticipation_D3Mapping/blob/master/data/150305_2_Pop_Raw.csv).

- The resulting data used in the blogs chart is shown [here](https://github.com/prockley/prockley.github.io/blob/master/assets/LFPR2011_Data.csv).

### Creation of responsive D3.js choropleth chart
- This tutorial gave some of the basis for the final visualisation:-
	http://www.cartographicperspectives.org/index.php/journal/article/view/1278/1359
- The JavaScript code can be seen [here](https://github.com/prockley/prockley.github.io/blob/master/js/LFPR2011.js).
- After some degree of faffage the various files making up the chart were combined into one html file. This was displayed in an iframe in the actual blog post.