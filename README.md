<div align="center">

# Trader Behavior vs. Market Sentiment

A data-driven analysis of how Bitcoin market sentiment (Fear vs. Greed) impacts historical trader performance, uncovering patterns in trading behavior, position sizing, and profitability.

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

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

- **Sentiment-Driven Performance Analysis:** Correlates daily closed PnL and trade position sizes from traders with the Bitcoin Fear & Greed Index.
- **Data Cleansing & Aggregation:** A streamlined preprocessing pipeline that handles raw historical trade data, aligns timeframes, and computes aggregate metrics.
- **Advanced Visualizations:** Compelling charts built with Matplotlib that illustrate complex market dynamics at a glance.
- **Behavioral Insights:** Demonstrates that "Greed" phases correspond with higher PnL and larger position sizes, while "Fear" phases trigger conservative, risk-averse behavior.

---

## Tech Stack

- **Language:** Python
- **Data Manipulation & Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib
- **Environment:** Jupyter Notebooks

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

   - Update `.env` with your API keys if you wish to fetch live data.

5. **Run the Notebook:**

   ```bash
   jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
   ```

</details>

---

## Architecture / How it Works

1. **Data Ingestion:** Historical trade data and the Bitcoin Fear & Greed Index are loaded from raw CSVs.
2. **Preprocessing:** Time-series data is normalized. Dates are aligned to merge high-frequency trade data with daily sentiment indices.
3. **Computation Logic:** Aggregations are performed to calculate average PnL and average trade sizes categorized by sentiment thresholds (Extreme Fear, Fear, Neutral, Greed, Extreme Greed).
4. **Output:** The grouped data is visualized using Matplotlib to generate visual distributions and trend lines, clearly illustrating the shift in trader behavior.

---

## Technical Highlights & Learnings

- **Challenge:** Merging high-frequency asynchronous trade executions with daily sentiment metrics without losing critical granularity.
  - **Solution:** Implemented standard Pandas operations including an `inner merge` on aligned date columns to accurately attribute trades to the exact prevailing sentiment at execution time.
- **Challenge:** Filtering raw historical trade data to extract meaningful performance metrics.
  - **Solution:** Used Pandas `filtering` (e.g., isolating closed trades where PnL != 0) and `groupby` aggregations to ensure the final analysis accurately reflected genuine behavioral trends rather than noise.
- **Takeaway:** Building this pipeline reinforced the importance of standardizing data processing techniques, establishing a strong foundation in applying Pandas efficiently for time-series analysis and merging datasets.

---

## Contact

I am a Software Engineer passionate about data-driven problem solving and clean architecture. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)