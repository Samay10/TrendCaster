# TrendCaster: Stock Market Trend Prediction System

**TrendCaster** is a stock market prediction system that uses Markov Chains and machine learning to forecast market trends based on historical data. The system analyzes past stock price movements to identify transition probabilities and generate predictive insights, helping traders make more informed decisions.

## Features

- **Market Trend Forecasting:** Predicts stock market trends using Markov Chains.
- **Real-Time Data Analysis:** Analyzes historical and real-time data to identify market trends.
- **Risk Assessment:** Provides risk metrics and confidence intervals to aid in decision-making.
- **Multiple Simulation Paths:** Generates multiple future price simulation paths to assess market movement.
- **Directional Accuracy:** Achieved 55% directional accuracy, providing insights for better trading strategies.

## Tech Stack

- **Python**
- **Markov Chains**
- **scikit-learn**
- **yfinance**
- **NumPy**
- **Pandas**
- **Matplotlib**

## Installation

To get started with **TrendCaster**, follow the steps below:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/TrendCaster.git
2. Navigate to the project directory:
   ```bash
   cd TrendCaster
3. Run the code file:
   ```bash
   StockPred.ipynb

## Usage
- Download Historical Stock Data:
  The system uses the yfinance library to fetch historical stock price data (e.g., AAPL). Adjust the start and end dates as required.

- Simulate Market Trends:
  TrendCaster uses a Markov Chain model to simulate future stock price movements based on historical price transitions.

- Visualize Results:
  The system generates a graphical representation of the simulated stock prices to visualize potential market trends.

## Example

```python
import yfinance as yf
import matplotlib.pyplot as plt
from trendcaster import TrendCaster

# Download historical stock data for Apple (AAPL)
stock_data = yf.download('AAPL', start='2023-11-01', end='2023-12-01')

# Initialize TrendCaster with historical data
trendcaster = TrendCaster(stock_data)

# Simulate stock price for the next 30 days
simulated_dates, simulated_prices = trendcaster.simulate_stock_price(days=30)

# Plot simulated prices
plt.plot(simulated_dates, simulated_prices, label='Simulated Prices')
plt.xlabel('Days')
plt.ylabel('Price')
plt.title('Simulated Stock Price Movement')
plt.legend()
plt.show()
```
## Contributing

We welcome contributions to improve **TrendCaster**! If you have ideas, improvements, or bug fixes, feel free to fork the repository, create a new branch, and submit a pull request.

### How to Contribute:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Create a new pull request.

## License

This project is licensed under the GNU v3.0 License - see the [LICENSE](LICENSE) file for details.
