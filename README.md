# Street extract to linked places

This code takes a set of coordinates and returns a file in [Linked Places format](https://github.com/LinkedPasts/linked-places-format) listing all of the roads with some data about the type of road  
It makes use of [OpenStreetMap](http://www.openstreetmap.org/) data for the current streets and the [GB1900 Gazetteer](https://www.visionofbritain.org.uk/data/) (Abridged) made available by the GB1900 Project for the list of streets in 1900  
Because the gazetteer only covers the British Isles, it will only work with places within the UK, if you want to use it for anywhere outside of that, you will need to provide dates 
This code was originally written for a project focussed on the Campsbourne Estate in London, so default settings are for that location

## How to use the code

### Variables to amend
The program takes a set of co-ordinates, in this case the boundary of the Campsbourne Estate, but these coordinates can be amended to select another area. 
** To find the relevant coordinates ** go to [OpenStreetMap](http://www.openstreetmap.org/) and find the top left point of the area of interest, right click on it then select Show address. The coordinates shown will be for the north and west points, repeat this in the bootom right for the south and east points  
Because the Campsbourne Estate is in London, the initial data selection is for London, this is simply to give a smaller dataset to select the from, this can be amended by the user to another filter area if required.  
** To find the relevant surrounding area name ** go to [OpenStreetMap](http://www.openstreetmap.org/) and find the area of interest, right click on it then select Query features. In the list of features, look under the Enclosing features heading and chose one at an appropriate level  
Once you have amended the coordinates and filter area as required, adjust the project url to the appropriate one for your project  

### Running the code

The code is in a jupyter notebook, which you can run using the binder link below  
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/JoKent/campsbourne/HEAD?urlpath=%2Fdoc%2Ftree%2Fstreet-extract-to-linked-places.ipynb)   

Amend the variables in the second code block, or run with the existing ones if you just want to get the default results set for the campsbourne estate  

Run each block of code in order by pressing the 'play' icons next to the code blocks, the resulting data set in Linked Places format will be output into the binder folder  

** You must copy down this file before closing the window, binder resets when it is closed, so you will lose the file if you do not save it  ** 


