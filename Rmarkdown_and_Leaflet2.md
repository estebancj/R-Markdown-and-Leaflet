---
title: "Coursera: Developing Data Products 2017 - R Markdown and Leaflet"
author: "Esteban Castillo"
date: "December 15, 2017"
output: 
      html_document:
        self_contained: false
        keep_md: true
---



## Instructions

1. Create a web page using R Markdown that features a map created with Leaflet.

2. Host your webpage on either GitHub Pages, RPubs, or NeoCities.

3. Your webpage must contain the date that you created the document, and it must contain a map created with Leaflet. We would love to see you show off your creativity!


## Interactive map of Puebla Mexico, top universities


This is a quick example of a map of the three top universities located in Puebla city (near to Mexico city) using the package Leaflet for the interactive map (with the location of each university) and Rmarkdown to create a HTML presentation of this assignment.


## Steps


Load the Leaflet package for the interactive map. If not installed, type on the console install.packages("leaflet"). Additionally load the magrittr package for using pipes (%>%). If not installed, type on the console install.packages("magrittr")


```r
library(leaflet)
library(magrittr)
```

Load lats and longs associated to the top universities and show them in the interactive map (including a hyperlink to each of them).


```r
map <- leaflet() %>%
  addTiles() %>%
  addMarkers(lng=-98.283107, lat=19.054420, popup='<a href="http://www.udlap.mx/inicio.aspx?idioma=2"> UDLAP</a>') %>%
  addMarkers(lng=-98.201159, lat=19.034521, popup='<a href="http://www.buap.mx/">BUAP</a>') %>%
  addMarkers(lng=-98.2163, lat=19.0485, popup='<a href="https://web.upaep.mx/index.php?option=com_content&view=article&id=3255&Itemid=1555">UPAEP</a>')
map 
```

<!--html_preserve--><div id="htmlwidget-76cd8e7bed150d295885" style="width:672px;height:480px;" class="leaflet html-widget"></div>
<script type="application/json" data-for="htmlwidget-76cd8e7bed150d295885">{"x":{"options":{"crs":{"crsClass":"L.CRS.EPSG3857","code":null,"proj4def":null,"projectedBounds":null,"options":{}}},"calls":[{"method":"addTiles","args":["https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"maxNativeZoom":null,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"continuousWorld":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":null,"unloadInvisibleTiles":null,"updateWhenIdle":null,"detectRetina":false,"reuseTiles":false,"attribution":"&copy; <a href=\"http://openstreetmap.org\">OpenStreetMap<\/a> contributors, <a href=\"http://creativecommons.org/licenses/by-sa/2.0/\">CC-BY-SA<\/a>"}]},{"method":"addMarkers","args":[19.05442,-98.283107,null,null,null,{"clickable":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},"<a href=\"http://www.udlap.mx/inicio.aspx?idioma=2\"> UDLAP<\/a>",null,null,null,null,null,null]},{"method":"addMarkers","args":[19.034521,-98.201159,null,null,null,{"clickable":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},"<a href=\"http://www.buap.mx/\">BUAP<\/a>",null,null,null,null,null,null]},{"method":"addMarkers","args":[19.0485,-98.2163,null,null,null,{"clickable":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},"<a href=\"https://web.upaep.mx/index.php?option=com_content&view=article&id=3255&Itemid=1555\">UPAEP<\/a>",null,null,null,null,null,null]}],"limits":{"lat":[19.034521,19.05442],"lng":[-98.283107,-98.201159]}},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->



