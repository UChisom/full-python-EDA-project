# Ford GoBike System Data Exploration
## by Chisom Urom


## Dataset

The dataset consisted of 183412 individual bike rides made in a bike-sharing system covering the greater San Francisco Bay area. There were 16 variables including latitude and longitude positions for start and end stations. 

Following my wrangling process, I retained rows in the dataset, useful for my analysis and dropped some extraneous columns. For tidiness, I separated the dataset into two tables, one containing information on the user, and the other on the trip.

The dataset was provided by Udacity in the Data Analyst course and can be assessed [here](https://video.udacity-data.com/topher/2020/October/5f91cf38_201902-fordgobike-tripdata/201902-fordgobike-tripdata.csv). 
More data on additional cities can also be assessed on this github page [here](https://www.google.com/url?q=https://github.com/BetaNYC/Bike-Share-Data-Best-Practices/wiki/Bike-Share-Data-Systems&sa=D&source=editors&ust=1658742700929482&usg=AOvVaw2vYZ7-sONEyUEd006XOg0k)

The variablies inthe dataset are as follows:
- Trip Duration (seconds)
- Start Time and Date
- End Time and Date
- Start Station ID
- Start Station Name
- Start Station Latitude
- Start Station Longitude
- End Station ID
- End Station Name
- End Station Latitude
- End Station Longitude
- Bike ID
- User Type (Subscriber or Customer)


## Summary of Findings

>I found that the general trend in usage of the bike share system was was largely predicated on the user-type. As such, Customers generally took longer duration trips than Subscribers. 

>This was initially surprising for Customers to have longer average trip durations than Subscribers, but further analysis revealed that Subscribers were mostly using the service particularly for shorter durations than Customers. 
To obtain this relationship, I grouped the durations into Short, Medium, and Long trips in the following order:

- Miniumum duration to first quartile = `Short`
- First Quartile to third quartile = `Medium`
- Third quartile to maximum duration = `Long`

>Furthermore, I found that the peak periods of use varied by day of the week and time of the day, with more Subscribers using the service around the 8th and 17th hour on weekdays but not weekends. Customers however, had a smilar pattern by the hours of each day, but the distribution was more uniform over the hours of the day. 

>This was because Customers had slightly more use during off-peak hours on those weekdays. In my analysis of bike use by the genders, I discovered the Males had a predominant population, but had a similar proportion of subscribed users only marginally higher than Females and the Other genders. 

>Outside the main variables of interest, I also discovered that Thursday had the most trips taken, also, the most visted start and end stations were `Market St at 10th St` and `San Francisco Caltrain Station 2  (Townsend St at 4th St)` respectively.

>Similarly, I found that most users followed the route from `Berry St at 4th St` to `San Francisco Ferry Building (Harry Bridges Plaza)` stations, as it was the most frequent trip taken (Start to end).


## Key Insights for Presentation


>My focus for the visualisation will be to illustrate the effect of user type on the rate of bike use. Other variables to be featured in the explanatory slide include the time of day, day of the week and duration of use. I start by introducing the user type and distriution of the usage duration.

>Next, I'll represent the daily usage by user type in a clustered bar chart, then I'll show the hourly usage by the user types for the peak hours as well. I'll proceed to compare the average duration between the two user types before visualising the impacts of age and gender on bike use. To illustrate the impact of age, I'll be using a violin plot not present in my exploratory analysis.

>I'll concentarate on the user-type variable as it had the most effect on user behaviour in my analysis. The next visualisation willpresent the variations in bike use by Day of the week and hour for each user type. Finally, I'll plot the differences in trip duration for each user type on different days using a colour palette that depict increasing duration.

>Summarily, the type of user had the greatest impact on the use of the bike share system. These differences manifested in the following ways:
- The bike share service had more use by Subscribers but Customers type users has a higher average duration on trips.
- Thursday was the busiest day of the week for both Subscribers and Customers.
- Subscribers mostly used the bike share system at peak hours during the week days (at the 8th and 17th hour), while customers had a slightly more balanced used for different hour of the day.
- Weekend had a sudden decline in usage by subscribers and the peak hour became around the 14th hour of the day.
- Customer type users took more long duration trips than Subscribers. Even during the weekends, more customers took even more medium and long duration trips.
- Subscribers took more short and medium duration trips than long durations and mostly during weekdays.