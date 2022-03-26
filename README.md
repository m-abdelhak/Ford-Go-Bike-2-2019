# Ford-Go-Bike-2-2019
This data set includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area.
And the target from that wrangling effort is to detect the week and strong points in service performance to help development team to take the right decisions to increase company performance and profit.
By exploring our data set we found that we have 15 columns in it, each record is for a one bike ride information, like location and time of start and end, ride duration, and some personal information about the rider (year of birth and gender), and another information about the service he got.
We found that we have missing values in the following columns:
1-	"start_station_id"
2-	"start_station_name"
3-	"end_station_id"
4-	"end_station_name"
although they have a latitude and longitude
also, we have missing values in:
5-	"member_birth_year"
6-	"member_gender"
So, I decided to give a generic name and Id for all missing ones, but firstly try to find if I have already a station with the same location and have an ID to put in the missing field, but if I not found, I should create one.
Then I have a chart showing stations locations like a map, and I found that it seems to have four main zones, so I made a function to generate a Zone column to the data set, and check what is the activities across zones. And I found that it is very very low, so I proceed with that, and then add a counter for station appearing in the data set, to show the most active stations and most active zone.
It seems that the highest activities is for Zone #4, then for Zone #3, then Zone #1, and Zone #2 has a very low activity, also as traveling between zone have very low activity, so our zone separation is meaningful.
Then I want to check the most active track, and I choose 50 times appearance in the data set to be the lower limit for the most active station.
Then I want to study bikes activity, to get the most preferred bikes specs, and data shows that bikes Ids from 4500 to 5500 has the most preferred specs, that reflected in their count of using and duration, company may buy more from those types to increase performance.
Then I convert the start time column to some columns show its needed components, and noticed that the activities are low in weekends (Sat., & Sun.), but day (13, wed., Feb) has a low activity, although it is the day before what is called in America "Valentine's Day", so it may has a relation in getting low activities at that day.
Also, the busiest hours in the day are from (7 to 9 O'clock) and from (16 to 18 O'clock)
After that I checked the most common ages and the most common ride duration times, so I converted the year of birth to age column, and decide to put the missing data to have 150 years old to be obvious in the charts, and don’t loose their effect in data analysis, and I got the fact that the most common durations from 5.2 to 16.7 minutes, and the common ages are form 27 to 32 years.
Then I study the relation among 'user_type', 'member_gender', 'bike_share_for_all_trip' at the whole data set and at each Zone, and I got the following:
•	Customers are very high in Zone #2 compared with other Zones.
•	Males are the most gender type on each Zone, and Zone #1 have the most percent of Males.
•	Zone #1 is the highest in the 'bike_share_for_all_trip' 'Yes' value, and also is higher than 'No' value.
•	all customers have No bike share for all trip
•	Females have higher customers percentage than males.
Then I continue with studying ages distributions and ride durations for each Zone, and noticed that Zone #1 most common ages are below 35, and is the lowest, also Zone #4 has the highest percent of missing age data, that was opted to appear at 150 years.
By continue analysis I got the following:
•	Females have higher riding time in average than males
•	The most yes bike share are younger than the no ones.
•	Females and Males shares almost the same age distribution, but males have slightly higher older distribution than females.
•	Younger people tend to be customers than subscribers.
•	From (30 to 35) have the highest riding durations, and Zone #3 & #4 have the superiors
