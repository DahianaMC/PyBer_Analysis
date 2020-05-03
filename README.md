# PyBer Analysis Report
### Purpose
Pyber data was provided to create visualizations to help to understand the data easier.  The objective is to create charts that can provide the information quickly and detect patterns, trends, correlations and outliners.  We will be using bubble charts, box plots, line charts for the analysis.  In this case Matplolib will be used to create the charts to visualize data from a Data Series or DataFrame.
## Background and Results
- The data includes two files: city_data and ride_data.  The city_data includes the city name, driver count by city and type of city.  The ride data includes city name per ride, date by ride, the fare for each ride and the ride id.  
- We inspected the data for NaN values, and analize if the files can be merged.  Both data sets have the city name and was merged using this column to create a DataFrame.  
- Using the merged DataFrame we created 3 DataFrames for each type of city: Urban, Suburban and Rural, then we computed the number of rides, the average fare and driver counts per city for each DataFrame by city type.  
- We incorporated the data calculated in a bubble chart and show the Total Number of Rides (Per City) vs Average Fare.
- The mean, median and mode were calculated for rides, fare and drivers by city type using different methods like pandas, numpy and SciPy, and also the box plots were created for ride count, ride fare and driver count by city type.
- After getting the percentages of fares, rides and drivers by city type, we created a pie chart for each of the variables (fares, rides and drivers).
- For Challenge of Module 5:
  - Need to create a DataFrame that summarizes the key metrics for the ride-sharing data by city type.
  - Create a multiple-line chart, with one line for each city type, that shows the sum of the fares for each week.
  - Write a report with the results.


### Technical Analysis

### Results
- Bubble Chart: PyBer Ride-Sharing Data (2019)

![Fig1](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig1.png)

  - The bubble chart shows the total number of rides in the urban cities are higher, but cheaper comparing with the rural and suburban cities.  Urban cities have more than doble of the rides of the rural cities, but the fares in rural cities are more expensive comparing with the suburban and urban cities.

- Box Plots: 
  - Ride Count Data (2019)

  ![Fig2](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig2.png)

  Shows the ride counts per city by city type.  Urban cities has 3 times of rides of rural cities, suburban cities has almost twice the rides of the rural cities.  The data for urban cities shows an outlier, but I will not remove it since the point is very close to the upper limit and more information will be needed to remove that point from the data.

  - Ride Fare Data (2019)

  ![Fig3](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig3.png)

  Shows the ride fares by city type.  Rural fares show the highest fares for city type, and urban cities reported the lowest fares.  The rural fares are more spread out than the suburban and urban cities.  

  - Driver Count Data (2019)

  ![Fig4](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig4.png)

  - Shows the driver count by city type.  Less drivers are needed for rural cities

![Fig5](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig5.png)

![Fig6](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig6.png)

![Fig7](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig7.png)

![Fig8](https://github.com/DahianaMC/PyBer_Analysis/blob/master/Analysis/Fig8.png)

### Summary

## Challenges Encountered and Overcome

### Challenges and Difficulties Encountered

* Programming

* Data analysis

* Graphing, etc

### Technical Analyses Used

## Recommendations and Next Steps

### Recommendations for Future Analysis

### Additional Analysis 1

* Description of Approach

* Technical Steps

### Additional Analysis 2

* Description of Approach

* Technical Steps
