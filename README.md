# Bitcoin Return Prediction

This prject predicts the daily return of bitcoin from 7/1/2017 to 3/30/2022 using historical bitcoin data from 9/17/2014 to 6/30/2017.

## Description
This analysis compares two approaches to predict bitcoin daily return. A classifier is used to predict the range of the next day return and a regressor is used to predict the exact return. The classifier (XGBRF) achieves a coefficient of determination of 0.98 and the regressor (Extra Trees Regressor) achieves a coefficient of determination of 0.70. 

## Dependencies and libraries
- python 3.8.10
- XGBoost 1.3.3
- LightGBM 3.3.2
- sklearn 0.23.2
- pandas 1.4.2
- numpy 1.20.0
- plotly 5.7.0
- ta 1.10.1
- pycaret 2.3.10 
