# Ford GoBike Dataset Exploration
## by Johnpaul Kosisochukwu Nwagwu


## Dataset

>The Ford GoBike Dataset contains approximately 183,000 entries of individual rides made in a bike sharing system in Greater SanFrancisco Bay area. The data set can be found here https://video.udacity-data.com/topher/2020/October/5f91cf38_201902-fordgobike-tripdata/201902-fordgobike-tripdata.csv. We will explore important features such as duration_sec, start_hour, end_hour, member_gender, user_type and start_dayname among others. Some of these features were extracted from existing variables. 

>Data Warngling performed include 
    Change start time to date time type and split to day, dayname, month and year columns
    Change end time to date time type and split to day, dayname, month and year columns

> After wrangling, I started with univariate analysis, then bivariate analysis and multivariate analysis. The summary of my findings are documented in these stages

## Summary of Findings

#### Univariate Analysis
> looking at the start month and start year columns, we see that Data collected was for the month of February and the year 2019. 
> Next, we proceed to look at the start day column and we see that The top five most travelled days in February are 28th, 20th, 21st, 19th and 7th. This doesn't provide too much insight so we extract a new column called daynames.
> The daynames column gives us vital information, Most trips were made on thursdays with over 35000 trips with the least trips made on weekends(Saturdays and Sundays) of about 15,000.

> Moving onto the end year and month columns we discover that month of march appears in the month column. odd as the start month only has February. Upon further investigation, we realize that Some trips started on 28th February and ended on March 1. 

> We notice that Trips of up to 80,000 seconds were recorded in a few instances were recorded in the trip duration column and The distribution of the trip duration is right skewed with most trips lasting about 400 to 500 seconds
> looking at our user type column, we see that Majority of users in our data are subscribers with more than 70%
> Looking at the start and end hour columns, the Top 5 Most travelled times are 5pm, 8am, 6pm, 9am and 4pm.
> We also notice from the start and end time columns that Aside work travel hours, afternoon trips are more common, followed by late night trips and then early morning trips
> About 80% of trips were individual trips(not shared)
> Looking at the gender column, Male users were more than twice as large as female users
> Outlier present in member birth year. Graph of memeber birth year is left skewed with the most frequent age bracket between 19 and 39 years
> We observe that Start stations id 58 and 67 were the most visited stations.
> and also Most trips started in station ids 58, 67, 81, 21 and 3 and ended in station ids 67, 58, 21, 15 and 3 while 
> The least 5 visited station are station ids 244, 244, 301, 300 and 51

#### Bivariate Analysis
> As we suspected during our initial exploration, the start hours and end hours of trips in our data show a strong linear relationship with     one another
> Start and end hours also shows a somewhat positive correlation with trip duration

> Interestingly, Despite the number of subscribers being more than double the size of customers as seen previously, they boast similar start hours on average as compared with the Subscribers but they have thinner interquartile range for the end hours.

> For the Gender of individuals on gobike data, we see than the male and female have about the same mean value for start and end hours desquite the frequency of males being more than half of the females in the data(gender imbalance).

> Finally, as expected the box plots for both the end hours and start hours of the bike share trip for all trip are the same since they are for the same trip

> Looking at the start day names and end day names distribution against start and end hours, we see that outliers are present on Saturdays and Sundays(midnight/very early morning trips). This gives us an idea that early morning and late night trips perhaps are more common in weekends

> All shared trips are by Suscribers only

> Users whose gender is other are all Subscribers

> Most of the trips are individual trips and not shared

#### Multivariate Analysis

> Interesting insights, So in general for hours between 4:00 and 21:00, The Customers spend more time travelling than the subscribers with the peak travel time being between 11:00 and 15:00 of less than 1100 seconds. The Suscribers peak travel duration is almost constant at about 600 seconds

> we see that subscribers boast greater travel duration for hours between 0:00 and 4:00 when compared to customers, the peak travel time for customers is about 3000 seconds and the peak travel duration for customers ia a little about 2500 seconds and there are more subscriber trips on an average when compared to the customers

> Here we see that for hours between 21:00 and 24:00, the customers have more trips on an average than the subscribers although the different doesn't appear very significant at first glance. More 23:00 hour trips are common.


## Key Insights for Presentation


> The distribution of the trip duration is right skewed with most trips lasting about 300 to 700 seconds.There also appears to trip lengths are big as 80,000 seconds

> Most trips were made on thursdays with over 35000 trips with the least trip of about 15,000 made on weekends(Saturdays and Sundays) 

> More than 80% of users in our data are subscribers. We have over 160,000 susbcribers abnd about 20,000 customers

> We see that the top 5 Most travelled hours are 17:00, 8:00, 18:00, 9:00 and 16:00. These are work trip times. Also, the least trips are taken in the early hours of the morning and midnight

> We can see that about 90% of trips were individual trips(not shared)

> We can see that all shared trips are by Suscribers only

> Interesting insights, So in general for hours between 4:00 and 21:00, The Customers spend more time travelling than the subscribers with the peak travel time being between 11:00 and 15:00 and less than 1100 seconds. The Suscribers peak travel duration is almost constant at about 600 seconds