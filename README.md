# Linear-Regression-Assignment - Bike Sharing

# Introduction

Build a model to predict the features that will lead to increase the demand for bike sharing.

# Problem Statement

A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.
A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state.
In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.
They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:
Which variables are significant in predicting the demand for shared bikes. How well those variables describe the bike demands Based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on some factors.

# Business Goal:

You are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market.


# Table of Contents

* General Info

* Technologies Used

* Conclusion


# General Information

* Analye the contents of day.csv and derive conclusions.
* The data contains 2018 and 2019 data and various features when the bike was booked.
* Perform eda, prepare the data, build the model on training set and identify the features that will lead to high demand of the data. 
* Evaluate the model on test set to see if the model fits the data or not.

# Technologies used

* Python libaries
* Pandas
* Numpy
* Matplotlib
* Seaborn
* Warnings
* Statsmodels
* sklearn
* EDA techiniques to clean up the data

# Conclusions 

## Conclusions from Univariate analysis

1. We dont see much difference with the seasons, but fall seems to be the highest.
2. No of holidays is less compared to working days.
3. We have more working days compared to weekends
4. The clear weathersit has more count.
5. humidity and windspeed - show the bell curve

## Conclusions from Bivariate analysis

1. For the fall season we see the max no of bookings of vechicles.
2. The no of bike booking is more in year 2019 compared to 2018.
3. For the month of Sep we see max bookings.
4. The no of bookings is highest on non holiday days.
5. Max bookings are found on weekends.
6. Max bookings are found on non working days.
7. Max bookings are found on clear weather days.


## Conclusions from Multivariate analysis


1. It is found that temp and atemp have highest correlation with cnt - bookings of the bike.
2. From the pair plot both temp and atemp variables follow the linear correlation against each other this might be due to high colinearity need to check when modeling.
3. From the pair plot looks like the temp and atemp follows the positivie correlations against the cnt.

## Conclusion from Model building

We can see that the equation of our best fitted line is:
cnt = 0.508462 + 0.245724 \times yr - 0.085507 \times holiday - 0.190233 \times windspeed - 0.250334 \times season_spring -0.049694 \times season_summer-0.023054 \times season_winter-0.108634 \times mnth_Dec -0.120162 \times mnth_Jan-0.018222 \times mnth_Jul-0.099464 \times mnth_Nov+0.053371 \times mnth_Sep+0.086918 \times weathersit_clear-0.224786 \times weathersit_light
Overall we have a decent model.

# Top 3 significant features are
Year
spring season
When the weather condition is Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds

# Business Insights 

1. We can see that there are features which positive and negative. The +ve independent features will lead to increase in demand for the booking and the -ve independent features will decrease demand for booking. However, we see that the -ve coeffients are weak i.e., <0.5. Though we have weak negative coefficients but considering the weather condition and seasons they might adversely impact the demand for bikes.
2. The company has seen the bike booking grow in the year 2019 compared to 2018. So post covid the company can look towards increase in demand for bike booking.
3. Company can design business strategy to increase the business during clear weather conditions and during spring season, sep month i.e beginning of fall season in US. Since the weather is clear people would opt bike booking compared to other seasons where they might encounter rains or dry(sunny) days.
4. When there is light weather condition where snow or light rains or high winds, during winter,holiday,summer seasons for the months Jul,Nov - Jan time period where minimal booking is expected due to bad weather condition for bikers. The company can reduce the supply and probably do some other activities like maintenace, reduce the manpower etc.