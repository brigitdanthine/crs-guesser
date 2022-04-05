# crs-guesser
QGIS Plugin to guess the crs

qgisMinimumVersion=3.0
description=Guesses unknown CRS for layers
version=0.1
author=Brigit Danthine
email=brigit.danthine@uibk.ac.at

The plugin was developed for the special case when there are files or coordinates whose CRS is unknown.
Note: this is not the preferred way to set the CRS. It is intended to help only in the special cases when no conclusions about the certainly correct CRS are possible. 
Short Tutorial:
1. Download this repository as zip file. Do NOT unzip it. 
2. Open QGIS and go to Plugins -> Manage and Install Plugins
3. Go to Install from ZIP
4. Choose downloaded zip and press Install Plugin

Inside the Plugin:
1. Input either one of the unknown coordinate or choose a input-layer
2. Select wether all CRS of QGIS (only EPSG) should be searched, only those of Austria or from a custom list 
3. Specifying the CRS of the output layer
4. Press OK

In the background:
The plugin converts the entered coordinate from all desired CRS into the CRS of the automatically loaded output layer

In QGIS:
5. Load a basemap (e.g. with the QuickMapPlugin)
6. Zoom to the corresponding location the point should be situated
7. Look in the attribute table from which original CRS the correctly situated point was reprojected. This is the correct CRS for the respective coordinates.  
