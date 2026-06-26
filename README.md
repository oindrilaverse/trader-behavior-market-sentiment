<div align="center">

# Trader Behavior vs. Market Sentiment

**A data-driven analysis of how Bitcoin market sentiment (Fear vs. Greed) impacts historical trader performance.**
This project uncovers patterns in trading behavior, leverage usage, and profitability across different market cycles to provide actionable insights into human psychology in financial markets.

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

- **Sentiment-Driven Performance Analysis:** Correlates daily closed PnL and leverage data from traders with the Bitcoin Fear & Greed Index.
- **Data Cleansing & Aggregation:** Robust preprocessing pipeline that handles messy historical trade data, aligns timeframes, and computes aggregate metrics.
- **Advanced Visualizations:** Clean, compelling charts built with Matplotlib that illustrate complex market dynamics at a glance.
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

## Architecture / How it Works

1. **Data Ingestion:** Historical trade data (Hyperliquid) and the Bitcoin Fear & Greed Index are loaded from raw CSVs/APIs.
2. **Preprocessing:** Time-series data is normalized. Dates are aligned to merge high-frequency trade data with daily sentiment indices.
3. **Computation Logic:** Aggregations are performed using standard Pandas operations, such as inner merges on dates, filtering, and groupby calculations, to calculate average PnL categorized by sentiment thresholds (e.g., Extreme Fear, Fear, Neutral, Greed, Extreme Greed).
4. **Output:** The data is fed into Matplotlib to generate visual distributions and trend lines, clearly illustrating the shift in trader behavior.

---

## Technical Highlights & Learnings

- **Challenge:** Merging trade executions with daily sentiment metrics without over-complicating the data pipeline.
  - **Solution:** Implemented standard Pandas inner merges on extracted date columns to accurately attribute trades to the prevailing sentiment of the day.
- **Challenge:** Processing trade execution data effectively to find meaningful patterns.
  - **Solution:** Applied standard Pandas operations like filtering and groupby calculations to compute aggregate metrics across different sentiment classifications, ensuring a reliable and straightforward analysis.
- **Takeaway:** Building this pipeline reinforced the effectiveness of fundamental Pandas operations (merging, filtering, and grouping) to clean, align, and analyze time-series data without relying on overly complex methods.

---

## Contact

I am a Software Engineer passionate about data-driven problem solving and clean architecture. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)
