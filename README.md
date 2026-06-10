<div align="center">

# 📊 Trader Behavior vs. Market Sentiment

**A data-driven analysis of how Bitcoin market sentiment (Fear vs. Greed) impacts historical trader performance.**
This project uncovers patterns in trading behavior, leverage usage, and profitability across different market cycles to provide actionable insights into human psychology in financial markets.

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c?style=for-the-badge&logo=python&logoColor=white)](https://matplotlib.org/)
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

- **Sentiment-Driven Performance Analysis:** Correlates daily closed PnL and size metrics from traders with the Bitcoin Fear & Greed Index.
- **Data Cleansing & Aggregation:** Preprocessing pipeline that parses string timestamps, aligns timeframes, and filters relevant historical trade records.
- **Advanced Visualizations:** Clean, compelling charts built with Matplotlib that illustrate complex market dynamics and average PnL by sentiment classification at a glance.
- **Behavioral Insights:** Demonstrates how trader performance, size, and PnL differ across varying market sentiment phases (Fear vs. Greed).

---

## 🛠 Tech Stack

- **Language:** Python
- **Data Manipulation & Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib
- **Environment:** Jupyter Notebook
- **Data Sources:** Historical Trader Data (`historical_data.csv`), Crypto Fear & Greed Index (`fear_greed_index.csv`)

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

   - Update `.env` with your API keys if you wish to fetch live data instead of using the provided CSV datasets.

5. **Run the Notebook:**

   ```bash
   jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
   ```

</details>

---

## 🏗 Architecture / How it Works

1. **Data Ingestion:** Historical trade data (`historical_data.csv`) and the Bitcoin Fear & Greed Index (`fear_greed_index.csv`) are loaded into Pandas DataFrames.
2. **Preprocessing:** Time-series data is normalized. Specifically, string timestamps (`Timestamp IST` with format `%d-%m-%Y %H:%M`) are parsed, and the date component is extracted to prepare for merging with daily sentiment indices.
3. **Computation Logic:** The datasets are inner-joined on the `date` column. Realized trades are isolated by filtering out open or unrealized positions (where `Closed PnL != 0`). Aggregations (like `mean()`) are performed on `Closed PnL` and `Size USD`, grouped by the sentiment `classification`.
4. **Output:** The aggregated data is fed into Matplotlib to generate visual distributions, such as bar charts comparing Average PnL by Market Sentiment.

---

## 💡 Technical Highlights & Learnings

- **Challenge:** Merging high-frequency asynchronous trade executions with daily sentiment metrics without losing critical data or introducing errors.
  - **Solution:** Standardized the temporal resolution by cleanly parsing complex string timestamps (`%d-%m-%Y %H:%M`) and extracting just the date component. This allowed for an accurate, deterministic inner join on the `date` key between the high-frequency trading dataframe and the daily sentiment dataframe.
- **Challenge:** Accurately calculating final PnL averages without skewing results with ongoing or unrealized positions.
  - **Solution:** Applied strict filtering logic (`Closed PnL != 0`) to extract only finalized trades. By doing so, the statistical aggregations (`mean()`) grouped by sentiment classifications precisely reflect actual realized trader performance rather than floating PnL fluctuations.

---

## 📫 Contact

I am a Software Engineer passionate about data-driven problem solving and clean architecture. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)
