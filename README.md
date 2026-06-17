<div align="center">

# 📊 Trader Behavior vs. Market Sentiment

**A robust, data-driven analysis of how Bitcoin market sentiment (Fear vs. Greed) directly impacts historical trader performance and behavior.**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

</div>

---

## 🎨 Visuals

![Demo](./assets/demo.gif)
*(Placeholder for data visualization dashboard demo)*

---

## 🔗 Live Links

- **[Live Interactive Notebook](https://example.com/live)** *(Coming soon)*
- **[Full Documentation & Data Dictionary](https://example.com/docs)** *(Coming soon)*

---

## ✨ Features

- **Sentiment-Driven Performance Analysis:** Correlates daily closed PnL (Profit and Loss) and position sizing data from traders with the Bitcoin Fear & Greed Index to extract actionable behavioral insights.
- **Robust Data Cleansing & Aggregation:** Employs advanced Pandas preprocessing pipelines to handle messy historical, high-frequency trade data, align timestamps, and compute aggregate metrics without look-ahead bias.
- **Advanced Statistical Visualizations:** Generates clean, compelling charts using Matplotlib to effectively communicate complex market dynamics and shifts in human psychology.
- **Behavioral Insights Generation:** Uncovers key findings, such as the tendency for "Greed" phases to correspond with higher PnL and leverage usage, while "Fear" phases trigger conservative, risk-averse behavior.

---

## 🛠 Tech Stack

- **Data Manipulation & Analysis:** Python, Pandas, NumPy
- **Data Visualization:** Matplotlib
- **Development Environment:** Jupyter Notebooks
- **Data Sources:** Hyperliquid Historical Trader Data, Alternative.me Crypto Fear & Greed Index

---

## 🚀 Installation & Setup

<details>
<summary><b>Click here to view detailed step-by-step setup instructions</b></summary>
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
   - Copy the example `.env` file to set up your local configuration:

     ```bash
     cp .env.example .env
     ```

   - Update `.env` with your relevant API keys if fetching live data (e.g., Hyperliquid API, Alternative.me API).

5. **Run the Analysis:**

   ```bash
   jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
   ```

</details>

---

## 🏗 Architecture / How it Works

1. **Data Ingestion:** Historical trade execution data (from Hyperliquid) and daily Bitcoin Fear & Greed Index values are loaded from raw CSV files.
2. **Preprocessing & Alignment:** Time-series data is normalized. High-frequency asynchronous trade executions are merged with daily sentiment indices using Pandas' `merge` operation, accurately attributing trades to the prevailing sentiment at execution time.
3. **Computation Logic:** Aggregations are performed to calculate average PnL, position sizing (Size USD), and trading behavior categorized by sentiment thresholds (e.g., Extreme Fear, Fear, Neutral, Greed, Extreme Greed).
4. **Data Visualization:** The processed data is fed into Matplotlib to generate visual distributions and trend lines, clearly illustrating the behavioral shifts across different market cycles.

---

## 💡 Technical Highlights & Learnings

- **Challenge:** Accurately merging high-frequency asynchronous trade executions with daily sentiment metrics without losing critical granularity or introducing look-ahead bias.
  - **Solution:** Designed and implemented a robust timestamp alignment pipeline utilizing Pandas, ensuring trades were accurately attributed to the exact prevailing sentiment on the execution date.
- **Challenge:** Handling outliers, messy timestamps, and data anomalies inherent in historical trade datasets (e.g., liquidation spikes).
  - **Solution:** Applied robust data-cleaning techniques, including parsing inconsistent date formats and filtering anomalies, to ensure the final statistical analysis reflected genuine behavioral trends rather than noise.
- **Key Takeaway:** Architecting this analysis pipeline reinforced the importance of writing scalable, clean data-processing functions and maintaining a rigorous approach to index alignment in time-series data modeling.

---

## 📫 Contact

I am a Software Engineer passionate about data-driven problem solving, clean architecture, and building impactful products. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)
