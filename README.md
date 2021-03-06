# PyBer Analysis Report
## Purpose
Pyber data was provided to create visualizations to help to understand the data easier.  The objective was to find correlations between the drivers count, ride counts and fares in different cities that are subdivided by city types: Urban, Suburban and Rural.  We will be using bubble charts, box plots, line charts, tables for the analysis to provide the information quickly and detect patterns, trends, correlations and outliners.  In this case Matplolib will be used to create the charts to visualize data from a Data Series or DataFrame.

## Background and Results
- The data includes two files: city_data and ride_data.  The city_data includes the city name, driver count by city and type of city.  The ride data includes city name per ride, date by ride, the fare for each ride and the ride id.  
- We inspected the data for NaN values, and analyze if the files can be merged.  Both data sets have the city name and was merged using this column creating a DataFrame.  
- Using the merged DataFrame we created 3 DataFrames for each type of city: Urban, Suburban and Rural, then we computed the number of rides, the average fare and driver counts per city for each DataFrame by city type.  
- We incorporated the data calculated in a bubble chart and show the Total Number of Rides (Per City) vs Average Fare.
- The mean, median and mode were calculated for rides, fare and drivers by city type using different methods like Pandas, Numpy and SciPy, and also the box plots were created for ride count, ride fare and driver count by city type.
- After getting the percentages of fares, rides and drivers by city type, we created a pie chart for each of the variables (fares, rides and drivers).
- For Challenge of Module 5:
  - Need to create a DataFrame that summarizes the key metrics for the ride-sharing data by city type.
  - Create a multiple-line chart, with one line for each city type, that shows the sum of the fares for each week.
  - Write a report with the results.


### Results from Module
- Bubble Chart: PyBer Ride-Sharing Data (2019)

![Fig1](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig1.png)

  - The bubble chart shows the total number of rides in the urban cities are higher, but cheaper comparing with the rural and suburban cities.  Urban cities have more than doble of the rides of the rural cities, but the fares in rural cities are more expensive comparing with the suburban and urban cities.

- Box Plots: 
  - Ride Count Data (2019)

  ![Fig2](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig2.png)

  The box plot shows the ride counts per city by city type.  Urban cities have 3 times of rides of rural cities, suburban cities has almost twice the rides of the rural cities.  The data for urban cities shows an outlier, but I will not remove it since the point is very close to the upper limit and more information will be needed to remove that point from the data.

  - Ride Fare Data (2019)

  ![Fig3](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig3.png)

  The box plot shows the ride fares by city type.  Rural fares show the highest fares for city type, and urban cities reported the lowest fares.  The rural fares are more spread out than the suburban and urban cities.  

  - Driver Count Data (2019)

  ![Fig4](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig4.png)

  - The box plot shows the driver count by city type.  Less drivers are needed for rural cities and urban cities have more drivers, but also depends on the city.  The number of drivers on some urban cities are almost 3 times the suburban cities and 7 times the rural cities.
  
- Percentage of Total Fares by City Type

  ![Fig5](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig5.png)

  - 62.7% of the total fares for the urban, suburban and rural cities are from urban cities, 30.5% came from suburban cities and rural cities has only 6.8% of the total fares.

- Percentage of Total Rides by City Type

  ![Fig6](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig6.png)

  - 68.4% of the total rides came from urban cities, suburban has 26.3% and rural only 5.3% of the total rides.
  
- Percentage of Total Drivers by City Type

  ![Fig7](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig7.png)
  
   - 80.9% of the total drivers correspond to the urban cities, suburban cities have 16.5% and rural cities 2.6%.
   
## Challenge 5 Results

- Technical Analysis 1: 
  - Create the series for total rides, total drivers and total fares by city type, then calculate the driver count by city type, the sum of the fares by city type and the average fare per ride.

  - Driver count by city count was calculated from the city_data_df, making a group by type then make a sum of the driver count.  Another way to make this calculation is taking the merged dataframe (pyber_data_df) and group by city and type them calculate the mean of driver count and group by the type again and make the sum.

  - The sum of the fares was calculated from the merged dataframe, making the group by type then making the sum of the fares.
  
  - The average fare per ride was computed making a group by type then an average of the fares.
  
  - After creating the series, we created the following dataframe:

  ![Summary Key Metrics DataFrame](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Summary%20Key%20Metrics%20DataFrame.JPG)

  - The table shows the rural cities have 13 more rides than the rural cities, and 2.6 more rides than suburban cities.  Since the rides are much higher for urban cities, the total drivers and total fares are also higher.  
  - Looking the average fare per ride and average fare per driver, help to predict if more or less drivers are needed, if the average fare per ride calculated represents the fare that should be charged per ride in the city.  Let's assumed the rural average fare per ride is close to the one that is supposed to be charged, so when you compare with the average fare per driver you know you will need more drivers to be closed to the average fare per ride.  But when you look the urban city type is the opposite, the average fare per driver is less than average fare per ride, this means there are more drivers than needed and this make to drop the fare.

- Technical Analysis 2:
- Multiple-line chart: Total Fare by City Type by week
  - We created a dataframe that has the fares by city types in a period of time 01/01/2019 to 04/28/2019.  Then the sum of the fares by city type was calculated per week.

  ![Fig8](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig8.png)
  
  - In general, urban cities have the higher accumulated fares. Comparing the lines for each city type, the suburban cities have about the doble of the rural fares, and the urban has the doble of the suburban fares.

### Summary
- In conclusion the urban cities have more drivers and rides than the suburban and rural cities, this also make the sum of fares to be higher.  Looks like there are more drivers that really needed in the urban cities, and more drivers are needed for rural and suburban cities.


### Challenges and Difficulties Encountered

* Programming:
  - I almost could not do the calculation per week of the fares in the pivot table for the Technical Analysis 2.  I was using the correct formatting but I was getting an error.  After looking and use google, finally I noticed the issue was the time was reading as an object, so I had to change the data type for the time, after that the calculation worked.
  - It was hard to figure it out the syntax to copy only 2 columns from a dataframe. Using google and support from TA solve my issue.

* Data analysis
  - When we merged the 2 data set provided using the city, the driver count does not make sense, because the city_data file has 120 cities and driver count by each city, when we merged the data sets, the driver count is assigned to the cities of the file ride_data, this file was made by ride id and has 2375 rows, and the cities are the same 120 cities from city_data file, so if the city was repeated twice on the ride_data file, the value for driver count is going to be assigned twice or depending of the times the city name is repeated.  If you sum the driver count by city types only on the merged data frame, the driver count will be incorrect, you need to make the calculation on the city_data file, or if you are using the merged dataframe, first you need to make an average of the driver count by city and city type, then you can make the sum.


## Recommendations and Next Steps

- The summary key metrics for urban type should be done by city, the fares are subject to the size of the city and population.  It will be better to have this information by city to get a better understanding how the average fares behave.
- For the outliers, if we know the population and size of the city, we can compare the data and define if the outlier can be removed.

### Recommendations for Future Analysis
- The driver name should be included in the data provided, it will represents the real number of drivers by city.
- The driver count provided on the city data file does not have a date, so there is uncertanty if those driver count correspond to the time of the rides on the file ride data was acquired.
 


