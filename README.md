# World_Weather_Analysis
Columbia DataBootcamp challenge using API calls to OpenWeather and Google Maps

## Overview
The purpose of this analysis was to generate random coordinates, use those coordinates to get the nearby cities, make an API call for weather data, and map that data for vacation planning purposes. The analysis also generated hotel names in the cities that met the vacation search criteria (minimum and maximum temperature requirements for the vacation) and plan a driving route to hotels in four cities nearby, in this case the four vacation hotels were located in Australia. 

## Results
Starting with the code below the first step of the analysis was to generate random coordinates. From here I imported citypy and generated a list of cites near to the coordinates.
~~~
lats = np.random.uniform(low=-90.000, high=90.000, size=2000)
lngs = np.random.uniform(low=-180.000, high=180.000, size=2000)
lat_lngs = zip(lats, lngs)
lat_lngs
~~~

Then making an API call to OpenWeather the following dataframe was generated with weather conditions for the list of cities: 

![Screen Shot 2022-05-21 at 9 55 56 AM](https://user-images.githubusercontent.com/99676466/169659625-371c9fdb-1e3b-410f-b2fe-6174992013c2.png)

The analysis then generated a new dataframe with hotel names in the cities that met the weather criteria of minimum temperature of 65 degrees F and maximum temperature of 75 degrees F. 

![Screen Shot 2022-05-21 at 9 57 39 AM](https://user-images.githubusercontent.com/99676466/169659691-cc7e0d59-77e1-4cc5-9f05-cbcfe23ddeed.png)

A Google heatmap was also made to show all the cities that met the criteria. The analysis continued by planning a trip to four cities in Australia that met the temperature criteria and a travel route was planned to those four cities and the hotel stays from the above dataframe. 

![image](https://user-images.githubusercontent.com/99676466/169659814-10690cbd-fdbc-4d63-900b-113866badd44.png)

## Summary
The analysis is useful for travel planning, gathering world weather data, and mapping with heatlayers, info boxes, and routes. It could be easliy tweeked to other criteria based on other weather conditions such as cloudiness or humidity. 
