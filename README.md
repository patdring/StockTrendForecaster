# StockTrendForecaster
Utilizing LSTM neural networks for stock price prediction. This repo contains a Jupyter Notebook demonstrating time series forecasting using historical stock data, economic indicators, and sentiment analysis. Ideal for exploring machine learning in finance.

## Stock Price Prediction using LSTM

This project focuses on predicting stock prices for the next 5 days based on historical data using a Long Short-Term Memory (LSTM) network. The goal is to demonstrate the application of LSTM neural networks in time series prediction, particularly in the context of financial markets.

## Project Overview

The core idea of this project is to predict stock prices using historical data. The dataset comprises simulated stock prices, along with correlated features such as economic indicators, temperature data, and sentiment data. These features are crafted to mimic real-world scenarios where multiple factors influence stock prices.

## Features

The dataset includes the following features:
- **Stock Prices**: Simulated stock prices.
- **Economic Data**: Simulated economic data correlated with stock prices.
- **Temperature Data**: Simulated temperature data, somewhat correlated with stock prices.
- **Sentiment Data**: Simulated sentiment data, representing public sentiment and its impact on stock prices.

These features are combined and normalized to form the input to the LSTM model.

## LSTM for Time Series Prediction

LSTM networks are a type of recurrent neural network (RNN) suitable for time series prediction due to their ability to remember long-term dependencies. They are particularly useful in financial markets where past information is a key indicator of future trends.

### Model Architecture

The LSTM model used in this project is defined with the following parameters:
- **Input Size**: 4 (corresponding to the 4 features in the dataset)
- **Hidden Layer Size**: 100
- **Output Size**: 1 (predicting stock prices)
- **Number of Layers**: 3
- **Dropout**: 0.5

The model predicts stock prices based on a sequence of data points from the past.

### Training and Validation

The model is trained with a batch size of 32 and a sequence length of 8. Early stopping is implemented to prevent overfitting, and gradient clipping is used to ensure stable training. The Adam optimizer with a learning rate of 0.001 and a learning rate scheduler are employed.

## Visualization

The results are visualized by comparing the actual stock prices with the 5-day predictions from the model. This visualization aids in understanding the model's performance and accuracy.

## Usage

This project is structured as a Jupyter Notebook, making it easy to follow the code and visualize the output step-by-step.

## Getting Started

To run this project, clone the repository and open the Jupyter Notebook in an environment that supports Python and PyTorch. Ensure you have the necessary libraries installed, including `torch`, `numpy`, `matplotlib`, and `sklearn`.

## Conclusion

This project demonstrates the capability of LSTM networks in predicting time series data. While the dataset used is simulated, the approach and methodology can be applied to real-world financial datasets.
