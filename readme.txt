Gas Power Generation Forecasting 

The inspiration for this project came from my recent research proposal to Natural England for the production of a Risk Register in the State of Natural Capital Report. The report identifies Gas power generation as a significant source of NO2 and PM emissions in the UK.
Although the share of renewables is increasing in the energy mix, Gas is still the most secure source of energy and will be so in the foreseeable future.
To restrict air pollution emissions coming from power generation accurate forecasting of Gas power production is very important to ensure that gas power plants are only used when necessary which can help to reduce greenhouse gas emissions, improve grid reliability, and reduce costs.
Thus, I decided to explore time series forecasting for gas power generation.

The dataset used here is from The Modo Energy Platform. It is the hourly data collected from the 24th of June 2022 to the 25th of June 2023.

Links:

https://news.sky.com/story/why-the-uk-producing-half-its-electricity-from-gas-12431632

https://www.nationalgrideso.com/electricity-explained/how-electricity-generated/how-electricity-generated-using-gas

Employing appropriate statistical models and algorithms is crucial for gas power generation prediction. There are many Techniques such as classic time series analysis like ARMA, ARIMA models,  regression analysis, and newer methods like Machine Learning models, Artificial Neural Networks and Phophet that can be applied to historical data to develop predictive models. Also, incorporating domain expertise from power industry professionals, energy economists, and data scientists can provide valuable insights and improve the accuracy of gas power generation predictions.

In this notebook, I've used two methods for time series forecasting:

1) XGBoost - a popular machine learning algorithm which learns complex patterns and interactions in the data while maintaining good generalization performance. It combines multiple weak models to create a strong and accurate predictive model which makes it efficient in time series forecasting. XGBoost is used to forecast a period of two weeks of hourly gas production.

2) LSTM - a type of recurrent neural network (RNN) that is designed to make predictions on a series of data. They can capture long-term dependencies in the input sequence and make predictions based on the learned patterns. LSTM has been used to forecast a one-day period of hourly gas production.

I then measured the accuracy of the predictions by a using RMSE (Root Mean Squared Error) - it is a statistic which evaluates regression models to compare different models. The lower the RMSE, the better model it is at making predictions.

Comparing the RMSEs, LSTM was a more accurate predictor for gas production, with the drawback being, that it gave extremely inaccurate predictions for a longer period of 2 weeks.

XGBoost had a higher RMSE, but did a better job at predicting a longer period of forecast. 
