# Stock Price Prediction and Sentiment Analysis

This project is a Flask-based web application that leverages machine learning algorithms, such as ARIMA, LSTM, and Linear Regression, to predict stock prices and analyze the sentiment of tweets related to the stocks. The app allows users to enter a stock symbol and get predicted stock prices, sentiment analysis, and recommendations for trading actions.

## Features

- **Stock Price Prediction:** 
  - **ARIMA Model** for time-series forecasting.
  - **LSTM (Long Short-Term Memory)** neural network for predicting stock prices.
  - **Linear Regression** for predicting future prices based on historical data.

- **Sentiment Analysis:** 
  - Fetches and analyzes tweets related to a given stock symbol using **Tweepy** and **TextBlob**.
  - Sentiment is categorized into positive, negative, or neutral.

- **Stock Recommendations:** 
  - Based on predicted stock trends and tweet sentiment, the app suggests whether to buy or sell the stock.

- **Graphical Visualizations:** 
  - Provides visualizations of stock price trends and sentiment analysis as pie charts and line plots.

## Installation

To run this project, you need to have Python 3.x installed. Additionally, the following dependencies are required:

1. Flask
2. Alpha Vantage (for stock data)
3. Tweepy (for Twitter API)
4. Statsmodels (for ARIMA model)
5. Keras (for LSTM)
6. Scikit-learn
7. TextBlob (for sentiment analysis)
8. Yfinance (for stock price data)
9. Matplotlib (for visualizations)

### 1. Clone the Repository

```bash
git clone https://github.com/your-repo/stock-price-prediction.git
cd stock-price-prediction
```

### 2. Install Dependencies

Create a virtual environment (optional but recommended) and activate it.

```bash
python3 -m venv venv
source venv/bin/activate   # On Windows, use venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

### 3. Set Up Twitter API Keys

Create a `.env` file and add your Twitter API keys as follows:

```
CONSUMER_KEY=your-consumer-key
CONSUMER_SECRET=your-consumer-secret
ACCESS_TOKEN=your-access-token
ACCESS_TOKEN_SECRET=your-access-token-secret
NUM_OF_TWEETS=100  # Adjust as needed
```

### 4. Run the Application

Start the Flask application by running:

```bash
python main.py
```

Visit the app in your web browser at `http://localhost:5000`.

## Usage

1. Enter a stock symbol (e.g., AAPL, TSLA) in the provided input field.
2. The app will fetch historical stock data and analyze it using ARIMA, LSTM, and Linear Regression models.
3. The app will display:
   - Predicted stock prices for the next day.
   - A pie chart showing the sentiment of recent tweets related to the stock.
   - A recommendation to **Buy** or **Sell** based on predictions and sentiment.

## Output

The application will generate the following outputs:

- **Stock Price Prediction Plots** (for ARIMA, LSTM, and Linear Regression models).
- **Sentiment Analysis Pie Chart**: Positive, Negative, and Neutral sentiment percentages based on recent tweets.
- **Recommendation**: Whether to buy or sell the stock based on predictions and sentiment.

## Contributing

If you would like to contribute to this project, feel free to fork the repository and submit a pull request with your improvements. Contributions are welcome!
