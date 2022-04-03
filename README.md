# World_Weather_Analysis

## Overview

This analysis uses weather date from OpenWeatherMap's API and Google Maps's API to create maps to visualize a travel itinerary. 

The purpose of this repository is to hold three deliverables:
- Deliverable 1: Retrieve Weather Data
- Deliverable 2: Create a Customer Travel Destinations Map
- Deliverable 3: Create a Travel Itinerary Map

#### Deliverable 1: Retrieve Weather Data

I created a set of 2,000 random latitudes and longitudes. Then, using the `citypy` module, I got the nearest city to each latitude and longitude pair.
Then I performed an API call to OpenWeatherMap to retrieve the following information for each city: 
- latitude and longitude
- maximum temperature
- percent humidity
- percent cloudiness
- wind speed
- weather description (such as clouds, fog, light rain, clear sky, etc.)

I added this weather data to a DataFrame:

![city_data_df](https://github.com/stephperillo/World_Weather_Analysis/blob/main/Weather_Database/city_data_df.png)

#### Deliverable 2: Create a Customer Travel Destinations Map

Next I used input statements to retrieve customer weather preferences, then used those preferences to identify potential travel destinations and the hotel nearest to each city location. The preferences that we asked for are preferred minimum and maximum temperatures. I created a marker layer map with pop-up markers that displays the desired cities based on the desired temperature range.

This is an example of a map with a desired temperature range of 75 to 90 degrees Fahrenheit:

![WeatherPy_vacation_map.png](https://github.com/stephperillo/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png)

#### Deliverable 3: Create a Travel Itinerary Map

I used Google Directions API to create a potential itinerary for 4 cities in Brazil that met the desired temperature conditions previously set. I also created a marker layer map showing pop-up markers for each of the cities that displays the driving route for the itinerary. 

The cities on this itinerary are:
1. Touros
2. Natal
3. Cabedelo
4. Olinda

![Brazil_itinerary.png](https://github.com/stephperillo/World_Weather_Analysis/blob/main/Vacation_Itinerary/Brazil_itinerary.png)

Each city marker pops up with an information box containing the name of the closest hotel, the city and country name, and the current weather description. The markers can be opened individually to view each information box and one can zoom in or out of the map.

![WeatherPy_travel_map_markers.png](https://github.com/stephperillo/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map_markers.png)

This analysis can be used to filter and choose a number possible vacation destinations based on weather conditions.
