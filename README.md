# python-api-challenge
In this challenge we use Python requests, APIs, and JSON traversals to answer a fundamental question: "What is the weather like as we approach the equator?"

The obvious answer is "It gets hotter.” But, if pressed for more information, how would you prove that?

## Instructions
This activity is broken down into two deliverables, WeatherPy and VacationPy.

### Part 1: WeatherPy
Create a Python script to visualise the weather of over 500 cities of varying distances from the equator.
1. Generate random geographic coordinates and find the nearest city to each latitude and longitude combination using the [citipy Python library](https://pypi.org/project/citipy/).
2. Next, the [OpenWeatherMap API](https://openweathermap.org/api) is used to retrieve waether data for each city.
3. Create a series of scatter plots to display the following relationships:
   -  Latitude vs. Temperature
   -  Latitude vs. Humidity
   -  Latitude vs. Cloudiness
   -  Latitude vs. Wind Speed
4. Separate the plots above into Northern and Southern hemispheres, then calculate the linear regression for each.

Linear regression is used to derive correlation beetween latitude and different weather attributes i.e. how the weather changes (or doesn't) depending on proximity to the equator?

### Part 2: VacationPy
Show how weather data can be used to plan future vacations using the [Geoapify API](https://www.geoapify.com/) and the [geoViews Python library](https://geoviews.org/).
1. Create a map that displays a point for every city in the `city_data_df`
2. Narrow down the city_data_df DataFrame to find your ideal weather condition. For example:
   - A max temperature lower than 27 degrees but higher than 20
   - Wind speed less than 4.5 m/s
   - Cloudiness is less than 5
   - The main objective is to limit the dataframe to 10-20 rows.
3. Create a new DataFrame called hotel_df to store the city, country, coordinates, and humidity based on the shortlisted cities from the step above
4. For each city, use the Geoapify API to find the first hotel located within 10,000 metres of your coordinates.
5. Add the hotel name and the country as additional information in the hover message for each city in the map as in the following image:

## How to execute code?
1. Create api_keys.py at the same location as these jupyter notebooks.
2. Assign your OpenWeatherMap API key to "weather_api_key" variable.
3. Assign your Geoapify API key to "geoapify_key" variable.
4. Run `WeatherPy.ipynb` to collect and store weather data from approximately 550-650 cities around the world using randomly generated coordinates. **API keys will be required for Geoapify and OpenWeather App**.
5. Graphs created by `WeatherPy.ipynb` will be stored in `output_data`.
6. `VacationPy.ipynb` should be run after `WeatherPy.ipynb` as it is dependent on the data collected by latter.

## References
- **citipy Python Library** https://pypi.org/project/citipy/
- **OpenWeatherMap API** https://openweathermap.org/api
- **Geoapify API** https://www.geoapify.com/
- **geoViews Python Library** https://geoviews.org/
