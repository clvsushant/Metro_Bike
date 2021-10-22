# LA Metro BikeShare 

The Metro Bike Share system makes bikes available 24/7, 365 days a year in Downtown LA, Central LA, North Hollywood and the Westside. Metro Bike Share offers convenient round-the-clock access to a fleet of bicycles for short trips. Metro Bike Share is one of LA Metro's multiple public transportation options for Angelenos and visitors to get around.


![metro_bike](https://github.com/aclao89/LA_Metro_Bike/blob/master/Images/DSC01282-1600x885.jpg)

I analyzed consumer behavior in terms of membership types, volumes of trips by day, monthly, popular routes and visualizations in the Greater Los Angeles area in 2017. Based on these findings, I can provide meaningful data to adjust station locations, number of bike availablity, popular routes taken, and popularity by month/day to improve usability and customer satisfaction. 


                                                        Exploration Questions
                                                        
 
 What is the distribution of membership types? 
 
 ![memberships](https://github.com/aclao89/LA_Metro_Bike/blob/master/Images/membership_types.png)
 
 63.4% of their membership base are monthly subscribers. 29.3% are walk-ups meaning customers just purchase on the spot without any membership enrollment. Generally, a company profits when their most of their customers have a subscription-based membership.
 
 
 Which day has the longest average trip duration?
 
 ![avg duration](https://github.com/aclao89/LA_Metro_Bike/blob/master/Images/avg_trip_duration_by_day.png)
 
 Sunday had the highest average duration of a trip. According to the total volume of rides by day, Sunday had the least amount.It's possible that customers are just taking longer trips or more traffic that contributes to the higher duration.
 
 
 Which day has the most volume of trips?
 
 
 ![daily_trips](https://github.com/aclao89/LA_Metro_Bike/blob/master/Images/daily_trips_by_week.png)
 
 It's not suprising to see that the highest trip volume is on Friday. 
 
 
 Which month has the most volume of trips? 
 
 ![monthly trips](
https://github.com/aclao89/LA_Metro_Bike/blob/master/Images/monthly_trips_2017.png)

The highest number of trips were during October 2017. This high volumn of trips might be related to the moderate weather (72°), tourism, and possibly school commute. It's expected to have a low volume during the cold winter months of January and February and steadily increase as Spring arrives.

 
 
 What are the most popular routes taken?
 
 ![popular routes](https://github.com/aclao89/LA_Metro_Bike/blob/master/Images/top_50_routes.png) 
 
 
 
 Ocean Front Walk & Navy is in Venice Beach, a popular location for locals and tourists alike especially via bikes. Based on this chart, riders seem to take round trips in this area, perhaps it is near establishments. 
 
 


                                                        Data Format Overview
Total rides in 2017: 229,255

Columns: 14 

Total rides after removing rows with N/A values: 225,034


Each .csv file contains data for one quarter of the year. Each file contains the following data points:

                                                        Trip Information

trip_id: Locally unique integer that identifies the trip

duration: Length of trip in minutes (it is actually in seconds once I cleaned table)

start_time: The date/time when the trip began, presented in ISO 8601 format in local time

end_time: The date/time when the trip ended, presented in ISO 8601 format in local time

start_station: The station ID where the trip originated (for station name and more information on each station see the Station Table)

start_lat: The latitude of the station where the trip originated

start_lon: The longitude of the station where the trip originated

end_station: The station ID where the trip terminated (for station name and more information on each station see the Station Table)

end_lat: The latitude of the station where the trip terminated

end_lon: The longitude of the station where the trip terminated

bike_id:  Locally unique integer that identifies the bike

plan_duration: The number of days that the plan the passholder is using entitles them to ride; 0 is used for a single ride plan (Walk-up)
trip_route_category: "Round Trip" for trips starting and ending at the same station or "One Way" for all other trips

passholder_type: The name of the passholder's plan

bike_type: The kind of bike used on the trip, including standard pedal-powered bikes, electric assist bikes, or smart bikes.


                                                        Station Information

Data Format
Station ID: Unique integer that identifies the station (this is the same ID used in the Trips and Station Status data)

Station Name: The public name of the station. "Virtual Station" is used by staff to check in or check out a bike remotely for a special
event or in a situation in which a bike could not otherwise be checked in or out to a station.

Go live date: The date that the station was first available

Region: The municipality or area where a station is located, includes DTLA (Downtown LA), Pasadena, Port of LA, Venice

Status: "Active" for stations available or "Inactive" for stations that are not available as of the latest update

      
 
 
Source: 2017 Annual Trips & Stations Datasets https://bikeshare.metro.net/about/data/
