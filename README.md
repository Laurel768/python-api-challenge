# python-api-challenge

Python API Homework - What's the Weather Like?

This project examines weather in different parts of the world to answer the question:   "What's the weather like as we approach the equator?"

First, we created a Python script to visualize the weather of over 500 randomized cities across the world of varying distance from the equator. 
We utilized a simple Python library (https://pypi.python.org/pypi/citipy) and the OpenWeatherMap API (https://openweathermap.org/api) to create a representative model of weather across world cities.

We created some scatter plots to examine relationships between weather variables:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude


We ran a linear regression on each relationship, only this time separating them into Northern and Southern Hemispheres:

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

After each pair of plots explain what the linear regression is modeling such as any relationships you notice and any other analysis you may have.

Your final notebook must:

* Randomly select **at least** 500 unique (non-repeat) cities based on latitude and longitude.
* Perform a weather check on each of the cities using a series of successive API calls.
* Include a print log of each city as it's being processed with the city number and city name.
* Save a CSV of all retrieved data and a PNG image for each scatter plot.

### Part II - VacationPy

We took the data from Part I and created a heat map that displays the humidity for every city.
Using jupyter-gmaps and Google Places API, we narrowed down a list of cities to find ideal weather conditions.

We looked at cities with a wind speed less than 6 mph.
We removed any cities with a temperature higher than 85 degrees F.
We selected cities with a humidity less than 35%.

We were left with 10 cool, dry, cities.

Menongue, Angola
Viedma, Argentina
Sarakhs, Iran
Tikrit, Iraq
Bilma, Niger
Faya, Saudi Arabia
Sakakah, Saudi Arabia
Abha, Saudi Arabia
Viransehir, Turkey
Zambezi, Zambia

While these cities may not be on everyone's bucket list, they represent the ideal weather we selected.  These 10 cities are at least 14 degrees away from the equator.

It was surprising to see so many countries in Africa and the Middle East.  One usually thinks of these places as hot.  
And yes, there are times of the year when the temperature is quite high, however, our data was collected on one day in October.
These cities have low humidity, which can be quite pleasant.  None of these cities were chosen as tourist hotspots, just cities with pleasant weather.

