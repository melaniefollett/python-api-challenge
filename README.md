# Weather Analysis Using Python and APIs

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So I took my knowledge of Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"  The obvious answer is "the temperature increases" but I wanted to prove it.

# Part I: WeatherPy
For this project I created a Python script to visualize the weather of 500+ random cities across the world of varying distance from the equator (WeatherPy.ipynb). To accomplish this, I utilized a simple Python library, the OpenWeatherMap API, and a little common sense to create a representative model of weather across world cities.

My first objective was to build a series of scatter plots to showcase the following relationships:
- Temperature (F) vs. Latitude
- Humidity (%) vs. Latitude
- Cloudiness (%) vs. Latitude
- Wind Speed (mph) vs. Latitude

My next objective was to run linear regressions on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

Overall I determined that there is a relationship between latitude and temperature, particularly in the Northern Hemisphere with temperature increasing as latitude decreases (ie. gets closer to the equator).  Please see my written report (WeatherPyReport.docx) for a more indepth analysis of my findings.


# Part 2: VacationPy
Next I used my skills in working with weather data to plan future vacations. I used jupyter-gmaps and the Google Places API for this part of the project.  First I createed a heat map that displays the humidity for every city from Part 1 of the project.

I filtered the DataFrame to find my ideal weather condition. Specifically:
- A max temperature lower than 80 degrees but higher than 70.
- Wind speed less than 10 mph.
- Zero cloudiness.
I dropped any rows that didn't contain all three conditions to ensure ideal weather.

Next, I used Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.  Then I plotted the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.

# Tools/Technologies Used
- Python/Pandas
- Matplotlib
- Google Places API
