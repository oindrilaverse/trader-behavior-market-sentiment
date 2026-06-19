<div align="center">

# 📊 Trader Behavior vs. Market Sentiment

**An advanced, data-driven pipeline analyzing how Bitcoin market sentiment (Fear vs. Greed) directly impacts historical trader performance.**
This project uncovers quantifiable patterns in leverage usage and profitability across market cycles, providing actionable insights into trading psychology and risk management.

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c?style=for-the-badge&logo=python&logoColor=white)](https://matplotlib.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

</div>

---

## 🎨 Visuals

![Demo](./assets/demo.gif)
*(Placeholder for an interactive dashboard or data visualization demo)*

---

## 🔗 Live Links

- **[Live Deployment / Interactive Notebook](https://example.com/live)** *(Coming soon)*
- **[Full Documentation & Data Dictionary](https://example.com/docs)** *(Coming soon)*

---

## ✨ Features

- **Sentiment-Driven Performance Analytics:** Programmatically correlates daily closed PnL, win rates, and leverage ratios with the Bitcoin Fear & Greed Index to extract behavioral alpha.
- **Robust Data Preprocessing:** Engineered a scalable data cleansing pipeline that effectively handles messy, high-frequency historical trade execution data and aligns it with daily sentiment timeframes.
- **Advanced Data Visualizations:** Produces compelling, publication-ready charts using Matplotlib to clearly illustrate complex market dynamics and distribution shifts at a glance.
- **Actionable Behavioral Insights:** Statistically demonstrates that "Greed" phases correspond to elevated leverage usage and risk appetite, while "Fear" phases trigger distinct risk-averse behavior.

---

## 🛠 Tech Stack

### Data Engineering & Analysis
- **Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Visualization:** Matplotlib

### APIs & Data Sources
- **Trade Execution Data:** Hyperliquid Historical Trader API/CSV
- **Market Sentiment:** Alternative.me Crypto Fear & Greed Index API

### Environment
- **Development:** Jupyter Notebooks

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
   source venv/bin/activate  # On Windows: `venv\Scripts\activate`
   ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Environment Variables:**
   - Copy the example environment file:
     ```bash
     cp .env.example .env
     ```
   - Update `.env` with your API keys if you wish to fetch live data rather than using the historical CSVs.

5. **Run the Analysis Locally:**

   ```bash
   jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
   ```

</details>

---

## 🏗 Architecture / How it Works

1. **Data Ingestion:** High-frequency historical trade data (from Hyperliquid) and daily Bitcoin Fear & Greed Index metrics are loaded via raw CSVs or external APIs.
2. **Preprocessing & Alignment:** The raw time-series data is standardized. Timestamps are carefully aligned to merge the granular trade execution data with daily sentiment indices, avoiding look-ahead bias.
3. **Computation Engine:** Complex Pandas aggregations calculate core metrics—such as average PnL, sizing, and win rates—bucketing the data into discrete sentiment thresholds (Extreme Fear, Fear, Neutral, Greed, Extreme Greed).
4. **Visualization Output:** Aggregated metrics are fed into a Matplotlib pipeline to generate visual distributions, clearly showcasing the behavioral shifts of traders under varying market conditions.

---

## 💡 Technical Highlights & Learnings

- **Challenge:** Merging high-frequency, asynchronous trade executions with daily sentiment metrics without losing data granularity or introducing look-ahead bias.
  - **Solution:** Leveraged the Pandas `merge_asof` function and custom temporal grouping logic to accurately attribute each trade to the exact prevailing market sentiment at execution time.
- **Challenge:** Mitigating the impact of extreme outliers (e.g., massive liquidation spikes or API errors) in the historical trade data.
  - **Solution:** Implemented robust statistical filtering techniques (IQR-based clipping) to ensure the final analysis reflected genuine behavioral trends rather than noise.
- **Key Takeaway:** Developing this pipeline reinforced my expertise in time-series analysis, highlighting the importance of writing scalable, deterministic data-cleaning functions for messy real-world datasets.

---

## 📫 Contact

I am a Software Engineer passionate about data-driven problem solving, robust backend systems, and clean architecture. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)
