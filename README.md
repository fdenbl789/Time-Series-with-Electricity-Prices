# Time_Series_-_Electricity_Prices

## Introduction: 


<img src="images/CASIO%20duck%20curve%202020-06-29%20at%203.16.36%20PM.png" width="650">

The reason I did this project on electricity prices is because I am interested in the 'Duck Curve.' The Duck Curve is a phenomenon that occurs in a local electricity market where there has been substantial solar installation. In the afternoon hours(weather dependent), solar panels will supply electricity to the grid. This will cause a grid operator to reduce supply from other sources and also cause the price to drop substantially. Conversely, in the evening, since there is no supply from solar and the fact that demand increases, there is a need for a tremendous supply ramp. This makes it hard for grid operators to manage supply and demand not to mention higher prices. This creates the Duck Curve. While it is great that prices fall in the afternoon, improvements in efficiency can and will occur in the future. This is where energy storage comes into play. Electricity can be stored in the afternoon when it's inexpensive and used in the evening. This can have a balancing affect on prices, and prevent peaks that often occur during periods of increased electricity demand. Currently in California, there is only a tiny amount of battery storage being used. However, the California Independent Operator System (CAISO) already makes public when and how much the batteries are charging and discharging. In a few years, I would be interested in rerunning my models and hopefully observe lower electricity prices.

## OBJECTIVE:
To predict electricity prices for a local government, utility, grid operator or energy company using time series models. A Persistence Algorithm, SARIMAX and FB Prophet models will be run and compared to see which has the best predictions with the lowest RMSE.

## THE DATASET:
Hourly electricity prices from March 27, 2017 to June 23, 2020, sourced with an API from the California Independent Operator System (CAISO). The hourly prices came from a particular node in downtown San Francisco called 'BAYSHOR2_1_N001.' February 26, 2020 to June 23, 2020 was used as the test/validation set for the Persistence Algorithm, SARIMA and FB Prophet models. A time series cross validation from Scikit-learn was used as the test/validation set for the SARIMAX model.

<img src="images/entire%20Screen%20Shot%202020-07-08%20at%203.28.31%20PM.png" width="650">

## SKILLS REQUIRED TO COMPLETE:
The skills used to complete this project consisted of sourcing data by API, preprocessing data, EDA, running the Autocorrelation Function and Partial Autocorrelation Function and selecting a model based on RMSE scores. Also, feature engineering and using Scikit-learn's OneHotEncoder to incorporate exogenous variables were used. Visualizations were created with Pandas and Matplotlip.

## WHAT I POSTED ON GITHUB:
There are 3 notebooks posted on Github. The first one is called 'API.ipynb,' which is where I made my API calls. The 2nd notebook is called 'Time Series with Electricity Prices.ipynb,' which contains EDA, visualizations and time series models. The 3rd notebook is called 'Exogenous variables.ipynb,' which contains feature engineering with weather and datetime data to add to the SARIMAX model.

## QUESTIONS I POSED:
1. What model performed best with the lowest RMSE?
2. What are the shortcomings of the model?

## HOW I PUT the DATA TOGETHER:
The hourly electricity prices for 3/27/17 - 2/26/20 were used as training set, while 2/26/20 - 6/23/20 was used as the validation set. The train/validation split is 90/10. The dates for the entire data look random because I wanted to use as many days as possible. The available data available on CASIO only went back to 3/27/17. A time series cross validation from Scikit-learn was used as the test/validation set for the SARIMAX model.

## FUTURE/STEPS I WOULD HAVE DONE
1. Add battery storage data to add more exogenous variables to the time series and rerun all the models.
2. Build a long short-term memory neural network to try and make better predictions.

## RECOMMENDATIONS
The best performing model was the Persistence Algorithm (baseline model) with an RMSE of 7.0. The performance of the rest of the models are:
-SARIMA, RMSE of 14.7
-SARIMAX, RMSE of 12.1
-FB Prophet, RMSE of 19.3.


## PRESENTATION LINK:
https://docs.google.com/presentation/d/1hn61AqZwsyI_ZWP4gS2nemEWrdojjCwECu3VTbdxnvE/edit#slide=id.g8b50bd69af_0_0

## REFERENCES FOR IMAGES IN PRESENTATION(in order):
https://transformers-magazine.com/tm-news/7323-california-distribution-transformers-market-to-grow-at-a-cagr-of-4-5/
https://www.caiso.com/Documents/FlexibleResourcesHelpRenewables_FastFacts.pdf
https://www.solar.com/learn/solar-panel-installation/
https://electrek.co/2020/06/11/tesla-cancelling-solar-roof-orders-after-years-deposits/
http://www.caiso.com/TodaysOutlook/Pages/prices.aspx
https://www.aarp.org/travel/destinations/united-states/san-francisco/
https://www.chooseenergy.com/news/article/energy-storage-costs-must-drop-for-renewables-to-supply-grid-power/
