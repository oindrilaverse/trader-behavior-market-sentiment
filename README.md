<div align="center">

# 📈 Market Sentiment & Trader Performance Analysis

**An end-to-end data analytics pipeline that measures how the Bitcoin Fear & Greed Index influences trader leverage, risk appetite, and profitability.**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-white?style=for-the-badge&logo=python)](https://matplotlib.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

</div>

---

## 🎨 Visuals

![Demo](./assets/demo.gif)

---

## 🔗 Live Links

- **[Interactive Project / Live Deployment](https://example.com/live)**
- **[Full API Documentation](https://example.com/docs)**

---

## ✨ Features

- **Sentiment-Driven Insights:** Directly correlates historical trader execution metrics (like leverage and closed PnL) against broader market psychology indicators.
- **Robust Data Preprocessing:** Programmatically cleans high-frequency trade data, handles anomalies, and reliably aligns asynchronous time-series data.
- **Advanced Visualizations:** Uses Matplotlib to generate highly readable, compelling visual distributions of trader behavior during different market cycles.
- **Behavioral Profiling:** Mathematically demonstrates the increase in trader leverage during "Greed" phases versus conservative positioning during "Fear" phases.

---

## 🛠 Tech Stack

- **Data Engineering:** Python, Pandas, NumPy
- **Data Visualization:** Matplotlib
- **Development Environment:** Jupyter Notebook
- **External APIs:** Hyperliquid Historical Trade Data, Alternative.me Crypto Fear & Greed Index

---

## 🚀 Installation & Setup

<details>
<summary><b>Click here to view detailed setup instructions</b></summary>
<br>

**1. Clone the repository:**
```bash
git clone https://github.com/yourusername/trader-behavior-market-sentiment.git
cd trader-behavior-market-sentiment
```

**2. Setup a virtual environment:**
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

**3. Install dependencies:**
```bash
pip install -r requirements.txt
```

**4. Environment Variables:**
Ensure you have the required API keys setup by copying the example environment file:
```bash
cp .env.example .env
```

**5. Run the Jupyter Notebook locally:**
```bash
jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
```
</details>

---

## 🏗 Architecture / How it Works

1. **Data Ingestion:** High-frequency trade execution logs and daily market sentiment data are pulled into the pipeline.
2. **Transformation & Alignment:** Trade execution dates are extracted and standardized. The trade data is merged with the daily sentiment data to map each individual trade to the market psychology of that exact day.
3. **Filtering & Aggregation:** Zero-PnL trades are rigorously filtered to remove noise. The pipeline groups the remaining data into distinct sentiment classifications to compute mean statistics for leverage and trade sizes.
4. **Presentation:** The aggregated findings are visualized using Matplotlib charts.

---

## 💡 Technical Highlights & Learnings

- **Challenge:** Accurately associating individual trade executions with daily sentiment classifications without introducing data misalignment or look-ahead bias.
  - **Solution:** Implemented robust Pandas `merge` operations on matching date columns, alongside carefully designed grouping logic, to ensure perfectly synchronized time-series analysis.
- **Challenge:** Managing significant noise in the historical trade data, specifically regarding inactive positions.
  - **Solution:** Applied strict filtering mechanisms to isolate and remove zero PnL trades before performing statistical aggregations, ensuring that final insights reflect genuine trader decisions rather than dataset artifacts.
- **Takeaway:** Architecting this pipeline fundamentally reinforced my expertise in data wrangling, handling missing variables, and maintaining structural integrity when joining complex time-series datasets.

---

## 📫 Contact

I'm a Software Engineer who loves turning messy data into clean architectures and actionable insights. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)
