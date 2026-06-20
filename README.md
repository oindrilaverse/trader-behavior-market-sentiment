<div align="center">

# 📊 Trader Behavior vs. Market Sentiment

**A data-driven analysis of how Bitcoin market sentiment (Fear vs. Greed) impacts historical trader performance.**
This project uncovers patterns in trading behavior, leverage usage, and profitability across different market cycles to provide actionable insights into human psychology in financial markets.

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

- **Sentiment-Driven Performance Analysis:** Correlates daily closed PnL and trade sizing data from traders with the Bitcoin Fear & Greed Index.
- **Data Cleansing & Aggregation:** Robust preprocessing pipeline that handles historical trade data, aligns timeframes, and merges datasets by date.
- **Advanced Visualizations:** Clean, compelling charts built with Matplotlib that illustrate average trader PnL across market sentiment categories at a glance.
- **Behavioral Insights:** Demonstrates that "Extreme Greed" phases correspond with higher average closed PnL and lower average trade sizes compared to "Fear" phases.

---

## 🛠 Tech Stack

- **Language:** Python
- **Data Manipulation & Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib
- **Environment:** Jupyter Notebook
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
   Ensure you have Jupyter, Pandas, and Matplotlib installed:
   ```bash
   pip install pandas numpy matplotlib jupyter
   ```
   *(Or `pip install -r requirements.txt` if available)*

4. **Environment Variables:**
   - Copy the example `.env` file to set up environment variables (if required for live data scraping):
     ```bash
     cp .env.example .env
     ```

5. **Run the Notebook locally:**
   ```bash
   jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
   ```
</details>

---

## 🏗 Architecture / How it Works

1. **Data Ingestion:** Historical trade data (`historical_data.csv`) and the Bitcoin Fear & Greed Index (`fear_greed_index.csv`) are loaded via Pandas.
2. **Preprocessing:** Timestamps are converted into standardized date formats to align high-frequency trade data with daily sentiment indices.
3. **Computation Logic:** Datasets are merged on the exact date. Aggregations using `groupby` compute the average Closed PnL and Size (USD) across sentiment categories (e.g., Extreme Fear, Fear, Neutral, Greed, Extreme Greed).
4. **Output:** Results are plotted using Matplotlib to generate visual distributions, clearly illustrating the shift in trader behavior and profitability under different market conditions.

---

## 💡 Technical Highlights & Learnings

- **Challenge:** Merging disparate datasets (trade execution details vs. daily sentiment index) effectively.
  - **Solution:** Leveraged Pandas `to_datetime` formatting and `.dt.date` accessors to precisely align timestamps and perform an `inner` join. This attributed trades to the exact prevailing sentiment.
- **Challenge:** Extracting meaningful patterns from raw trading records.
  - **Solution:** Filtered for closed trades and utilized grouping aggregations on both the financial outcome (`Closed PnL`) and risk appetite (`Size USD`).
- **Takeaway:** This analysis demonstrated strong competencies in Python data manipulation, showing that technical implementations can successfully map psychological market conditions to concrete financial outcomes.

---

## 📫 Contact

I am a Software Engineer passionate about data-driven problem solving and clean architecture. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)