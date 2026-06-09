<div align="center">

# 📊 Trader Behavior vs. Market Sentiment

**A rigorous data-driven exploration of how Bitcoin market sentiment (Fear vs. Greed) fundamentally impacts historical trader performance and profitability.**
This project bridges the gap between raw trading data and human psychology, uncovering critical patterns in risk management, leverage usage, and decision-making across different market cycles.

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Data_Vis-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://matplotlib.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

</div>

---

## 🎨 Visuals

![Demo](./assets/demo.gif)
*(Placeholder for an interactive data visualization or dashboard showcasing key findings)*

---

## 🔗 Live Links

- **[Live Deployment / Interactive Dashboard](#)** *(Coming soon)*
- **[Full Documentation & Data Dictionary](#)** *(Coming soon)*

---

## ✨ Features

- **Sentiment-Driven Performance Analysis:** Correlates daily closed PnL and position sizing with the Bitcoin Fear & Greed Index to establish actionable insights.
- **Robust Data Pipeline:** Efficiently ingests, cleanses, and merges disjointed historical trade logs with daily sentiment indices utilizing advanced Pandas operations.
- **Actionable Visualizations:** Generates clean, intuitive charts built with Matplotlib that communicate complex market dynamics and behavioral shifts at a glance.
- **Behavioral Insights Generation:** Quantifiably demonstrates how varying market phases ("Greed" vs. "Fear") dictate trader profitability and risk appetite.

---

## 🛠 Tech Stack

- **Language:** Python 3.8+
- **Data Manipulation & Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib
- **Environment:** Jupyter Notebooks
- **Core Dependencies:** Detailed in `requirements.txt`

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

2. **Set up a virtual environment (Recommended):**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Environment Variables:**
   - Copy the example `.env` file to set up your environment:

     ```bash
     cp .env.example .env
     ```

   - *Note: Update the `.env` file with any required API keys if extending the pipeline to fetch live data.*

5. **Run the Analysis:**
   - Launch Jupyter Notebook to interact with the data pipeline:

     ```bash
     jupyter notebook Trading_Behaviour_vs_Market_Sentiment.ipynb
     ```

</details>

---

## 🏗 Architecture / How it Works

1. **Data Ingestion:** Loads granular historical trade data (`historical_data.csv`) and daily sentiment metrics (`fear_greed_index.csv`).
2. **Preprocessing & Alignment:** Standardizes diverse timestamp formats into structured datetime objects. Performs precision merging on dates to align high-frequency trades with daily sentiment scores.
3. **Computation Logic:** Filters out noise (e.g., open trades) and groups data by sentiment classifications. Calculates core metrics such as average Profit and Loss (PnL) and average position size (Size USD).
4. **Visualization:** Leverages Matplotlib to plot the average trader PnL across different market sentiment buckets, translating raw numbers into a clear visual narrative.

---

## 💡 Technical Highlights & Learnings

- **Challenge:** Aligning high-frequency, irregularly spaced trade executions with a daily-resolution sentiment index without losing data fidelity or introducing bias.
  - **Solution:** Implemented efficient datetime normalization and inner merge operations using Pandas, ensuring that every closed trade was accurately mapped to the prevailing market sentiment of that exact day.
- **Challenge:** Managing and aggregating a dataset containing highly variable PnL and position sizes, which could skew analytical results.
  - **Solution:** Utilized strategic grouping and robust statistical averaging to abstract away individual trade noise, yielding statistically significant insights into aggregate trader behavior.
- **Takeaway:** Building this pipeline reinforced my proficiency in Pandas for complex data wrangling and highlighted the importance of clean, maintainable code when deriving insights from messy, real-world financial data.

---

## 📫 Contact

I am a Software Engineer passionate about data-driven problem solving, robust architecture, and translating complex data into actionable insights. Let's connect!

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Portfolio:** [yourportfolio.dev](https://yourportfolio.dev)
- **Email:** [your.email@example.com](mailto:your.email@example.com)