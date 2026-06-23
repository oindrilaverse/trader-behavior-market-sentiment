<div align="center">

# 📊 Trader Behavior vs. Market Sentiment

**A data-driven analysis exploring how Bitcoin market sentiment (Fear vs. Greed) influences historical trader performance, leverage, and behavior.**
This project bridges the gap between raw trading data and behavioral finance, providing actionable insights into human psychology in crypto markets.

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

- **Sentiment-Driven Performance Analysis:** Correlates daily closed PnL and trade sizes from historical traders directly with the Bitcoin Fear & Greed Index.
- **Data Preprocessing & Normalization:** Employs precise datetime parsing to align asynchronous and diverse timestamp formats into a unified daily grain.
- **Actionable Visualizations:** Leverages Matplotlib to generate intuitive bar charts illustrating average PnL segmented by market sentiment phases.
- **Behavioral Insights:** Empirically demonstrates the relationship between market sentiment phases (like "Fear" or "Greed") and trader behavior, highlighting shifts in profitability and leverage scaling.

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
   - Copy the example `.env` file to set up necessary variables (if applicable to your local setup):

     ```bash
     cp .env.example .env
     ```

5. **Run the Notebook:**

   ```bash
   jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
   ```

</details>

---

## Architecture / How it Works

1. **Data Ingestion:** Loads historical trading logs (`historical_data.csv`) and sentiment index data (`fear_greed_index.csv`) using Pandas.
2. **Preprocessing & Alignment:** Raw datetime strings (e.g., `Timestamp IST` in custom format) are parsed and truncated to daily dates to ensure accurate alignment between independent datasets.
3. **Computation Logic:** The datasets are joined with an inner merge on the newly aligned daily dates. Non-realized data is filtered out (retaining only trades where `Closed PnL != 0`).
4. **Aggregation & Output:** The cleaned dataset is aggregated using standard Pandas grouping functions (`groupby`) to calculate the mean `Closed PnL` and `Size USD` corresponding to specific market sentiment classifications (e.g., Fear, Greed), ultimately outputting bar charts via Matplotlib.

---

## Technical Highlights & Learnings

- **Challenge:** Merging granular, asynchronous trade execution timestamps with daily-level market sentiment metrics without data loss or misalignment.
  - **Solution:** Implemented clean and rigorous date parsing using `pd.to_datetime` with explicit formatting logic (e.g., `%d-%m-%Y %H:%M`). By isolating the `.dt.date` component, I was able to successfully perform a clean standard inner merge across both datasets on a unified daily index.
- **Challenge:** Isolating true realized outcomes from ongoing, open position noise in the historical trade logs.
  - **Solution:** Applied strict filtering conditions (e.g., `Closed PnL != 0`) prior to performing groupings and aggregations to guarantee that the final analytics reflected realized PnL and definitive behavioral outcomes rather than unclosed position volatility.
- **Takeaway:** Building this analysis reinforced the importance of meticulous data cleaning and index normalization when blending disparate time-series sources, laying the groundwork for robust behavioral finance insights.

---

## Contact

I am a Software Engineer passionate about data-driven problem solving and clean, maintainable architecture. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)
