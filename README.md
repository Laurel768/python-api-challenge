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

There is a definite relationshiop between temperature and latitude.  The weather is warmer closer to the equator (Latitude = 0).  This is due to the shape of Earth.  
Earth is widest at the equator.  Even though the Earth rotates on a slightly tilted axis, the widest part of the planet is always closer to the sun than the poles, which are the most narrow.
Closer to the sun means warmer temperatures, even at night.

Humidity is the presence of water vapor in the atmosphere.  When water evaporates, it rises into the air, and the air becomes more humid. 
Hot places tend to be more humid than cool places because water evaporates faster in warm weather.
I would have expected to see more pronounced results in this graph, but the humidity seems to be all over the place.  This could be because there just isn't a lot of water vapor in certain areas.

Clouds are also caused by water vapor, so I would expect to see less clouds where there is less humidity.  Much like the humidity chart, cloudiness seems to have little correlation to latitude.

Wind speed is caused by atmospheric pressure, not latitude and this graph illustrates the wide variety of wind speeds over latitudes.


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

In the Northern Hemisphere, the linear regression for temp vs. latitude is illustrating how the temperature is highest closest to the equator and drops as you move away from the equator towards the North Pole.
The Southern Hemisphere linear regression shows the same, with weather coldest closest to the South Pole, increasing as you move closer to the equator.

The linear regression for humidity vs. latitude shows humidity slightly increasing as you move north of the equator. 
However, the Southern Hemisphere shows humidity increasing as you move towards the equator.
We have to take into consideration that our data is from the month of October.  While the northern hemisphere is going through the fall season, the southern hemisphere is going through spring.
Humidity can be affected by how much water is present (oceans, lakes) and also topography (mountains, valleys).

Our linear regression for clouds vs. latitude seem to indicate that cloudiness increases as you move north of the equator, and increases as you move south of the equator.
The amount of data scattered on these graphs indicate that there are other factors affecting clouds.  
Again, we need to remember that the southern hemisphere is heading into summer, and we would expect sunnier days.

The linear regression for wind speed shows wind speed increasing as you move away from the equator, either north or south.
However wind speeds varied from 0 - 25 mph.  
I would recommend a more in-depth study of wind, with data being collected at multiple times during the day and averaged, and also on multiple days throughout the year.
These graphs don't really show a strong correlation between wind speed and latitude. 

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

