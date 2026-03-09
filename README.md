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

Example Output: 

San Francisco Downtown: 
<img width="1431" height="601" alt="Screenshot 2026-03-09 at 12 40 08 AM" src="https://github.com/user-attachments/assets/96e53d4f-fcd7-4722-bc68-1847a8ee42ec" />

Close Up: 
<img width="1431" height="599" alt="Screenshot 2026-03-09 at 12 40 19 AM" src="https://github.com/user-attachments/assets/fdb411d8-9da7-4454-8b47-272a280f0559" />


Residential Area in SF:

<img width="1416" height="599" alt="Screenshot 2026-03-09 at 12 41 11 AM" src="https://github.com/user-attachments/assets/179872c3-ff4b-4fea-a47b-c5dee49b4cb6" />

This project was done for ABT 182 WQ 2026 at UC Davis. 
