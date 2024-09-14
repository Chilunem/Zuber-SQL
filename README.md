# Zuber-SQL
Exploratory data analysis and investigation of whether the duration of rides from the Loop to O'Hare International Airport changes on rainy Saturdays.


Table of Contents for README

Section Title	Description
DATA	Describes the source of data, included files, tables, and fields.
Description	Describes the final product's purpose, software, format, and included visuals.
Assumptions	Describes assumptions to include given by TripleTen and assumptions made based on the data and task.
Process	A general outline of how this project formed from start to finish.
Findings	Insights learned from the data analysis.

Data

A database with info on taxi rides in Chicago provided by TripleTen:

'neighborhoods' table: data on city neighborhoods
'name': name of the neighborhood
'neighborhood_id': neighborhood code
'cabs' table: data on taxis
'cab_id': vehicle code
'vehicle_id': the vehicle's technical ID
'company_name': the company that owns the vehicle
'trips' table: data on rides
'trip_id': ride code
'cab_id': code of the vehicle operating the ride
'start_ts': date and time of the beginning of the ride (time rounded to the hour)
'end_ts': date and time of the end of the ride (time rounded to the hour)
'duration_seconds': ride duration in seconds
'distance_miles': ride distance in miles
'pickup_location_id': pickup neighborhood code
'dropoff_location_id': dropoff neighborhood code
'weather_records' table: data on weather
'record_id': weather record code
'ts': record date and time (time rounded to the hour)
'temperature': temperature when the record was taken
'description': a brief description of weather conditions, e.g. "light rain" or "scattered clouds"

Description:

6 Step SQL query.
Exploratory data analysis and investigation of whether the duration of rides from the Loop to O'Hare International Airport changes on rainy Saturdays.

Assumptions:

There isn't a direct connection between the trips table and weather_records table in the database.
neighborhood_id is the Primary Key for the neighborhoods table.
cab_id is the Primary Key for the cabs table.
trip_id is the Primary Key for the trips table.
record_id is the Primary Key for the weather_records table.

Process:

Analyzed taxi rides by the company for specific dates, sorting by trip count. Analyzed rides for companies containing specific keywords, grouping by company name. Retrieved neighborhood IDs for O'Hare and Loop. Categorized weather conditions by hour. Retrieved Saturday rides from Loop to O'Hare, including weather and duration. Sorted the results.

Findings:

The taxi company "Flash Cab" had the highest number of taxi rides for Nov. 15th-16th, 2017 at 19,558 trips.
When searching SQL for a taxi company that contains the keyword "Yellow" or "Blue": The taxi company "Blue Diamond" had the highest number of taxi rides for Nov. 1st-7th, 2017 at 6,764 trips.
When comparing the two most popular taxi companies "Flash Cab" and "Taxi Affiliation Services" with all other available companies for Nov. 1st - 7th, 2017; The total number of taxi rides from "Other" is significantly higher than each top company separate or combined.
The SQL "neighborhood_id" identifiers of the O'Hare and Loop neighborhoods are ID # 63 and 50 respectively.
Each hour had been given a designated weather condition, starting with a Good designation.
A SQL table was printed to show all rides that started in the Loop on a Saturday and ended at O'Hare. Tables included Start time, weather conditions, and duration.
