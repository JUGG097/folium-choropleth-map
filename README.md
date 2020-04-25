# folium-choropleth-map
This repository was created to share my code and insight on how to generate a Choropleth map using Folium.


## WHAT IS A CHOROPLETH MAP
A choropleth map is a map which uses differences in shading, colouring, or the placing of symbols within predefined areas to indicate the average values of a particular quantity in those areas (*from oxford dictionary*) as seen in the image below:
![Choropleth map](https://dev-to-uploads.s3.amazonaws.com/i/923bb1buhmea16qsiarf.png)
In this article, I will try to walk you through the process of creating a choropleth map with python using the **folium** package. Visualization with choropleth map helps to give insight to data and is visually attractive.
I will divide the processes into four short steps which will be followed sequentially.

## STEP 1: SOURCING FOR SHAPEFILE IN *.KML* FORMAT
Inorder to generate a map visualization with **folium** we require a shapefile of the area of the world map we want to work with.
In this article I will be creating a visualization of the Nigeria map area, so the need to source for a shapefile in **.KML** format of the Nigeria map area having polygon coordinates of each state.
There are a lot of sites out there that simply supply this resource for free, for this visualization I got my shape file from [IGISMAP](https://www.igismap.com/download-nigeria-shapefile-free-administrative-boundary-state-city-map/), they also offer shapefiles for other countries.
![Igismap Site](https://dev-to-uploads.s3.amazonaws.com/i/cmc7jrhdiod50iq2h6yt.png)

## STEP 2: CONVERSION OF SHAPEFILE TO A GEOJSON
Moving on from step 1, let us convert the **.KML** file to a **Geojson** file.
I used an online cloud resource to convert my **.KML** to a **Geojson** file, the name of the online resource is [MYGEODATA](https://mygeodata.cloud/converter/kml-to-geojson).
![Mygeodata Site](https://dev-to-uploads.s3.amazonaws.com/i/ppwm98yyhokzhudwrnie.png)

## STEP 3: INTEGRATION OF OUR GEOJSON WITH THE DATA
From this step forward we get hands on with some **Python** codes.
We start by installing Python **Pandas** and **GeoPandas** packages to help us integrate the data we need to visualize into the geojson file.
In this article I am visualizing the COVID-19 confirmed cases distribution across the states of Nigeria using data gotten from the NCDC site (*note: data might not be up to date  by the time you are reading this publication*).
The Jupyter notebook containing the well commented code for this step can be found in my [GitHub Repo](https://github.com/JUGG097/folium-choropleth-map/tree/master/Notebooks).
Below is a screenshot of the final dataframe after integrating the **COVID-19** data with the Geojson file using **Pandas** and **Geopandas**.
![Integrated DataFrame](https://dev-to-uploads.s3.amazonaws.com/i/035zzmxytnsmqguo8z6m.png)

## STEP 4: GENERATION OF INTERACTIVE CHOROPLETH MAP WITH FOLIUM
To the final step which is the visualization of the choropleth map with **Folium**.
We will be using the **folium.Choropleth** module, so we need to install the Folium package for this using *conda install /pip install*.
The Jupyter notebook containing the well commented code for this step can be found in my [GitHub Repo](https://github.com/JUGG097/folium-choropleth-map/tree/master/Notebooks).
Below is a screenshot of our generated Choropleth interactive map.
![Generated Map](https://dev-to-uploads.s3.amazonaws.com/i/2j69uokluo8zexaqj3hr.png)

### PARTING WORDS...
Other forms of map visualization are possible using the **Folium** package check out the [Folium documentation](https://python-visualization.github.io/folium/modules.html) for more info on that.
The generated map can be saved as an **.html** file which can be embedded to a webpage.
I hope you find this article helpful and insightful, if so kindly leave a star on my [GitHub Repo](https://github.com/JUGG097/folium-choropleth-map).







