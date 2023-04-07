## Plotting a Graph from MERRA-2 NetCDF Files using Python
# by Jeffrey Fernandez

In this notebook, I utilized Python to plot a graph from the M2TMNXSLV (or tavgM_2d_slv_Nx) dataset, which is a time-averaged 2-dimensional monthly mean data collection within the Modern-Era Retrospective analysis for Research and Applications version 2 (MERRA-2). 

The M2TMNXSLV dataset includes meteorology diagnostics at commonly used vertical levels, such as air temperature, wind components, sea level pressure, surface pressure, and total precipitable water vapor. The dataset is provided in NetCDF format.

To plot a graph from these files, I used the netCDF4 package in Python to read in the data and the matplotlib library to create the graph. I loaded the necessary modules and libraries at the beginning of my code, and then used the following code to read in the NetCDF file:

```python
import netCDF4
import numpy as np

# open NetCDF file
nc_file = netCDF4.Dataset('/path/to/M2TMNXSLV.nc')

# read in variables
var1 = nc_file.variables['var1'][:]
var2 = nc_file.variables['var2'][:]
