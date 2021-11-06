# gis2minetest
A python notebook for converting geospatial data including classified LiDAR las/laz files and Open Street Maps data into [Minetest](https://www.minetest.net/downloads/) worlds.

## Updates
November 5, 2021: Integrated Open Street Maps (OSM) data download using the [Overpass API](https://wiki.openstreetmap.org/wiki/Overpass_API). Roads can now be mapped onto the terrain surface (see City of Vancouver screenshots below). Support for additional OSM map features coming soon. Also updated the `csv2terrain` mod to support a wider assortment of block types (e.g., stairs, slabs, and wool). This new feature allows slabs to be used to simulate sidewalks. Users are now encouraged to install the `csv2terrain` mod distributed with this repository when working with the `gis2minetest` script. Bug fixes.

October 31, 2021: Added additional support for mapping tree stems and differentiating canopy structure (see Malcolm Knapp Research Forest screenshots below).

## Sample Minetest Worlds
Two prefabricated Minetest worlds are included. Extract the folder contents to your `~\Minetest\worlds\` directory and then start Minetest to load the worlds.

## Downtown Vancouver, Canada
![Downtown Vancouver, Canada](/screenshots/downtownroads1.png)
![Downtown Vancouver, Canada](/screenshots/downtownroads2.png)
![Downtown Vancouver, Canada](/screenshots/downtownroads3.png)
![Downtown Vancouver, Canada](/screenshots/downtownroads4.png)

## BC Place, Vancouver, Canada
![Downtown Vancouver, Canada](/screenshots/bcplace2.png)
![Downtown Vancouver, Canada](/screenshots/bcplace3.png)
![Downtown Vancouver, Canada](/screenshots/bcplace4.png)

## Canada Place, Vancouver, Canada
![Downtown Vancouver, Canada](/screenshots/canadaplace1.png)
![Downtown Vancouver, Canada](/screenshots/canadaplace2.png)
![Downtown Vancouver, Canada](/screenshots/canadaplace3.png)

## Malcolm Knapp Research Forest, British Columbia, Canada
New feature supports mapping tree stems and differentiating canopy structure
![Malcolm Knapp Research Forest, British Columbia, Canada](/screenshots/mkrf1.png)
Trees with different heights are more apparent
![Malcolm Knapp Research Forest, British Columbia, Canada](/screenshots/mkrf2.png)
Retention trees have very well defined canopies within the harvest block and stem locations are likely accurate
![Malcolm Knapp Research Forest, British Columbia, Canada](/screenshots/mkrf3.png)
View from the ground at the edge of the harvest block, looking upslope
![Malcolm Knapp Research Forest, British Columbia, Canada](/screenshots/mkrf4.png)
View from the ground under a retention tree within the harvest block
![Malcolm Knapp Research Forest, British Columbia, Canada](/screenshots/mkrf5.png)
View from the ground under the canopy
![Malcolm Knapp Research Forest, British Columbia, Canada](/screenshots/mkrf6.png)
Shading under the canopy is now much more apparent (time is 12PM noon)
![Malcolm Knapp Research Forest, British Columbia, Canada](/screenshots/mkrf7.png)
