#Zipcode Viewer
##Uses HTML5, javascript and css.

An HTML page to view zipcodes by municipalities in Mexico. 

###Libraries used:

* d3.js - For csv parsing and scales. 
* jQuery - For event handling. 
* topojson - Part of d3, for geographical projections. 
* ogr2ogr - Part of GDAL. For converting shapefiles into json. Usage explained below.

###Fonts used:

* [Montserrat](https://fonts.google.com/specimen/Montserrat)

###Scripts:

* Index.html - Main HTML page. Calls the js scripts. 
* altGto.js - Main js script. Parses the csv data and draws the map. Based on the Guanajuato Zip Code viewer. 

###Sources: 

* mex_municipal.shp - Shapefile for the desired state with municipalities. 
* munzip.csv - Csv with CVEGEO, name and CP columns.

###Preparing the files

1. Download the desired shapefile from your website of choice. I downloaded the agebsymas package from [Diego Valle's Website](https://www.diegovalle.net/). 
2. Identify the shapefile you need. I used gto_municipal.shp. 
3. Convert the shapefile to JSON using ogr2ogr. This was tricky to learn. 
	* You have to navigate, using the commandline, to the folder where your .shp is stored. .dbf, .prj and .shx files *must be in the same folder as the .shp file*.

	* ogr2ogr -f GeoJSON gto.json gto_municipal.shp *(where "gto.json" is the output file, and "gto_municipal.shp" is the input file.)*

4. Your file is ready to be used. 