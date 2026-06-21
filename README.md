<div align="center">

# 📊 Trader Behavior vs. Market Sentiment

**A robust, data-driven analysis exploring how Bitcoin market sentiment (Fear vs. Greed) quantitatively impacts historical trader performance.**
By systematically correlating trade executions with prevailing market psychology, this project extracts actionable behavioral insights regarding leverage usage, risk appetite, and overall profitability across varying market conditions.

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Data_Visualization-11557c?style=for-the-badge&logo=python&logoColor=white)](https://matplotlib.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

</div>

---

## 🎨 Visuals

<div align="center">
  <img src="./assets/demo.gif" alt="Demo">
</div>

*(Placeholder for actual data visualization/dashboard demo showcasing PnL distributions by sentiment.)*

---

## 🔗 Live Links

- **[Live Deployment / Interactive Dashboard](https://example.com/live)**
- **[Full Documentation & Methodology](https://example.com/docs)**

---

## ✨ Features

- **Sentiment-Driven Performance Analysis:** Statistically correlates daily closed PnL and trade sizing metrics from over 200,000 executed trades with the Bitcoin Fear & Greed Index.
- **Robust Data Pipeline:** Engineered a data cleansing and aggregation workflow that normalizes messy historical execution data, strictly aligns asynchronous timeframes, and calculates precise aggregate metrics.
- **Actionable Behavioral Insights:** Empirically demonstrates that "Greed" phases correspond with significantly higher average PnL and elevated risk profiles, while "Extreme Fear" phases consistently trigger defensive, risk-averse trading strategies.
- **Advanced Visualizations:** Leverages comprehensive Matplotlib charting to clearly communicate complex time-series dynamics and market psychologies to non-technical and technical stakeholders alike.

---

## 🛠 Tech Stack

- **Data Science & Analysis:** Python 3, Pandas, NumPy
- **Data Visualization:** Matplotlib
- **Development Environment:** Jupyter Notebook
- **Data Integrations / APIs:** Hyperliquid Historical Trader Data, Alternative.me Crypto Fear & Greed Index

---

## 🚀 Installation & Setup

<details>
<summary><b>Click here to view step-by-step setup instructions</b></summary>
<br>

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/trader-behavior-market-sentiment.git
   cd trader-behavior-market-sentiment
   ```

2. **Set up the virtual environment:**

   It is recommended to use an isolated environment to prevent dependency conflicts.
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use: `venv\Scripts\activate`
   ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Environment Variables:**

   To fetch real-time data or refresh the sentiment index, configure your environment variables.
   ```bash
   cp .env.example .env
   ```
   *Edit `.env` to include your required API keys (e.g., `HYPERLIQUID_API_KEY`).*

5. **Run the Notebook:**

   Launch Jupyter to interactively run the pipeline and view visualizations.
   ```bash
   jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
   ```

</details>

---

## 🏗 Architecture / How it Works

The project follows a linear, highly reproducible ETL (Extract, Transform, Load) paradigm built directly into a Jupyter Notebook:

1. **Data Ingestion:** High-frequency historical trade execution data (from Hyperliquid) and daily Bitcoin Fear & Greed indices are loaded.
2. **Preprocessing & Alignment:** UNIX timestamps and localized date formats are parsed and rigorously normalized. Dataframes are securely joined on corresponding execution dates to prevent look-ahead bias.
3. **Core Computation:** Grouping logic aggregates the aligned dataset by distinct sentiment classifications (e.g., Extreme Fear vs. Extreme Greed), systematically calculating mean performance and average risk allocation.
4. **Visualization Layer:** Transformed aggregations are directly piped into Matplotlib to generate intuitive bar charts and distributional analyses, exposing the underlying market narratives.

---

## 💡 Technical Highlights & Learnings

- **Challenge: Time-Series Data Alignment**
  - *Context:* Merging high-frequency, minute-by-minute asynchronous trade executions with a daily-resolution sentiment metric risks losing data granularity or introducing critical misalignments.
  - *Solution:* Implemented precise datetime transformations and deterministic Pandas merging strategies to accurately attribute every distinct trade to the exact prevailing market sentiment at the time of execution.
- **Challenge: Anomaly Handling in Financial Data**
  - *Context:* Raw cryptocurrency trading data contains extreme outliers such as liquidation cascades and API artifacts that severely skew aggregate means.
  - *Solution:* Utilized robust exploratory data analysis (EDA) techniques to identify and filter anomalous records, ensuring that the computed sentiment trends reflected genuine human behavior rather than statistical noise.
- **Takeaway:** Developing this analytical pipeline deeply reinforced my expertise in writing scalable, memory-efficient Pandas transformations and highlighted the critical importance of rigorous index alignment in time-series forecasting and behavioral analysis.

---

## 📫 Contact

I'm a Data-Driven Software Engineer passionate about translating complex datasets into clean, actionable architectures. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)
