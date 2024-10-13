# Stock Price Prediction Using LSTM

This project demonstrates the use of an LSTM (Long Short-Term Memory) neural network for stock price prediction. The model uses historical stock data along with several technical indicators to predict future stock prices. This project focuses on the backend development of the machine learning model, from data collection and preprocessing to model training and evaluation.

## Key Features

- **Stock Data Collection**: 
  - Fetches historical stock data using the Yahoo Finance API.
  - Supports adjustable data retrieval periods and intervals for flexibility.

- **Technical Indicators**: 
  - Adds commonly used technical indicators such as:
    - Simple Moving Average (SMA)
    - Exponential Moving Average (EMA)
    - Relative Strength Index (RSI)
    - Bollinger Bands
    - Volatility (standard deviation)
    
- **LSTM Model**:
  - A sequence-based LSTM model is built to predict stock prices based on past performance.
  - The model is trained on time-series data for better handling of the sequential nature of stock price data.
  - Includes dropout layers for regularization and to prevent overfitting.

- **Prediction and Visualization**:
  - After training, the model predicts future stock prices, which are then compared with actual stock prices.
  - A static plot visualizes the actual vs predicted stock prices.

## Workflow

1. **Data Collection**:
   - Historical stock data is fetched using Yahoo Finance's API. You can specify the stock ticker, period (e.g., 1 month), and interval (e.g., 5 minutes) for data collection.

2. **Feature Engineering**:
   - Several technical indicators are computed and added to the data to enhance the model's predictive power. These include moving averages (SMA, EMA), RSI, Bollinger Bands, and volatility.

3. **Data Preprocessing**:
   - The data is scaled using `MinMaxScaler` to normalize it for the LSTM model.
   - The time-series data is split into sequences to capture the sequential nature of stock price movements.

4. **LSTM Model**:
   - The model uses an LSTM architecture, which is well-suited for time-series forecasting.
   - Two LSTM layers with dropout are used, followed by fully connected dense layers to make the final prediction.

5. **Model Training**:
   - The model is trained on the processed data, and validation is performed to ensure model generalization.
   
6. **Prediction and Evaluation**:
   - The trained model is used to predict stock prices, and the results are compared to the actual prices.
   - The model's performance is evaluated using Mean Squared Error (MSE), and results are visualized using Matplotlib.
