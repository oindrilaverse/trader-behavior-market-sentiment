<div align="center">

# Trader Behavior vs. Market Sentiment

**A data-driven analysis of how Bitcoin market sentiment (Fear vs. Greed) impacts historical trader performance and profitability.**

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen?style=for-the-badge)](https://github.com/yourusername/repo)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)

</div>

---

## Visuals

![Demo](./assets/demo.gif)

---

## Live Links

- **[Live Deployment / Interactive Notebook](https://example.com/live)**
- **[Full Documentation & Data Dictionary](https://example.com/docs)**

---

## Features

- **Sentiment-Driven Performance Analysis:** Correlates daily closed PnL and leverage data from historical traders directly with the Bitcoin Fear & Greed Index to map out behavioral shifts.
- **Robust Data Cleansing & Aggregation:** Employs a comprehensive preprocessing pipeline that effortlessly handles messy, high-frequency historical trade execution data, aligns timeframes, and computes reliable aggregate metrics.
- **Advanced Visualizations:** Leverages Matplotlib to generate clean, compelling visual distributions and trend lines that illustrate complex market dynamics and shifts in risk appetite at a glance.
- **Actionable Behavioral Insights:** Quantitatively demonstrates that "Greed" phases correspond with higher PnL and increased leverage usage, while "Fear" phases trigger highly conservative, risk-averse trading behavior.

---

## Tech Stack

**Frontend / Visualization**
- Matplotlib

**Backend / Data Processing**
- Python 3.8+
- Pandas
- NumPy

**Environment & APIs**
- Jupyter Notebooks
- Hyperliquid API (Historical Trader Data)
- Alternative.me API (Crypto Fear & Greed Index)

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
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Environment Variables:**
   - Copy the example `.env` file to set up your environment:
     ```bash
     cp .env.example .env
     ```
   - Update the `.env` file with any relevant API keys for fetching live data (e.g., Hyperliquid API, Alternative.me API).

5. **Run the Notebook:**
   ```bash
   jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
   ```
</details>

---

## Architecture / How it Works

1. **Data Ingestion:** High-frequency historical trade data (Hyperliquid) and the daily Bitcoin Fear & Greed Index are loaded from raw CSV files and API endpoints.
2. **Preprocessing:** Time-series data is normalized, and raw execution timestamps are aligned to accurately map high-frequency trade data with daily sentiment indices.
3. **Computation Logic:** Aggregations filter for closed trades (non-zero PnL) to calculate the mean PnL, leverage ratios, and win rates categorized strictly by sentiment thresholds (Extreme Fear, Fear, Neutral, Greed, Extreme Greed).
4. **Output Generation:** The processed and merged data is fed into plotting functions to generate visual distributions and trend lines that clearly illustrate shifts in historical trader behavior.

---

## Technical Highlights & Learnings

- **Challenge:** Merging high-frequency asynchronous trade executions with daily sentiment metrics without losing critical granularity or introducing look-ahead bias.
  - **Solution:** Implemented robust Pandas `merge_asof` and custom grouping logic to accurately attribute trades to the exact prevailing sentiment at execution time.
- **Challenge:** Handling outliers and extreme anomalies in historical trade data (e.g., liquidation spikes).
  - **Solution:** Applied IQR-based filtering and custom robust statistical techniques to ensure the final analysis reflected genuine behavioral trends rather than noise.
- **Takeaway:** Building this pipeline reinforced the importance of writing scalable data-cleaning functions and maintaining a deep understanding of index alignment in time-series analysis.

---

## Contact

I am a Software Engineer passionate about data-driven problem solving and writing clean, scalable architecture. Let's connect!

- [My LinkedIn Profile](https://linkedin.com/in/yourprofile)
- [My Portfolio](https://yourportfolio.dev)
- [Email Me](mailto:your.email@example.com)
