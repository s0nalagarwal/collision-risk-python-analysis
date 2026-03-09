# collision-risk-python-analysis
The goal is to create a function that takes an input of collision data points and street centerline data and will output a color-coded interactive map of roads with high risk of collision. This measure will be based on collisions per length in meters for each road.

Overall Project workflow:

* Read in road and collision data
* Set an extent in long/lat and then convert back into a regional CRS.
* Crop all datasets to correct extent
* Conduct a spatial join based on distance
* Find outliers, make boxplots, and other descriptive stats
* Merge spatial join dataset back to original roads dataset
* Divide counts by length column
* Plot based on quantiles, or any other specified break method
* Plot on interactive map using leafmap
* Make a function that does all of these steps automatically so that this workflow can work for other parts of San Francisco, and other datasets too, if possible.
