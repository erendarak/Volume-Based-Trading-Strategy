# Volume-Based Trading Strategy

## Project Overview
This project combines concepts from **machine learning**, **deep learning**, and **finance** to develop a **volume-based trading strategy**. By analyzing the relationship between trading volume and stock price movements, the strategy aims to predict stock returns and generate actionable trading signals. 

The strategy is implemented using **Long Short-Term Memory (LSTM)** neural networks for forecasting trading volumes and integrates rule-based decision-making for adaptive trading.

---

## Features
- **Volume Forecasting**: Predict trading volumes using LSTM-based models.
- **Market Regime Classification**: Identify bull and bear markets using moving averages.
- **Signal Generation**: Generate buy, sell, and hold signals based on trading volume, market regimes, and recent returns.
- **Risk Management**: Incorporate stop-loss and take-profit mechanisms to optimize returns and limit losses.
- **Backtesting Framework**: Validate the strategy on historical data with robust performance metrics.

---

## Technologies Used
- **Python**
- **Pandas, NumPy**: Data preprocessing and analysis.
- **TensorFlow/Keras**: Implementing LSTM neural networks.
- **Matplotlib, Seaborn**: Data visualization and exploratory analysis.
- **Quantopian/cvxportfolio**: Backtesting and simulation (if applicable).

---

## Installation and Usage
### Prerequisites
- Python 3.8 or later
- Required libraries: `tensorflow`, `numpy`, `pandas`, `matplotlib`, `scikit-learn`

Install dependencies using pip:
```bash
pip install tensorflow numpy pandas matplotlib scikit-learn
```

### Running the Project
1. **Prepare the Dataset**:
   - Historical stock data for NVIDIA (NVDA) is required, including OHLC and volume data.
   - The dataset should be cleaned and formatted with features such as daily returns, volatility, and trading volume.

2. **Run the Jupyter Notebook**:
   - Execute `cs440Strategy.ipynb` step-by-step to preprocess the data, train the LSTM model, and generate signals.

3. **Backtesting**:
   - Use the provided backtesting framework to evaluate the performance of the strategy on test data.

---

## Methodology
### Data Preprocessing
- Cleaning and normalization of historical stock data.
- Feature engineering: daily returns, volatility, and rolling averages.
- Temporal segmentation for training and testing (80%-20% split).

### Model Design
1. **Volume Prediction**:
   - LSTM neural network for predicting trading volumes.
   - Inputs: historical volumes, returns, and volatility.

2. **Market Regime Identification**:
   - Moving Average Crossovers (SMA 20 and SMA 50) to classify bull and bear markets.

3. **Signal Generation**:
   - Buy, sell, and hold signals based on:
     - Predicted volumes (high/low thresholds).
     - Market regime (bull or bear).
     - Recent returns.

### Backtesting
- Initial capital: $10,000.
- Evaluate performance metrics:
  - **Sharpe Ratio**: Risk-adjusted returns.
  - **Net Profit/Loss**: Total gains/losses over the test period.

---

## Results
- **Sharpe Ratio**: 1.34 (indicating favorable risk-adjusted returns).
- **Net Profit**: 1,310% over the test period.
- **Correlation**: Predicted and actual volumes showed a strong correlation of 0.59.

---

## Future Work
- **Dynamic Thresholds**: Enhance signal generation with adaptive thresholds.
- **Real-Time Implementation**: Integrate with live data feeds for real-time trading.
- **Scalability**: Test the strategy across multiple stocks and asset classes.
- **Advanced Models**: Explore alternative architectures like Transformers or hybrid models.

---

## Contributors
- **Eren Darak**
- **Ahmet Berkay Arslanpençe**
- **Ragıp Şamil Bekiryazıcı**

---

## Repository
Access the project code and documentation on GitHub: [Volume-Based Trading Strategy Repository](#)

---

## Contact
For further information, contact the contributors through their provided emails or GitHub profiles.
