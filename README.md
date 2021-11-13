# gis2minetest
A python notebook for converting geospatial data including classified LiDAR las/laz files and Open Street Maps data into [Minetest](https://www.minetest.net/downloads/) worlds.

## Credit
The following notebook was inspired and adapted from [James Wooton](https://gist.github.com/quantumjim/2d9ea27d0e0428a537b953ac04d3721b).

[Prof. Paul Pickell](https://github.com/pauldpickell) (University of British Columbia) added additional instructions and functionality to change the scale, fill holes in the ground using inverse distance weighting interpolation, integrate Open Street Maps data, and visualize other elevation derivatives. Support for additional map layers beyond LiDAR data coming soon.

Licensed under [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.en.html).

## Before you get started
- [Download Minetest](https://www.minetest.net/downloads/). To install, simply extract the contents somewhere that you have read/write access to on your computer (e.g., your user directory on Windows `C:\Users\YourUsername\minetest\`). Navigate to the `bin` folder, find the `minetest.exe` executable, right-click it and create a shortcut on your desktop or taskbar, then double-click the shortcut to run Minetest.
- [Download the csv2terrain mod from this fork](https://github.com/pauldpickell/csv2terrain). To install, simply extract the contents into your `mods` folder within your Minetest directory. For example, `C:\Users\YourUsername\minetest\mods\`. Ensure that the folder is renamed `csv2terrain`. Run Minetest and create a new world with any options then press the `Select Mods` button and you should see `csv2terrain` listed there if the installation was done correctly.
- Put the Jupyter notebook (gis2minetest.ipynb) in the same folder as your data or otherwise indicate the pathname and filename for your data. The LiDAR data can be in either `.las` or `.laz` format. It is assumed that the ground has been classified in this LiDAR point cloud.
- Read the instructions within the Jupyter notebook.

## Updates
November 9, 2021: Added new visualizations of slope and hillshade. Bug fixes.

November 7, 2021: Added new visualizations of bare Earth Digital Terrain Models (DTM) from a LiDAR point cloud and DTM derivatives such as aspect and Topographic Position Index (TPI). Stream-lined the instructions and bug fixes.

November 5, 2021: Integrated Open Street Maps (OSM) data download using the [Overpass API](https://wiki.openstreetmap.org/wiki/Overpass_API). Roads can now be mapped onto the terrain surface (see City of Vancouver screenshots below). Support for additional OSM map features coming soon. Also updated the `csv2terrain` mod to support a wider assortment of block types (e.g., stairs, slabs, and wool). This new feature allows slabs to be used to simulate sidewalks. Users are now encouraged to install [the `csv2terrain` mod from this fork](https://github.com/pauldpickell/csv2terrain) when working with the `gis2minetest` script. Bug fixes.

October 31, 2021: Added additional support for mapping tree stems and differentiating canopy structure (see Malcolm Knapp Research Forest screenshots below).

## Sample Minetest Worlds
Two prefabricated Minetest worlds are included. Extract the folder contents to your `~\Minetest\worlds\` directory and then start Minetest to load the worlds.

## Visualizing aspect
- 0-22.5° = red
- 22.5-67.5° = orange
- 67.5-112.5° = yellow
- 112.5-157.5° = green
- 157.5-202.5° = cyan
- 202.5-247.5° = blue
- 247.5-292.5° = violet
- 292.5-337.5° = magenta
- 337.5-360° = red
![Malcolm Knapp Research Forest, British Columbia, Canada](/screenshots/aspect5.png)
## Visualizing slope
- 0-18° = blue
- 18-36° = green
- 36-54° = yellow
- 54-72° = organe
- 72-90° = red
![Malcolm Knapp Research Forest, British Columbia, Canada](/screenshots/slope.png)
## Visualizing hillshade
Experimenting with 8-bit color depth in the block textures (256 block types) for visualizing different color palettes.
![Malcolm Knapp Research Forest, British Columbia, Canada](/screenshots/mkrfhillshade8bit.png)
## Visualizing Topographic Position Index
Experimenting with 8-bit color depth in the block textures (256 block types) for visualizing different color palettes.
- red (valley)
- blue (ridge)
![Malcolm Knapp Research Forest, British Columbia, Canada](/screenshots/mkrftpi8bit.png)

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
