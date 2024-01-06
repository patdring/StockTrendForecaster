# Project Overview

The core idea of this project is to predict stock prices using historical data. The dataset comprises simulated stock prices, along with correlated features such as economic indicators, temperature data, and sentiment data. These features are crafted to mimic real-world scenarios where multiple factors influence stock prices.

## Features

The dataset includes the following features:
- **Stock Prices**: Simulated stock prices.
- **Economic Data**: Simulated economic data correlated with stock prices.
- **Temperature Data**: Simulated temperature data, somewhat correlated with stock prices.
- **Sentiment Data**: Simulated sentiment data, representing public sentiment and its impact on stock prices.
  
## LSTM (Long Short-Term Memory) Networks

### Overview
LSTM networks are an advanced type of Recurrent Neural Network (RNN) designed to capture long-term dependencies in sequential data. Unlike standard RNNs, LSTMs include a series of gates that control the flow of information, allowing them to remember important inputs over long time intervals and forget the irrelevant ones.

### Architecture
- **Gates in LSTM**: Each LSTM unit has three gates: input, output, and forget gates. These gates determine what information should be retained or discarded as data flows through the sequence of LSTM cells.
- **Cell State**: The cell state acts as a conveyor belt running straight down the entire chain, with minor linear interactions. It carries relevant information throughout the processing of the sequence.
- **Hidden States**: Along with the cell state, hidden states are updated and passed to the next cell, contributing to the prediction at each step.

### Pros:
- **Long-Term Dependency Learning**: Exceptional in capturing long-term relationships, crucial for time series.
- **Flexibility**: Adaptable to different types of sequential data.
- **Reduced Vanishing Gradient Problem**: Overcomes limitations of traditional RNNs by mitigating the vanishing gradient problem.

### Cons:
- **Complexity**: More complex architectures leading to longer training times.
- **Resource-Intensive**: Demands more computational power.
- **Overfitting Risk**: Especially in scenarios with limited data.

---

## N-Beats

### Overview
N-Beats is a deep learning model for time series forecasting that stands out due to its pure forward fully-connected neural network architecture. It leverages a unique backward and forward residual link structure to decompose the forecast into multiple interpretable components.

### Architecture
- **Fully Connected Layers**: N-Beats uses stacks of fully connected layers without any convolutional or recurrent layers.
- **Backcast and Forecast**: The model makes use of two outputs at each block – backcast, which is used to subtract the already explained part of the input series, and forecast, which predicts future values.
- **Interpretable Outputs**: The model can be configured to produce outputs that offer interpretations in terms of trend and seasonality components.

### Pros:
- **Interpretable Forecasts**: Generates forecasts that can be broken down into understandable components.
- **Model Flexibility**: Can be used standalone or in conjunction with other models.
- **Simple Structure**: Relies on fully connected layers, avoiding the complexity of RNNs or CNNs.

### Cons:
- **Data Intensive**: Requires substantial data for optimal performance.
- **Computational Demand**: Potentially high computational requirements due to deep networks.
- **Relatively New**: As a newer model, it might lack extensive real-world testing compared to established methods.

---

## Prophet

### Overview
Prophet is a forecasting tool developed by Facebook, designed to be accessible and produce high-quality forecasts. It is particularly effective for time series data with strong seasonal patterns and several seasons of historical data.

### Architecture
- **Trend Models**: Prophet automatically selects between linear or logistic growth trend models.
- **Seasonality Decomposition**: It decomposes the time series into daily, weekly, and yearly seasonalities.
- **Holiday Effects**: Allows incorporating known holiday effects into the model.
- **Automated Model Tuning**: Automatically detects change points and adjusts trends accordingly.

### Pros:
- **User-Friendly**: Requires minimal data pre-processing and tuning.
- **Effective Seasonality Handling**: Captures complex seasonal patterns effectively.
- **Robust to Missing Data**: Handles missing data and outliers gracefully.

### Cons:
- **Black Box Nature**: Offers less control over the modeling process.
- **Optimized for Specific Use Cases**: Best suited for datasets with strong seasonal patterns.
- **Limited Scope for Customization**: Offers less flexibility for expert adjustments.
