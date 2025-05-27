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

![Candlestick Chart Preview](https://images.app.goo.gl/cUSD4zQNKdH5rRVT6)
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

Install dependencies using pip:

```bash
pip install requests pandas plotly
