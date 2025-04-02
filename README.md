# Finance Data Analysis

This repository contains a financial data analysis project that processes and visualizes Bitcoin (BTC) price data. The project utilizes Python, Pandas, Matplotlib, and other libraries for financial analysis, including moving averages, RSI, MACD, and Bollinger Bands.

## 📌 Features

- 📊 **Data Processing**: Load and clean historical BTC price data.
- 📈 **Technical Indicators**: Calculate and visualize:
  - Simple Moving Averages (SMA)
  - Relative Strength Index (RSI)
  - Moving Average Convergence Divergence (MACD)
  - Bollinger Bands (BB)
  - Stochastic Oscillator
- 📉 **Trading Signals**: Identify potential buy/sell signals based on indicator thresholds.
- 📷 **Visualization**: Generate charts for BTC price trends and indicators.
- 🔄 **Backtesting** (Upcoming): Test trading strategies based on historical data.

## 🛠️ Installation

Ensure you have Python 3 installed. Then, clone this repository and install dependencies:

```bash
# Clone the repository
git clone https://github.com/vvact/finance.git
cd finance

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

# Install required packages
pip install -r requirements.txt
```

## 📥 Data Acquisition

The dataset should be stored as a CSV file. Ensure your dataset has columns like:
```plaintext
timestamp, open, high, low, close, volume, SMA_10, SMA_50, RSI_14, MACD, Bollinger Bands, etc.
```
If using Binance API or another source, modify `data_loader.py` to fetch and format data.

## 📊 Usage

Run the Jupyter Notebook to analyze and visualize the data:
```bash
jupyter notebook
```
Open `finance_analysis.ipynb` and execute the cells to compute indicators and generate plots.

Alternatively, run a Python script:
```bash
python analysis.py
```

## 📌 Example Plots

- **Close Price and Moving Averages**:
  ```python
  plt.figure(figsize=(14, 7))
  plt.plot(btc_df['timestamp'], btc_df['close'], label="Close Price", color="blue")
  plt.plot(btc_df['timestamp'], btc_df['SMA_10'], label="SMA 10", color="red")
  plt.plot(btc_df['timestamp'], btc_df['SMA_50'], label="SMA 50", color="green")
  plt.legend()
  plt.show()
  ```

- **MACD and Signal Line**:
  ```python
  plt.figure(figsize=(14, 5))
  plt.plot(btc_df['timestamp'], btc_df['MACD'], label="MACD", color="blue")
  plt.plot(btc_df['timestamp'], btc_df['MACD_signal'], label="Signal Line", color="red")
  plt.axhline(0, linestyle="--", color="black")
  plt.legend()
  plt.show()
  ```

## 🚀 Future Improvements

- Implement an interactive dashboard.
- Add a backtesting module.
- Explore machine learning models for price prediction.

## 📜 License
This project is licensed under the MIT License.

## 🤝 Contributing
Feel free to fork, open issues, or submit pull requests!

## 📩 Contact
For questions or suggestions, contact [Your Name] via GitHub Issues.

---
**Happy Trading! 📈🚀**

