<div align="center">

# 📊 Trader Behavior vs. Market Sentiment

**A data-driven analysis uncovering how Bitcoin market sentiment impacts historical trader performance. By analyzing trade behavior, leverage usage, and profitability across different market cycles, this project provides actionable insights into human psychology in financial markets.**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Data_Vis-blue?style=for-the-badge)](https://matplotlib.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

</div>

---

## 🎨 Visuals

![Demo](./assets/demo.gif)
*(Placeholder for actual data visualization/dashboard demo)*

---

## 🔗 Live Links

- **[Live Deployment / Interactive Notebook](#)** *(Coming soon)*
- **[Full Documentation & Data Dictionary](#)** *(Coming soon)*

---

## ✨ Features

- **Sentiment-Driven Performance Analysis:** Correlates daily closed PnL and leverage data from traders with the Bitcoin Fear & Greed Index.
- **Robust Data Cleansing & Aggregation:** Handles messy historical trade data, aligns timeframes, and computes aggregate metrics like average PnL and leverage ratios.
- **Advanced Data Visualization:** Illustrates complex market dynamics and shifts in trader behavior through clean, compelling charts built with Matplotlib.
- **Behavioral Insights Extraction:** Quantifies human psychology by demonstrating that "Greed" phases correspond with higher returns and risk appetite, while "Fear" triggers conservative, risk-averse behavior.

---

## 🛠 Tech Stack

- **Language:** Python 3.8+
- **Data Manipulation & Analysis:** Pandas, NumPy
- **Data Visualization:** Matplotlib
- **Environment:** Jupyter Notebooks
- **Data Sources:**
  - Hyperliquid Historical Trader Data
  - Alternative.me Crypto Fear & Greed Index

---

## 🚀 Installation & Setup

<details>
<summary><b>Click here to view detailed setup instructions</b></summary>
<br>

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/trader-behavior-market-sentiment.git
   cd trader-behavior-market-sentiment
   ```

2. **Create and activate a virtual environment:**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Environment Variables:**
   - Copy the example `.env` file:

     ```bash
     cp .env.example .env
     ```

   - Update `.env` with your API keys if you wish to fetch live data (e.g., Hyperliquid API, Alternative.me API).

5. **Run the Notebook:**

   ```bash
   jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
   ```

</details>

---

## 🏗 Architecture / How it Works

1. **Data Ingestion:** Historical trade execution details (price, size, side, leverage, and PnL) and the daily Bitcoin Fear & Greed Index are loaded into memory.
2. **Preprocessing & Alignment:** Time-series data is normalized, and trade timestamps are aligned to merge high-frequency trade data seamlessly with daily sentiment indices using Pandas data joining functions.
3. **Computation Logic:** Trades are aggregated to calculate average PnL, leverage ratios, and trade size categorized by sentiment classifications (e.g., Extreme Fear, Fear, Neutral, Greed, Extreme Greed).
4. **Output Generation:** The processed distributions are fed into Matplotlib to generate visual distributions and trend lines, clearly illustrating the shift in trader behavior.

---

## 💡 Technical Highlights & Learnings

- **Challenge:** Merging high-frequency asynchronous trade executions with daily sentiment metrics without losing critical granularity or introducing look-ahead bias.
  - **Solution:** Implemented robust Pandas `merge_asof` and custom grouping logic on normalized dates to accurately attribute trades to the exact prevailing sentiment at execution time.
- **Challenge:** Handling outliers and extreme anomalies in historical trade data (e.g., liquidation spikes).
  - **Solution:** Applied IQR-based filtering and custom robust statistical techniques to ensure the final analysis reflected genuine behavioral trends rather than noise.
- **Takeaway:** Building this analytical pipeline reinforced the importance of writing scalable data-cleaning functions and maintaining a deep understanding of index alignment in time-series analysis.

---

## 📫 Contact

I am a Software Engineer passionate about data-driven problem solving and writing clean, maintainable code. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)
