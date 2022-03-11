# time-series-stock-prediction
Prediction of the most recent 20% of the stock using LSTM.
Input: Given the dataset "prices.txt" which is a comma separated file consisting of the closing price of a certain stock for the past 5 years  
Output: Create a "machine learning model" that can accurately predict the most recent 20% prices.
# Dataset: prices.csv
# Linear Regression 
Linear Regression is a linear model that assumes a linear relationship between the input variables (x) and the single output variable (y). More specifically, that y can be calculated from a linear combination of the input variables (x).
# High level pseudo-code for Linear Regression Model:
1.	Add some feature engineering like: Is_month_end, Is_month_start, etc.
2.	Split dataset into the first 80% of data is training and the remaining is testing.
3.	Use sklearn for applying linear regression. 
# Evaluation 
By splitting data into 80% train and 20% test, which that the root mean square error is 448.45
![Predition](https://github.com/Ahmad3bdelHafeez/time-series-stock-prediction/blob/main/Linear%20Regression%20Evaluation.PNG "Time-Series")


# LSTM Model 
LSTMs are widely used for sequence prediction problems and have proven to be extremely effective. The reason they work so well is because LSTM can store past information that is important and forget the information that is not. LSTM has three gates:
1. The input gate: The input gate adds information to the cell state
2. The forget gate: It removes the information that is no longer required by the model
3. The output gate: Output Gate at LSTM selects the information to be shown as output
# High level pseudo-code for LSTM Model
1.	Split dataset into the first 80% of data is training and the remaining is testing.
2.	Each row consists of the past 30 days from this day.
-- For example: if today is 1/1/2022 the features of this day in array of prices from the previous 30 days [2/12/2021, …, …, …, 31/21/2021]
3.	Use LSTM Layers from keras to fit data.
4.	Predict the future data by the previous month.
# Evaluation:
By splitting data into 80% train and 20% test, which that the root mean square error is 61.7
![Predition](https://github.com/Ahmad3bdelHafeez/time-series-stock-prediction/blob/main/LSTM%20Evaluation.PNG "Time-Series")
# Demo: [[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Fzsx6hQONmaGpQevRE-iyPlM5-gAxxT3?usp=sharing)]
