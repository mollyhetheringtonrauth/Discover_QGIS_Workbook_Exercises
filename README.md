# DISCOVER QGIS 3.x Workbook exercises

Compilation of the workbook exercises and challenge problems I completed as I taught myself QGIS using DISCOVER QGIS 3.x Workbook by Kurt Menke.

## Scope of skills demonstrated
* Stylizing a map to communicate key biogeographical features
* Working with vector and raster data and files types
* Normalizing geospatial data
* Developing automated analysis pipelines using the Processing Modeler Tool
* Creating, managing, and querying geospatial databases using SpatiaLite

## PART 1: Introduction to Geospatial Technology

### Exercise 2 Challenge: Displaying Geospatial Data
In this challenge exercise I stylize a map displaying the species distribution of black bears across the eastern United States in relation to federal land ownership. I colored the federal land ownership according to the standard Bureau of Land Management colors.

### Exercise 5: Basic Geospatial Analysis Techniques
In this exercise I conduct a spatial analysis of the National Geodetic Survey Monuments of Albuquerque New Mexico using open source data.
Completed Tasks:
* Downloaded open source vector data of 1) the locations of the Geodetic Survey Monuments, 2) the municipal limits for Bernalillo County, 3) the road inventory for Bernalillo County, and 4) the county limits for the state of New Mexico. All data files can be found in the Part1/Exercise5 directory.  
* Normalized the Data. 1) Convert all layers to the same CRS (in this case State Plane Coordinate System: NAD83(HARN)/New Mexico Central(ftUS)). 2) Clip all data layers to the study area (the City of Albuquerque) using overlay tools and query/selection tools.
* Additional tools used: 1) dissolve tool to merge adjacent polygons together, 2)vector buffer tool to create a 1 mile radius around the Albuquerque City limit, 3) provider feature filter tool to filter the features of a vector layer using a SQL query, 4) select features by value tool within the attribute table, 5) clip tool to crop a layer in accordance with the features of another layer
* Labeled landmarks (roads, geodetic survey monuments) and stylized a map

## PART 2: Spatial Analysis

### Exercise 4: Vector Data Analysis- Overlay Techniques
In this exercise I explore the spatial relationships between two input vector datasets using overlay techniques. I use data on the distribution of the Sierra Spotted Owl and Sierra Willow Flycatcher within the Sierra National Forest boundary.
Tools Used:
* clip tool - outputs the features of dataset A that fall within the features of dataset B
* intersection processing tool- outputs the features common to both dataset A and dataset B
* union processing tool - topological overlay of two polygon datasets; the output preserves the features that fall within the spatial extent of either dataset
* dissolve processing tool- creates a single feature multi-polygon shape layer from a multi-feature multi-polygon shape layer while maintaining all the original attributes

### Exercise 5: Vector Data Analysis- Creating a site selection model
In this exercise I use the Processing Modeler Tool to build a reproducible and automated multi-step data analysis model to discover airports that meet the specific criteria provided by a client. Specifically the model discovers airports located in Nueces County, Texas that are within 3 miles of Corpus Christi city limits (but not within the city), 0.5 miles within any source of water and within 1 mile of a county road.

What is great about using the Processing Modeler Tool, is that the model is saved and can be used on different datasets and ran as a single process. Additionally, the model can be exported as python code.

### Exercise 7: Raster Data Analysis- Working with Topographic Data
In this exercise I used a digital elevation model raster to determine suitable habitat for a plant species. Specifically, starting with a digital elevation model raster layer (.dem), I used the Raster Terrain Analysis Processing Tools to calculate the hillshade, slope and aspect. I used the reclassification tool to aggregate the continuous data from the slope and aspect rasters into categorical data that corresponded to suitable habitat for plant species A. Lastly, to determine habitat suitability while accounting for both slope and aspect, I performed a raster calculation where I added the reclassified slope and aspect raster layers together.

### Exercise 8: Raster Data Analysis- Density Surfaces
create a heatmap from vector data points

## PART 3: Data Acquisition and Management

### Exercise 4
aggregating data. grouped by subregion
stylized a map

### Exercise 5: Raster Data Structure
merging and clipping raster data- raster data often come in tiles and need to be merged together to form a seamless raster covering the study area
