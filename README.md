# Ford-GoBike-System-Data-Time-Series-and-Users
Investigation Overview This presentation is interested in showing the bike demands; when and from who the major demands are coming from? Trying to answer the question,when, will push us to time series analysis.


Dataset Overview

Our dataset consists on 183213 sample trips with 14 features (duration_hr, start_time, end_time, start_station_id, start_station_name, end_station_id, end_station_name, bike_id, user_type, member_age, member_gender, bike_share_for_all_trip, distance_km, age_group).

This is the cleaned version of 201902-fordgobike-tripdata.csv which originally contained 183412 sample trips with 16 features (duration_sec, start_time, end_time, start_station_id, start_station_name, start_station_latitude, start_station_longitude, end_station_id, end_station_name, end_station_latitude, end_station_longitude, bike_id, user_type, member_birth_year, member_gender, bike_share_for_all_trip)

We cleaned missing values in start_station_id start_station_name end_station_id end_station_name, member_birth_year and member_gender features, corrected a wrong member_birth_yaer entry, converted start_time, end_time, bike_id, start_station_id, end_station_id and member_birth_year to their appropriate datatypes. We also calculated distance from start_station_latitude, start_station_longitude,end_station_latitude and end_station_longitude features and dropped them. We converted duration_sec to duration_hr, member_birth_year to age and created age_group from age.

Riders Age Group Distribution

Approximately 2% of our demands came from people above 60years and 94% from people below 60years with the higest percentage coming from those between the age of 18-39. The age group of about 5% of total demand is unknown, they represents those that their member_birth_year were not filled.

age_group Counts ---  Energetic(18-39) : 134318; Ageing(40-60) : 37104; unidentified : 8263; Above 60 : 3529; 
age_group percentage ---  Energetic(18-39) : 73.31%; Ageing(40-60) : 20.25%; unidentified : 4.51%; Above 60 : 1.93%; 

Days with higest bike rides
More trips occured from Tuesday to Friday with Thursday as the highest while Monday, Saturday and Sunday had the lowest trips


The busiest time of the day
We can see a gradual raise in the graph as early as 4am reaching it's first peak by 8am. If we should place a line at 15000KM, we will see clearly the busiest hours are 7am - 9am and 4pm - 7pm. Bearing in mind that the majority of the users are within the age of 18-39 and 40-60 which could be called the working/business class, one could argue that the busiest hours are actually the time they should be going to work/ventures (7am - 9am) and when they should be returning home (4pm - 7pm)

