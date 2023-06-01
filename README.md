# citipy-geoapify-apis
A project exploring the `citipy` and `Geoapify` APIs to produce a dataset of randomized global cities and associated weather data.

## Procedure
This activity is broken down into two deliverables, WeatherPy and VacationPy.

#### Deliverable 1: WeatherPy
The `WeatherPy.ipynb` notebook generates random latitude/longitude combinations and uses the `citipy` library to find the closest cities to those locations. Using those city names, the OpenWeatherMap API is used to retrieve geocoding information and weather data. Regression analysis is used to fit a simple first degree polynomial model to Northern and Southern hemisphere relationships between latitude and a variety of weather attributes in the cities of interest.

**1. Create Plots to Showcase the Relationship Between Weather Variables and Latitude**
  - Use random generation techniques and the `citipy` API to create a random list of global cities.
  - Use the `OpenWeatherMap` API to retrieve weather data from the random cities list.
  - Create a series of scatter plots to showcase the following relationships:
    - _Latitude vs. Temperature_
    - _Latitude vs. Humidity_
    - _Latitude vs. Cloudiness_
    - _Latitude vs. Wind Speed_

    ![Latitude Scatterplots](images/latitude_scatterplots.png)

**2. Compute Linear Regression for Each Relationship**
- Compute the linear regression for each relationship.
- Separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude).
- Create a series of scatter plots including the linear regression line, the model's formula, and the $r$ values:
  - _Northern Hemisphere: Temperature vs. Latitude_
  - _Southern Hemisphere: Temperature vs. Latitude_
  
  ![Temperature Regression](images/temp_regressions.png)
  
  - _Northern Hemisphere: Humidity vs. Latitude_
  - _Southern Hemisphere: Humidity vs. Latitude_

  ![Humidity Regression](images/humidity_regressions.png)

  - _Northern Hemisphere: Cloudiness vs. Latitude_
  - _Southern Hemisphere: Cloudiness vs. Latitude_

  ![Cloudiness Regression](images/cloudiness_regressions.png)

  - _Northern Hemisphere: Wind Speed vs. Latitude_
  - _Southern Hemisphere: Wind Speed vs. Latitude_

  ![Wind Speed Regression](images/wind_speed_regressions.png)

#### Deliverable 2: VacationPy
**1. Map Cities with Markers Scaled by Humidity**
- Map the collected city data with marker size scaled by humidity.

![Vacation Candidate Cities](images/all_cities.png)

**2. Map Cities with Markers Scaled by Humidity**
- Use ideal weather condition preferences to restrict the cities data frame to a handful of viable vacation options.
  - _Maximum temperature greater than 22ºC_
  - _No cloudiness_ 
- Use the Geoapify API to retrieve the closest hotel within 10,000 meters of the latitude/longitude retrieved for each relevant city.
- Generate the same map as above, but restricted to ideal locations and with the hotel information added.

![Vacation Candidate Cities Filtered by Weather](images/ideal_weather.png)
