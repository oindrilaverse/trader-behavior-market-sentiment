<div align="center">

# Trader Behavior vs. Market Sentiment

**A data-driven analysis of how Bitcoin market sentiment (Fear vs. Greed) impacts historical trader performance.** This project uncovers patterns in trading behavior, leverage usage, and profitability across different market cycles to provide actionable insights into human psychology in financial markets.

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen?style=for-the-badge)](https://github.com/yourusername/trader-behavior-market-sentiment/actions)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

</div>

---

## Visuals

![Demo](./assets/demo.gif)
*(Placeholder for actual data visualization/dashboard demo)*

---

## Live Links

- **[Live Deployment / Interactive Notebook](https://example.com/live)** *(Coming soon)*
- **[Full Documentation & Data Dictionary](https://example.com/docs)** *(Coming soon)*

---

## Features

- **Sentiment-Driven Performance Analysis:** Correlates daily closed PnL and leverage data from traders with the Bitcoin Fear & Greed Index to uncover behavioral patterns.
- **Data Cleansing & Aggregation:** A robust preprocessing pipeline handling messy historical trade data, ensuring accurate timeframe alignment and metric computation.
- **Advanced Visualizations:** Clean, compelling charts built with Matplotlib that illustrate complex market dynamics and user behavior at a glance.
- **Behavioral Insights:** Demonstrates that "Greed" phases correspond with higher PnL and leverage usage, while "Fear" phases trigger conservative, risk-averse behavior.

---

## Tech Stack

- **Language:** Python
- **Data Manipulation & Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib
- **Environment:** Jupyter Notebooks
- **Data Sources:** Hyperliquid Historical Trader Data, Alternative.me Crypto Fear & Greed Index

---

## Installation & Setup

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
   python3 -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Environment Variables:**
   - Copy the example `.env` file to set up environment variables:

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

## Architecture / How it Works

1. **Data Ingestion:** Historical trade data (`historical_data.csv`) and the Bitcoin Fear & Greed Index (`fear_greed_index.csv`) are loaded into Pandas DataFrames.
2. **Preprocessing:** Time-series data is normalized. Dates are aligned using the trade execution date to associate each trade with the prevailing market sentiment on that day.
3. **Computation Logic:** Aggregations are performed to calculate average closed PnL, leverage ratios, and win rates categorized by sentiment thresholds (e.g., Fear, Greed).
4. **Output:** The aggregated data is fed into Matplotlib to generate visual distributions and bar charts, clearly illustrating the shift in average PnL and trader behavior across market sentiment phases.

---

## Technical Highlights & Learnings

- **Challenge:** Merging high-frequency asynchronous trade executions with daily sentiment metrics without losing critical granularity or introducing look-ahead bias.
  - **Solution:** Emphasized the use of robust Pandas `merge_asof` and custom grouping logic to accurately attribute trades to the exact prevailing sentiment at execution time, maintaining high data integrity.
- **Challenge:** Handling outliers and extreme anomalies in historical trade data (e.g., liquidation spikes).
  - **Solution:** Applied **IQR filtering** and custom robust statistical techniques to ensure the final analysis reflected genuine behavioral trends rather than statistical noise.
- **Takeaway:** Building this data pipeline reinforced the importance of writing scalable data-cleaning functions and maintaining a strong engineering mindset when dealing with index alignment in financial time-series analysis.

---

## Contact

I am a Software Engineer passionate about data-driven problem solving and clean architecture. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
