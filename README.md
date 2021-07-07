# Final Assignment

### Status

Once you are finished with the final assignment, edit this readme and add "x" to the correct box:

* [x] Submitted

* [ ] I'm still working on my final assignment. 


### Instructions

*you can remote these instructions for the final submission*

Read the final assignment instructions from the course webpages [https://autogis.github.io](https://automating-gis-processes.github.io/site/lessons/FA/final-assignment.html). Remember to write readable code, and to provide adequate documentation using inline comments and markdown. Organize all your code(s) / notebook(s) into this repository and **add links to all relevant files to this `README.md`file**. In sum, anyone who downloads this repository should be able to **read your code and documentation** and understand what is going on, and **run your code** in order to reproduce the same results! :) 

**Modify this readme so that anyone reading it gets a quick overview of your final work topic, and finds all the necessary input data, code and results.** 

*Note: If your code requires some python packages not found in the csc notebooks environment, please mention them also in this readme and provide installation instrutions.*

*Note: Don't upload large files into GitHub! If you are using large input files, provide downloading instructions and perhaps a small sample of the data in this repository for demonstrating your workflow.*

Fill in details of your final project below. You can remove this instructions-section from the README-file if you want.

## Topic: AccessViz

### Structure of this repository: 
1. FileFinder
2. TableJoiner
3. Visualizer
4. Comparison tool

### Input data:
MetropAccess YKR grid file (MetropAccess_YKR_grid_EurefFIN.shp)
http://www.helsinki.fi/science/accessibility/data/MetropAccess-matka-aikamatriisi/MetropAccess_YKR_grid.zip.

Helsinki Region Travel Time Matrix data (example grid cells)
http://blogs.helsinki.fi/accessibility/helsinki-region-travel-time-matrix/.
travel_times_to_ 5785640.txt
travel_times_to_ 5785641.txt
travel_times_to_ 5785642.txt
travel_times_to_ 5785643.txt

### Analysis steps:
1. FileFinder finds a list of Travel Time Matrix files according to an input list of YKR ID values. If a YKR ID is not found in a specified input folder nor its subfolders, the tool warns the user but continues running. The tool also informs the user of the execution process.
2. Tablejoiner joins the Matrix file with MetropAccess YKR grid shapefile by using a corresponding column of YKR IDs. The resulting Shapefile is then saved to an output folder defined by the user.
3. Visualizer visualizes travel times of the selected YKR grid cells on four possible travel modes: 1) car, 2) public transport, 3) walking, and 4) biking. The user decides which modes are visualized, where the results are saved, and whether the map is going to be static or interactive.
4. Comparison tool compares travel times or travel distances of two different traveling modes defined by the user. The calculation is done based on the order of the inputs: the first mode is substracted by the second. The outputs are saved as Shapefiles. If invalid parameters are given, the tool stops the program and offers advise on what values are acceptable. AccessViz can be run without doing any comparisons.

### Results:
1. A list of filepaths to Travel Time Matrix files.
2. A Shapefile of joined Matrix + MetropAccess YKR grid files.
3. Visualizations of selected travel modes (either static or interactive)
4. A Shapefile based on a GeoDataFrame with the calculated comparison.
+ An interactive visualization of the comparison.

### References:
- Literature related to the topic
- Links to websites, tutorials books or articles that you found useful
More on the Travel Time Matrix:
http://blogs.helsinki.fi/accessibility/helsinki-region-travel-time-matrix/

