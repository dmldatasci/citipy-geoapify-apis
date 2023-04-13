# python-api-challenge
Module 6 submission for UC Berkeley data science bootcamp.

The `WeatherPy.ipynb` notebook generates random latitude/longitude combinations and uses the `citipy` library to find the closest cities to those locations. Using those city names, the OpenWeatherMap API is used to retrieve geocoding information and weather data. Regression analysis is used to fit a simple first degree polynomial model to Northern and Southern hemisphere relationships between latitude and a variety of weather attributes in the cities of interest.

The `VacationPy.ipynb` notebook maps the collected city data with humidity scaling marker size. Then, ideal weather condition preferences are used to restrict the data frame to a handful of viable vacation options. The Geoapify API is used to retrieve the closest hotel within 10,000 meters of the latitude/longitude retrieved for each relevant city. The same map is generated with the additional hotel information, restricted to ideal locations.

Maps generated with the `hvplot` library did not appear top render in GitHub, despite the fact that they do render in the Jupyter notebooks themselves. As such, maps were saved to HTML files in the `output_data` directory along with other relevant graphical and textual outputs.