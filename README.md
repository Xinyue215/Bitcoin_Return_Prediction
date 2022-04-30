# Bitcoin Return Prediction

This prject predicts the daily return of bitcoin from 7/1/2017 to 3/30/2022 using historical bitcoin data from 9/17/2014 to 6/30/2017.

## Bitcoin price overview
**(1. Please describe price behaviors of Bitcoin in English)**
The bitcoin price experienced a drastic increase (around 850%) starting from May, 2017, achieved a high point in December, 2017 and droped around 60% during early 2018. There have been some fluctuations during 2018 to late 2020 and a more extreme price rise started in late 2020. This 500% of increase quickly follows by a 50% drop and another round of increase. 

The price rise during 2017 might be caused by the joint of large amounts of individual retail investors. The fact that the cryptocurrency stands outside of the global financial system attracted investors. However, since bitcoin was not mature enough at that point, people were affraid of volatility, which caused the price drop quickly after it reached a highpoint. The price increase in 2021 on the other hand, was mainly caused by investors from large-scale institutions. Bitcoin is now accepted by companies like Paypal, Microsoft, Visa, and etc. This increased investor's trusts in cryptocurrency. Moreover, the inflation caused by COVID-19 also encouraged investors to consider bitcoin as a store of value.

## Project description
**(2. Based upon #1 above, please outline, in English, your approach; your guesses/hypotheses; your process)**
The speculative nature of the bitcoin price leads to a technical analysis to invest the pattern of daily return based on its historical data. Technical indicators are used in tehnical analyses to predict the market trend. Here, the Technical Analysis library is used to generate a series of technical indicators from financial time series datasets.

From the Technical Analysis library, 86 features are generated. Machine learning technques can be used to investigate the underlying correlations between this high dimentional input and the daily return. 

This analysis compares two approaches to predict bitcoin daily return. A classifier is used to predict the range of the next day return and a regressor is used to predict the exact return. 

The behavior of classifiers can largely depend on the defination of return ranges. Hence, the number of counts in each interval need to be checked to ensure a reasonable defination. Several classifiers are compared using ROC curve, accuracy score, and coefficient of determination. All tested classifiers are able to describe the model very well but a boosted decision tree using XGBoost gives the best output with a coefficient of determination of 0.999. 

Several regressors are also compared using pycaret. Extra trees regressor wins with a coefficient of determination of 0.992. 

The comparison between the classifier and regressor is not fair because they searve different purposes. However, we can make a quick comparison of these two models if we just want to take a rough guess of the next day return. Therefore, the output of the regressor is grouped into the intervals defined in the classifier section and the residual plot shows both approaches describes the model very well.

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

