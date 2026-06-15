<div align="center">

# 📊 Trader Behavior vs. Market Sentiment

**A data-driven analysis uncovering how Bitcoin market sentiment impacts historical trader performance.**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

</div>

---

## 🎨 Visuals

![Demo](./assets/demo.gif)

---

## 🔗 Live Links

- **[Live Deployment / Interactive Notebook](#)** *(Link to live deployment or nbviewer)*
- **[Full Documentation & Data Dictionary](#)** *(Link to docs)*

---

## ✨ Features

- **Sentiment-Driven Performance Analysis:** Correlates daily closed PnL and trade sizes from historical data with the Bitcoin Fear & Greed Index.
- **Robust Data Processing:** Implements a streamlined preprocessing pipeline to handle and align historical trade execution data with daily sentiment metrics.
- **Data Visualizations:** Clean, compelling charts built with Matplotlib that illustrate complex market dynamics and aggregate metrics.
- **Behavioral Insights:** Demonstrates quantifiable shifts in trader behavior, such as higher PnL and larger position sizing during "Greed" phases versus conservative behavior in "Fear" phases.

---

## 🛠 Tech Stack

- **Data Processing & Analysis:** Python, Pandas, NumPy
- **Visualization:** Matplotlib
- **Environment:** Jupyter Notebook

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
   - Copy the example `.env` file to configure any required settings:

     ```bash
     cp .env.example .env
     ```

5. **Run the Notebook:**

   ```bash
   jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
   ```

</details>

---

## 🏗 Architecture / How it Works

1. **Data Ingestion:** Loads historical trade execution details (`historical_data.csv`) and the Bitcoin Fear & Greed Index (`fear_greed_index.csv`) using Pandas.
2. **Preprocessing & Alignment:** Parses timestamps into standardized dates to align high-frequency trading data with the daily sentiment index. The datasets are joined via an inner merge on the date column.
3. **Computation Logic:** Filters out non-closed trades (PnL = 0) and computes aggregates like the average Closed PnL and Position Size (USD) grouped by sentiment classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed).
4. **Output Generation:** Aggregated insights are rendered using Matplotlib to visually illustrate the correlation between market sentiment and trader profitability.

---

## 💡 Technical Highlights & Learnings

- **Challenge:** Effectively aligning asynchronous, high-frequency trade data with daily sentiment metrics.
  - **Solution:** Utilized standard Pandas datetime conversion and merging operations (`pd.to_datetime` and `pd.merge`) to establish a clear daily mapping between trades and sentiment.
- **Challenge:** Identifying actionable behavioral signals within noisy historical trade data.
  - **Solution:** Filtered to focus specifically on realized outcomes (`Closed PnL != 0`) and grouped data by sentiment bands to reveal clear patterns in average profitability and position sizing.
- **Takeaway:** Building this analysis underscored the value of clean data preparation and alignment in uncovering underlying human psychological patterns in financial markets.

---

## 📫 Contact

I am a Software Engineer passionate about data-driven problem solving and writing clean, maintainable code. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)
