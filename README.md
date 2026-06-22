<div align="center">

# 📊 Trader Behavior vs. Market Sentiment

**A data-driven analysis uncovering how Bitcoin market sentiment (Fear vs. Greed) directly impacts historical trader performance, leverage utilization, and profitability.**

[![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen?style=for-the-badge&logo=githubactions&logoColor=white)](https://github.com/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

</div>

---

## 🎨 Visuals

![Demo](./assets/demo.gif)
*(Placeholder for an interactive data visualization or dashboard showcasing market trends vs. PnL)*

---

## 🔗 Live Links

- **[Live Deployment / Interactive Notebook](https://example.com/live)**
- **[Full Documentation & Data Dictionary](https://example.com/docs)**

---

## ✨ Features

- **Sentiment-Driven Performance Analysis:** Correlates thousands of historical daily closed PnL records and leverage sizes with the Bitcoin Fear & Greed Index.
- **Robust Data Cleansing & Aggregation:** Handles messy historical trade data, intelligently aligns mismatched timeframes, and computes aggregate metrics effortlessly.
- **Advanced Data Visualization:** Delivers clean, compelling charts built with Matplotlib that illustrate complex market dynamics and psychological shifts at a glance.
- **Actionable Behavioral Insights:** Demonstrates that "Greed" phases statistically correspond with higher PnL and increased leverage utilization, while "Fear" phases trigger distinct conservative, risk-averse behavior.

---

## 🛠 Tech Stack

- **Data Manipulation & Processing:** Python, Pandas, NumPy
- **Data Visualization:** Matplotlib
- **Development Environment:** Jupyter Notebooks
- **Data Sources:** Hyperliquid Historical Trader Data (CSV), Alternative.me Crypto Fear & Greed Index (CSV)

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
   - Copy the example `.env` file to set up your environment:
     ```bash
     cp .env.example .env
     ```
   - Update `.env` with your desired configuration or API keys (if shifting to live data fetching).

5. **Run the Analysis:**
   - Launch Jupyter Notebook:
     ```bash
     jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
     ```
   - Make sure `historical_data.csv` and `fear_greed_index.csv` are present in the working directory before executing the cells.

</details>

---

## 🏗 Architecture / How it Works

The pipeline is designed for scalability and accurate time-series analysis:

1. **Data Ingestion:** Historical trade execution details (price, size, side, leverage, PnL) and the daily Bitcoin Fear & Greed Index are loaded from raw `.csv` files.
2. **Preprocessing & Time Alignment:** Time-series data is normalized. Execution timestamps (`Timestamp IST`) are converted and aligned to daily dates.
3. **Merging & Grouping:** The high-frequency trade data is inner-merged with daily sentiment metrics. Grouping logic segments data into distinct market psychological phases (e.g., Extreme Fear, Greed).
4. **Statistical Computation:** Calculates average Closed PnL and Position Size (USD) strictly for closed trades, eliminating open-position noise.
5. **Output & Insights:** Transformed data is fed into Matplotlib to generate visual distributions, clearly mapping the shift in trader behavior against prevailing market conditions.

---

## 💡 Technical Highlights & Learnings

- **Challenge - Time-Series Alignment:** Merging high-frequency asynchronous trade executions with a single daily sentiment metric without introducing look-ahead bias or losing critical granularity.
  - **Solution:** Leveraged Pandas `to_datetime` formatting and explicit date extraction to establish a clean relational key (`date`), ensuring precise inner-joins between massive disparate datasets.
- **Challenge - Isolating Realized PnL:** Raw datasets often contain a mix of open, partially filled, and closed positions, skewing performance metrics.
  - **Solution:** Implemented robust filtering criteria (`merged['Closed PnL'] != 0`) prior to aggregation, guaranteeing that statistical models only reflect finalized financial outcomes.
- **Takeaway:** Building this analytical pipeline reinforced the critical importance of rigorous data preprocessing and index alignment in financial time-series analysis. Clean data architecture is the foundation of trustworthy insights.

---

## 📫 Contact

I am a Software Engineer deeply passionate about data-driven problem solving, clean code architecture, and translating complex metrics into actionable insights. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)
