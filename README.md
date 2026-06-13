<div align="center">

# 📊 Trader Behavior vs. Market Sentiment

**A data-driven analysis of how Bitcoin market sentiment (Fear vs. Greed) impacts historical trader performance.**
This project uncovers patterns in trading behavior, position sizing, and profitability across different market cycles to provide actionable insights into human psychology in financial markets.

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

</div>

---

## 🎨 Visuals

![Demo](./assets/demo.gif)
*(Placeholder for actual data visualization/dashboard demo)*

---

## 🔗 Live Links

- **[Live Deployment / Interactive Notebook](https://example.com/live)** *(Coming soon)*
- **[Full Documentation & Data Dictionary](https://example.com/docs)** *(Coming soon)*

---

## ✨ Features

- **Sentiment-Driven Performance Analysis:** Correlates daily closed PnL and trade size data from traders with the Bitcoin Fear & Greed Index to identify profitable behavior patterns.
- **Data Preprocessing & Aggregation:** A robust pipeline that handles datetime parsing of non-standard formats and effectively merges historical trades with daily market sentiment.
- **Advanced Visualizations:** Clean, compelling charts built with Matplotlib that illustrate complex market dynamics at a glance, clearly mapping PnL averages to sentiment thresholds.
- **Actionable Behavioral Insights:** Demonstrates that "Greed" phases correspond with higher PnL and trade sizes, while "Fear" phases trigger conservative, risk-averse behavior resulting in lower average returns.

---

## 🛠 Tech Stack

- **Core Tech Stack:** Python
- **Data Manipulation & Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib
- **Environment:** Jupyter Notebooks
- **Data Sources:** Historical Trade Data, Crypto Fear & Greed Index

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

   - Update `.env` with your API keys if you wish to fetch live data or configure environment specifics.

5. **Run the Notebook:**

   ```bash
   jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
   ```

</details>

---

## 🏗 Architecture / How it Works

1. **Data Ingestion:** Historical trade data and the Bitcoin Fear & Greed Index are loaded into memory using Pandas DataFrames.
2. **Preprocessing:** Datetime strings are parsed—specifically mapping custom timestamp formats (e.g., `"%d-%m-%Y %H:%M"`) into standardized date objects.
3. **Merging Data:** An inner merge is performed on the date column, cleanly aligning high-frequency historical trades with the daily sentiment index.
4. **Computation Logic:** The system filters for closed trades (non-zero PnL) and groups them by sentiment classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed) to compute the mean Closed PnL and Position Size.
5. **Output:** The aggregated data is fed into Matplotlib to generate visual distributions and trend lines, clearly illustrating the shift in trader behavior.

---

## 💡 Technical Highlights & Learnings

- **Challenge:** Merging disparate datasets with differing time frequencies (high-frequency asynchronous trade executions vs. daily sentiment metrics).
  - **Solution:** Addressed the timestamp mismatch by successfully casting the custom trade execution timestamp (`"%d-%m-%Y %H:%M"`) to a `datetime.date` object. This normalized both datasets to the same granularity, allowing for a clean, deterministic Pandas `inner` merge on the date column.
- **Challenge:** Isolating meaningful performance data from raw historical logs.
  - **Solution:** Implemented filtering logic to exclude open/unrealized trades by targeting only non-zero `Closed PnL`, ensuring the groupby aggregation strictly analyzed realized behavioral outcomes.
- **Takeaway:** Building this pipeline reinforced the importance of robust datetime normalization in time-series analysis and demonstrated how proper data structuring via Pandas can seamlessly reveal macroeconomic behavioral trends.

---

## 📫 Contact

I am a Software Engineer passionate about data-driven problem solving and clean architecture. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)
