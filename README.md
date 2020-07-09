# Time_Series_-_Electricity_Prices

## Introduction: 


<img src="images/CASIO%20duck%20curve%202020-06-29%20at%203.16.36%20PM.png" width="650">

## THE DATASET:
Hourly electricity prices from March 26, 2017 to June 23, 2020, sourced with an API from California Independent Operator System (CAISO). The hourly prices came from a particular node in downtown San Francisco called 'BAYSHOR2_1_N001.'

## SKILLS REQUIRED TO COMPLETE:
The skills used to complete this project consisted of sourcing data by API, preprocessing data, EDA, running the Autocorrelation Function and Partial Autocorrelation Function and selecting a model based on RMSE scores and using Python to make visualizations with Pandas.

## WHAT I POSTED ON GITHUB:
There are 2 notebooks posted on Github. The first one is called 'API.ipynb', which is where I made my API calls. The 2nd notebook is called 'Time Series with Electricity Prices.ipynb', which contains the rest of the project.

## QUESTIONS I POSED:
1. What model performed best and why?
2. What are the shortcomings of the model?

## HOW I PUT the DATA TOGETHER:
The hourly electricity prices for 3/26/17 - 2/26/20 were used as training set, while 2/26/20 - 6/23/20 was used as the validation set. The train/validation split is 90/10. The dates for the entire data look random because I wanted to use as many days as possible. The available data available on CASIO only went back to 3/26/17.

## FUTURE/STEPS I WOULD HAVE DONE
1. Add weather data and battery storage data to create a multi-variate time series and rerun all the models.
2. Build a long short-term memory neural network to try and make better predictions.

## RECOMMENDATIONS
The best performing model was the Persistence Algorithm (baseline model) with an RMSE of 7.0. The SARIMA model had an RMSE of 14.7 and FB Prophet had an RMSE of 19.3.

## PRESENTATION LINK:
https://docs.google.com/presentation/d/1hn61AqZwsyI_ZWP4gS2nemEWrdojjCwECu3VTbdxnvE/edit#slide=id.g8b672cc1eb_0_41

## REFERENCES FOR IMAGES IN PRESENTATION(in order):
https://transformers-magazine.com/tm-news/7323-california-distribution-transformers-market-to-grow-at-a-cagr-of-4-5/

https://www.caiso.com/Documents/FlexibleResourcesHelpRenewables_FastFacts.pdf

https://www.solar.com/learn/solar-panel-installation/

https://electrek.co/2020/06/11/tesla-cancelling-solar-roof-orders-after-years-deposits/

http://www.caiso.com/TodaysOutlook/Pages/prices.aspx

https://www.aarp.org/travel/destinations/united-states/san-francisco/

https://www.chooseenergy.com/news/article/energy-storage-costs-must-drop-for-renewables-to-supply-grid-power/
