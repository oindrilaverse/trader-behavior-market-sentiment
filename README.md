<div align="center">

# 📊 Trader Behavior vs. Market Sentiment

**A robust, data-driven pipeline analyzing how Bitcoin market sentiment (Fear vs. Greed) directly impacts historical trader performance.** This project processes high-frequency trading data against daily sentiment indices to uncover actionable insights into leverage usage, risk appetite, and profitability across diverse market cycles.

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c?style=for-the-badge)](https://matplotlib.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

</div>

---

## 🎨 Visuals

![Demo](./assets/demo.gif)
*(A visual demonstration of the interactive notebook and data visualizations)*

---

## 🔗 Live Links

- **[Live Deployment / Interactive Notebook](#)** *(Coming soon)*
- **[Full Documentation & Data Dictionary](#)** *(Coming soon)*

---

## ✨ Features

- **Sentiment-Driven Performance Analysis:** Correlates daily closed PnL and leverage data from high-frequency traders with the broader Bitcoin Fear & Greed Index.
- **Robust Data Cleansing & Aggregation:** Employs advanced preprocessing techniques to clean messy historical trade data, perfectly align timeframes, and aggregate complex trading metrics.
- **Advanced Data Visualizations:** Generates clean, compelling charts to effortlessly communicate complex market dynamics and behavioral trends.
- **Behavioral Insights Engine:** Systematically proves that "Greed" phases correspond with significantly higher PnL and leverage usage, while "Fear" phases trigger conservative, risk-averse behavior.

---

## 🛠 Tech Stack

- **Language:** Python
- **Data Manipulation & Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib
- **Environment:** Jupyter Notebooks
- **Data Sources:** Hyperliquid Historical Trader Data, Alternative.me Crypto Fear & Greed Index

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
   - Copy the example `.env` file to create your local environment file:

     ```bash
     cp .env.example .env
     ```

   - Update `.env` with your relevant API keys if fetching live data (e.g., Hyperliquid API, Alternative.me API).

5. **Run the Notebook:**

   ```bash
   jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
   ```

</details>

---

## 🏗 Architecture / How it Works

The core logic revolves around an asynchronous time-series data alignment pipeline:
1. **Data Ingestion:** Historical trade data (from Hyperliquid) and the Bitcoin Fear & Greed Index are loaded from raw data sources.
2. **Preprocessing & Alignment:** Time-series data is normalized. Dates are meticulously aligned to seamlessly merge high-frequency trade data with aggregate daily sentiment indices.
3. **Computation Logic:** Advanced aggregations calculate average PnL, leverage ratios, and win rates dynamically categorized by specific sentiment thresholds (e.g., Extreme Fear, Neutral, Extreme Greed).
4. **Output Generation:** Processed data is fed into Matplotlib to render clear visual distributions and trend lines, illustrating shifts in trader psychology.

---

## 💡 Technical Highlights & Learnings

- **Challenge:** Merging high-frequency asynchronous trade executions with daily sentiment metrics without losing critical granularity or introducing look-ahead bias.
  - **Solution:** Implemented robust Pandas `merge_asof` and custom grouping logic to accurately attribute trades to the exact prevailing sentiment at execution time, ensuring absolute data integrity.
- **Challenge:** Handling significant outliers and extreme anomalies in historical trade data (such as sudden liquidation spikes).
  - **Solution:** Applied IQR-based filtering alongside custom robust statistical techniques so the final analysis highlights genuine behavioral trends rather than localized noise.
- **Takeaway:** Architecting this data pipeline heavily reinforced the importance of writing scalable data-cleaning functions, avoiding look-ahead bias, and mastering index alignment in complex time-series analysis.

---

## 📫 Contact

I am a Software Engineer deeply passionate about data-driven problem solving, robust backend logic, and clean architecture. I love turning complex data into actionable insights. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)
