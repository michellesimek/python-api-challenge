# Python-api-challenge

## Part 1: WeatherPy

The first task of this assignment was to wrtie a Python script to visualize the weather of 500+ cities across the world of varying distance from the equaton using OpenWeatherMap API. 

### Relationships between all cities
The first requirement was to create a series of scatter plots to showcase the following relationships:

- Temperature (F) vs. Latitude
![GitHub Logo](/Images/latitude_vs_temp.png)

- Humidity (%) vs. Latitude
![GitHub Logo](/Images/latitude_vs_humidity.png)

- Cloudiness (%) vs. Latitude
![GitHub Logo](/Images/latitude_vs_cloudiness.png)

- Wind Speed (mph) vs. Latitude
![GitHub Logo](/Images/latitude_vs_windspeed.png)

Next the cities were split up depending on if they were located in the Northern Hemisphere (greater than or equal to 0 degrees latitude) or Southern Hemisphere (less than 0 degrees latitude). The following plots and linear regressions were then created:

- Northern Hemisphere - Temperature (F) vs. Latitude
![GitHub Logo](/Images/northernhem_temp_vs_lat.png)

- Southern Hemisphere - Temperature (F) vs. Latitude
![GitHub Logo](/Images/southernhem_temp_vs_lat.png)

- Northern Hemisphere - Humidity (%) vs. Latitude
![GitHub Logo](/Images/northernhem_humidity_vs_lat.png)

- Southern Hemisphere - Humidity (%) vs. Latitude
![GitHub Logo](/Images/southernhem_humidity_vs_lat.png)

- Northern Hemisphere - Cloudiness (%) vs. Latitude
![GitHub Logo](/Images/northernhem_cloudiness_vs_lat.png)

- Southern Hemisphere - Cloudiness (%) vs. Latitude
![GitHub Logo](/Images/southernhem_cloudiness_vs_lat.png)

- Northern Hemisphere - Wind Speed (mph) vs. Latitude
![GitHub Logo](/Images/northernhem_windspeed_vs_lat.png)

- Southern Hemisphere - Wind Speed (mph) vs. Latitude
![GitHub Logo](/Images/southernhem_windspeed_vs_lat.png)

## Part 1: VacationPy
Looking at the city weather data we pulled from part 1 (WeatherPy), we created a heatmap displaying the humidity of each city. The data was then narrowed down to only citys with ideal weather conditions. Those conditions included:
- A max temperature lower than 80 degrees but higher than 70
- Wind speed less than 10 mph
- Zero cloudiness

Next, Google API places was used to find hotels within a 5000 meters radius for cities with the above ideal weather conditions. The Google API used was NearBySearch, which required iterrating through the dataframe and grabbing each city's latitude and longitude coordinates. After the hotels were located, only the first hotel for each city has pulled in the hotel dataframe. If no hotels were found within a 5000 meters radius, Hotel Name in the data was left blank. 

Finally, the hotel names were plotted on top of the humidity heatmap, with each pin containing the Hotel Name, City, and Country.

![GitHub Logo](/Images/heatmap5.png)


## Observable Trends

Three observable trends from looking at the data above include:

1. Latitude and temperature do appear to have a relationship. As you can see in the plot labeled "City Latitude vs. City Max Temperature", you can citys with a latitude closer to zero have a higher temperature, and as the latitude increases and goes further from zero, the temperature decreases. This makes sense since zero represents the equator, so the temperature would be higher.

![GitHub Logo](/Images/latitude_vs_temp.png)

2. Looking at the plot, "City Latitude vs. City Cloudiness", there seems to be no relationship between latitude and city cloudiness as the data points are all over the plot. 

![GitHub Logo](/Images/latitude_vs_cloudiness.png)

3. When you look at the northern and southern hemisphere plots comparing wind speed (mph) to latitude, the northern hemisphere has a cluster of datapoints below 15 mph, where the southern hemisphere is slightly more spread out.

![GitHub Logo](/Images/northernhem_windspeed_vs_lat.png)

![GitHub Logo](/Images/southernhem_windspeed_vs_lat.png)