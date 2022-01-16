# Weather Analysis

This directory is divided into two parts. Part I contains a jupyter notebook which analyses the weather patterns of 671 cities from around the world of varying distance from the equator. Part II contains a juptyer notebook which uses Google Maps to generate a humidity heatmap of all cities listed in Part I, and also displays hotels in cities which meet my ideal weather for a vacation.

### Part 1

From the analysis of weather patterns from 671 randomly chosen cities, the following four observation were found:
#### Observation 1: There is a relatively strong relationship between a city's temperature and it's distance from the equator.
Several of the figures show that city temperatures increase the closer they are to the equator. For instance Figure 5 shows that there is a strong negative correlation between maximum temperature and latitude for cities located within the Northern hemisphere (-0.81), while Figure 6 shows a slightly weaker but still strong positive relationship between maximum temperature and latitude for cities located within the Southern hemisphere (0.76). This may be because the equator always gets the most amount of direct sunlight (and thus warmth) of any place on the planet.

![figure 5](WeatherPy/output/Part-1/figure-5.png)

![figure 6](output/Part 1/figure-6.PNG)

<br>

#### Observation 2: There is a very weak relationship between a city's wind speed and it's distance from the equator.
The data shows that there is a weak relationship between a city's wind speed and it's distance from the equator and that this relationship differs in both strength and direction depending on the hemisphere. For instance Figure 11 shows a very weak positive relationship between wind speed (mph) and latitude for cities located within the Northern hemisphere (0.09), while Figure 12 shows a slightly weaker opposite relationship between wind speed (mph) and latitude for cities located within the Southern hemisphere (-0.08).
![figure 11](output/Part 1/figure-11.PNG)

![figure 12](output/Part 1/figure-12.PNG)

<br>

#### Observation 3: There is a very weak relationship between a city's cloudiness and it's distance from the equator.
The data shows that there is a weak relationship between a city's cloudiness and it's distance from the equator and that this relationship differs slightly in strength depending on the hemisphere. For instance Figure 9 shows a very weak positive relationship between cloudiness (%) and latitude for cities located within the Northern hemisphere (0.03), while Figure 10 shows a slightly stronger positive relationship between cloudiness (%) and latitude for cities located within the Southern hemisphere (0.13).
![figure 9](output/Part 1/figure-9.PNG)

![figure 10](output/Part 1/figure-10.PNG)

<br>

#### Observation 4: There is a very weak relationship between a city's humidity and it's distance from the equator.
The data shows that there is a weak relationship between a city's humidity and it's distance from the equator and that this relationship differs slightly in strength and direction depending on the hemisphere. For instance Figure 7 shows a very weak positive relationship between humidity (%) and latitude for cities located within the Northern hemisphere (0.04), while Figure 8 shows a slightly weaker negative relationship between humidity (%) and latitude for cities located within the Southern hemisphere (-0.02). This difference may be because there is more land to heat up in the northern hemisphere which causes the air to become slightly warmer and thus more humid.
![figure 7](output/Part 1/figure-7.PNG)

![figure 8](output/Part 1/figure-8.PNG)

<br>

### Part II 

I created a heat map that displays the humidity for every city from Part I, which also has markers for all the cities which fit my ideal vaction weather data of 
- A max temperature lower than 80 degrees but higher than 70.
- Wind speed less than 10 mph.
- Zero cloudiness.

![vacation heatmap](output/Part 2/city-hotel-heatmap.PNG)

## Tools/Packages used:
- OpenWeatherAPI
- Python
  - Pandas
  - Matplotlib
  - Citipy
  - Gmaps

## How to use
- Download the directory.
- Go to openweathermap.org and follow these [instructions](https://openweathermap.org/appid) to get your API key.
- Go to Google Developers and follow these [instructions](https://developers.google.com/maps/documentation/embed/get-api-key) to get your API key.
- Go to the [API keys config file](WeatherPy/api_keys.py) and enter your OpenWeatherMap API key in the `weather_api_key` variable and your Google API key in the `g_key` variable.
- Open the WeatherPy folder and then open Git Bash and type `jupyter notebook` to see either notebook.
