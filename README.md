# 📈 Ethereum Candlestick Chart Generator

This project fetches Ethereum (ETH) price data for the past 30 days from the [CoinGecko API](https://www.coingecko.com/en/api) and visualizes it as an interactive **Candlestick Chart** using Plotly. The chart is saved as an HTML file and automatically opened in your default web browser.

---

## 🔧 Features

- 📡 **Live Data Fetching** from CoinGecko
- 🔄 **OHLC Conversion** (Open, High, Low, Close) using Pandas
- 📊 **Interactive Candlestick Chart** with Plotly
- 🌐 **Auto Opens in Browser** for Easy Viewing

---

## 🧪 Demo Output

Here's what you'll get:

![Candlestick Chart Preview](https://static.vecteezy.com/system/resources/previews/017/130/199/non_2x/business-candle-stick-graph-chart-of-stock-market-investment-trading-on-background-design-bullish-point-trend-of-graph-illustration-free-vector.jpg)
*(This is a representative image; your output will be interactive and rendered in a browser)*

---

## 🛠️ Requirements

- Python 3.7+
- Libraries:
  - `requests`
  - `pandas`
  - `plotly`
  - `datetime`
  - `webbrowser` (built-in)

Install required packages using the provided requirements.txt file:

```bash
pip install -r requirements.txt
```
## 🚀 How It Works

This project performs three main steps to generate a candlestick chart for Ethereum using live market data:

### 1. **Fetch Ethereum Data**
The script pulls ETH market data from CoinGecko's API for the last 30 days using the `get_eth_market_chart()` function.

```python
eth_data = get_eth_market_chart()
```
### 2. **Convert to OHLC Format**
The raw price data is resampled into daily OHLC (Open, High, Low, Close) format using Pandas' `.resample()` method.

```python
ohlc = convert_to_ohlc(eth_data)
```
### 3. **Plot Candlestick Chart**
An interactive chart is created using Plotly and opened in your default browser:

```python
plot_candlestick_to_browser(ohlc)
```
## 📌 Customization Tips

- **Change Currency**:
  Modify the `vs_currency='usd'` parameter in `get_eth_market_chart()` to another currency like `eur`, `inr`, `gbp`, etc.

- **Adjust Time Range**:
  Modify the `days` parameter to `'7'`, `'90'`, `'365'`, or `'max'` to change the time window of the data.

- **Dynamic File Naming**:
  To avoid overwriting charts and save with the current date:
  ```python
  filename = f"eth_candlestick_{datetime.now().strftime('%Y-%m-%d')}.html"

## 🙌 Acknowledgments

- 📊 Charting powered by [Plotly](https://plotly.com/python/)
- 📡 Price data from [CoinGecko API](https://www.coingecko.com/en/api)

## 📜 License

This project is licensed under the **MIT License** — you are free to use, modify, and distribute it.



