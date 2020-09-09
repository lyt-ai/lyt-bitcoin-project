# lyt-bitcoin-project
Bitcoin Price Prediction

## Problem Statement

We sought to test the possibility of forecasting the prices of a financial asset for the following reasons:
1. As a demonstration to a full time day trader and possible client of the strength machine learning has in boosting trading profits
2. To test the feasibility of performing short term price predictions on volatile markets for determining buying, holding or selling positions.

## Technologies Used
1. Python
2. Keras & Tensorflow for Deep Learning
3. Jupyter Notebooks as an IDE
4. Google Collab as a low cost training and inference platform with GPU availability

## Methodology
### Data Gathering
Data was collected on a 1 minute aggregation basis from the Gemini cryptocurrency exchange (https://gemini.com) as it has one of the cleanest open source bitcoin price data repositories.

Date range for data was over a period of 3 years from Jan 2016 - June 2016, to ensure that our training dataset was large enough, and we held out the period after Jan 2016 as our testing data set.

### Data Processing
Our data set was cleaned, and a number of variables were engineered to boost the predictive power of the models we built. Examples include seasonality variables such as Day of week

Due to the application of the Long Short Term Memory deep learning algorithm, the data was transformed into 3 dimensional arrays that is applicable to capture the sequences of the bitcoin prices over time.

### Algorithm
As per our the nature of time series forecasting problem, we're applying the LSTM deep learning alorithm with the Keras implementation (Tensorflow backend) with the following architechure:
1. 3 hidden layers with 0.2 dropout after each layer and 1 output layer
2. Optimizer: ADAM
3. Loss Function: RMSE


### Results
Our model, when applied to test data after the crash in bitcoin prices performed quite well with a margin of error of just about 0.4%. In more business terms, this meant that our margin of error in predicting the price of bitcoin was just $12.

This gave us a lot of inspiration and promise as a proof of concept and led us to the point where we certainly believe we could move on to build Lyt-AI around selling financial asset price predictions.
