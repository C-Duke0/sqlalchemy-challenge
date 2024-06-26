# sqlalchemy-challenge
Instructions
Congratulations! You've decided to treat yourself to a long holiday vacation in Honolulu, Hawaii. To help with your trip planning, you decide to do a climate analysis about the area. The following sections outline the steps that you need to take to accomplish this task.
Part 1: Analyze and Explore the Climate Data
In this section, you’ll use Python and SQLAlchemy to do a basic climate analysis and data exploration of your climate database. Specifically, you’ll use SQLAlchemy ORM queries, Pandas, and Matplotlib. To do so, complete the following steps:
Precipitation Analysis
Find the most recent date in the dataset.
Using that date, get the previous 12 months of precipitation data by querying the previous 12 months of data.
Select only the "date" and "prcp" values.
Load the query results into a Pandas DataFrame. Explicitly set the column names.
Sort the DataFrame values by "date".
Plot the results by using the DataFrame plot method:
![Screenshot 2024-06-05 at 2 37 54 PM](https://github.com/C-Duke0/sqlalchemy-challenge/assets/162658233/8aa38747-b333-47be-87db-ffcdcbf25d21)
Station Analysis
Design a query to calculate the total number of stations in the dataset.
Design a query to find the most-active stations (that is, the stations that have the most rows). To do so, complete the following steps:
List the stations and observation counts in descending order.
Design a query that calculates the lowest, highest, and average temperatures that filters on the most-active station id found in the previous query.
Design a query to get the previous 12 months of temperature observation (TOBS) data. To do so, complete the following steps:
Filter by the station that has the greatest number of observations.
Query the previous 12 months of TOBS data for that station.
Plot the results as a histogram
![Screenshot 2024-06-05 at 2 38 21 PM](https://github.com/C-Duke0/sqlalchemy-challenge/assets/162658233/aec5dc9e-d4d5-477d-ab35-8b1eb32dbc9b)

Part 2: Design Your Climate App
Now that you’ve completed your initial analysis, you’ll design a Flask API based on the queries that you just developed. To do so, use Flask to create your routes as follows:
/api/v1.0/precipitation
Convert the query results from your precipitation analysis (i.e. retrieve only the last 12 months of data) to a dictionary using date as the key and prcp as the value.

/api/v1.0/stations
Return a JSON list of stations from the dataset.

/api/v1.0/tobs
Query the dates and temperature observations of the most-active station for the previous year of data.

/api/v1.0/<start> and /api/v1.0/<start>/<end>
Return a JSON list of the minimum temperature, the average temperature, and the maximum temperature for a specified start or start-end range.

For a specified start, calculate TMIN, TAVG, and TMAX for all the dates greater than or equal to the start date.

For a specified start date and end date, calculate TMIN, TAVG, and TMAX for the dates from the start date to the end date, inclusive.
