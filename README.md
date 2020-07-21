# Time_Series_-_Electricity_Prices

## Introduction: 


<img src="images/CASIO%20duck%20curve%202020-06-29%20at%203.16.36%20PM.png" width="650">

The reason I did this project on electricity prices is because I am interested in the 'Duck Curve.' The Duck Curve is a phenomenon that occurs in a local electricity market where there has been substantial solar installation. In the afternoon hours(weather dependent), solar panels will supply electricity to the grid. This will cause a grid operator to reduce supply from other sources and also cause the price to drop substantially. Conversely, in the evening, since there is no supply from solar and the fact that demand increases, there is a need for a tremendous supply ramp. This makes it hard for grid operators to manage supply and demand, not to mention creating higher prices. This creates the Duck Curve. While it is great that prices fall in the afternoon, improvements in efficiency can and will occur in the future. This is where energy storage comes into play. Electricity can be stored in the afternoon when it's inexpensive, and used in the evening when it's expensive. This can have a balancing affect on prices, and prevent peaks that often occur during periods of increased electricity demand. Currently in California, there is only a tiny amount of battery storage being used. However, the California Independent Operator System (CAISO) already makes public when and how much the batteries are charging and discharging. In a few years, I would be interested in rerunning my models and hopefully observe lower electricity prices.

## Objective:
To predict electricity prices for a local government, utility, grid operator or energy company using time series models. A Persistence Algorithm, SARIMAX and FB Prophet models will be run and compared to see which has the best predictions with the lowest RMSE.

## The Dataset:
Hourly electricity prices from March 27, 2017 to June 23, 2020, sourced with an API from the California Independent Operator System (CAISO). The hourly prices came from a particular node in downtown San Francisco called 'BAYSHOR2_1_N001.' 

<img src="images/entire%20Screen%20Shot%202020-07-08%20at%203.28.31%20PM.png" width="650">

## Skills Required to Complete:
The skills used to complete this project consisted of sourcing data by API, preprocessing data, EDA, running the Autocorrelation Function and Partial Autocorrelation Function and selecting a model based on RMSE scores. Also, feature engineering and using Scikit-learn's OneHotEncoder to incorporate exogenous variables were used. Visualizations were created with Pandas and Matplotlip.

## What I Posted on Github:
There are 4 notebooks posted on Github. The first one is called 'API.ipynb,' which is where I made my API calls. The 2nd notebook is called 'Time Series with Electricity Prices.ipynb,' which contains EDA, visualizations and time series models. The 3rd notebook is called 'Exogenous variables.ipynb,' which contains feature engineering with weather and datetime data to add to the SARIMAX model. The 4th notebook is called 'Practice for future multivariate time series.ipynb,' which contains code for a future project dealing with a multivariate time series analysis.

## Questions I Posed:
1. What model performed best with the lowest RMSE?
2. What are the shortcomings of the model?

## Train/Test Split:
For the Persistence Algorithm, SARIMA and FB Prophet models, the training set spanned from March 27, 2017 to February 26, 2020 and the test set spanded from February 26, 2020 to June 23, 2020 (90/10 split). A time series cross validation from Scikit-learn was used for the train/test set for the SARIMAX model (see graphs for breakout). Note that time series cross validation differs from k-fold VC becaues it does not shuffle the test indices. Successive training sets are supersets of those that come before them.


## Modeling Results
The best performing model was the Persistence Algorithm (baseline model) with an RMSE of 7.0. 

<img src="images/Persistence%20model%20-%201%20week%20predictions%202020-06-30%20at%2012.47.49%20PM.png" width="650">


2nd best, SARIMAX with an RMSE of 12.1

<img src="images/1st%20Split%20CV%20-%20SARIMAX%202020-07-08%20at%2010.59.49%20PM.png" width="650">

<img src="images/2nd%20split%20CV%20-%20SARIMAX%202020-07-08%20at%2011.00.42%20PM.png" width="650">

<img src="images/3rd%20split%20CV%20-%20SARIMAX%202020-07-08%20at%2011.02.20%20PM.png" width="650">


3rd best, SARIMA with an RMSE of 14.7

<img src="images/SARIMA%20no%20exognous%20variables%2C%20no%20CV%202020-06-30%20at%2012.54.21%20PM.png" width="650">


-Worst performing model, FB Prophet, RMSE of 19.3

<img src="images/FB%20Screen%20Shot%202020-06-30%20at%201.08.52%20PM.png" width="650">


## Future Steps
1. Add battery storage charge/discharge data to the exogenous variables and rerun all the models.
2. Build a long short-term memory neural network in order to make better predictions.


## Presentation Link:
https://docs.google.com/presentation/d/1hn61AqZwsyI_ZWP4gS2nemEWrdojjCwECu3VTbdxnvE/edit#slide=id.g8a55ece220_0_69

## References for Images in Presentation (in order):
https://transformers-magazine.com/tm-news/7323-california-distribution-transformers-market-to-grow-at-a-cagr-of-4-5/ \
https://www.caiso.com/Documents/FlexibleResourcesHelpRenewables_FastFacts.pdf \
https://www.solar.com/learn/solar-panel-installation/ \
https://electrek.co/2020/06/11/tesla-cancelling-solar-roof-orders-after-years-deposits/ \
http://www.caiso.com/TodaysOutlook/Pages/prices.aspx \
https://www.aarp.org/travel/destinations/united-states/san-francisco/ \
https://www.chooseenergy.com/news/article/energy-storage-costs-must-drop-for-renewables-to-supply-grid-power/ \
