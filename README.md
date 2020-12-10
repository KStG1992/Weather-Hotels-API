# Python API - What's the Weather Like?

## General Background

This script visualizes the current weather of 500+ cities across the world. Using Google Maps, a heatmap of each city's humidity is then created. To further customize the map, the program will look through the dataset and grab the "ideal" weather conditions for a perfect vacation. To help plan the vacation, the closest hotel is plotted over the heatmap. 

### Generating Cities Background

This script randomly generates a city and its corresponding coordinates by importing a module called CityPy.

### Calling Weather Data Background

Once the list of cities are generated, OpenWeatherMap is used to make a series of successive API calls for each city. The types of weather data retrieved are: Max Temperature, Wind Speed, Humidity, and Cloud Coverage. (NOTE: The units in this script are set to Imperial.)

There is a section in this project that retrieves the cities with ideal weather conditions. In this projection, ideal weather conditions are defined as follows:

    * Max Temperature lower than 80 degrees, but higher than 70.

    * Wind speed less than 10 mph.

    * Zero cloudiness.
    
### Generating Hotels Background

Once the ideal weather conditions are set, Google Places API is then used to find the first hotel for each idea city within 5000 meters. 


## Folders

In this repository you will find three main folders:
    * `output_data` - Contains 5 files: 1 CSV and 4 PNGs
    * `VacationPy` - Contains 1 Jupyter Notebook Script 
    * `WeatherPy` - Contains 1 Jupyter Notebook Script
    
### Output Data

* [cities.csv](output_data/cities.csv) - 500+ cities and the current weather conditions. 

* [Fig1.png](output_data/Fig1.png) - Temperature vs Latitude Plot

* [Fig2.png](output_data/Fig2.png) - Humidity vs Latitude Plot

* [Fig3.png](output_data/Fig3.png) - Cloudiness vs Latitude Plot

* [Fig4.png](output_data/Fig4.png) - Wind Speed vs Latitude Plot

### WeatherPy

* [WeatherPy.ipynb](WeatherPy/WeatherPy.ipynb):

In this script you will find the following data:

    * Length of Cities List
    * Print Log of Each City Being Processed
    * DataFrame with Cities and their weather
    * Creating CSV File
    * Inspecting Data for Humidity Over 100%
    * Four Plots of Temperature, Humidity, Cloudiness, and Wind Speed vs. Latitude
    * Four Linear Regression Plots of Temperature, Humidity, Cloudiness, and Wind Speed vs.       Northern Latitudes
    * Four Linear Repression Plots of Temperature, Humidity, Cloudiness, and Wind Speed vs.       Southern Latitudes

### VacationPy

* [VacationPy.ipynb](VacationPy/VacationPy.ipynb):

In this script you will find the following data: 

    * Humidity HeatMap
    * DataFrame of Cities with Ideal Weather Conditions
    * DataFrame with the Closest Hotel in Ideal Cities
    * Plotting Hotel Locations Over Humidity HeatMap
    * Clickable Markers with Display Info Box

