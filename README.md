# Forecasting Emerging Tech Occupations in New Brunswick  
### Capstone Project — Data Analytics & AI

This project analyzes employment trends in technology-related occupations in New Brunswick (NB), Canada, using public data from Statistics Canada. It combines data processing, exploratory analysis, machine learning forecasting, and generative AI to identify which tech occupations are emerging and how they are expected to evolve in the coming years.

---

## Project Goal

The central research question:

**Which technology-related occupations are emerging in New Brunswick, and how can we forecast their future trends using historical labor market data?**

The project aims to:

- Identify growth patterns in STEM and tech occupations  
- Compare tech-sector trends with other major sectors  
- Build predictive models to forecast future employment  
- Generate automated insights using LLMs  
- Produce a complete, reproducible analytics pipeline  

---

## Key Research Questions

- Which STEM occupations show consistent growth in NB?  
- How does tech-sector growth compare to health, finance, trades, and service sectors?  
- What economic factors may influence these trends?  
- What are the predicted employment levels for tech occupations in the coming years?  
- How can generative AI support interpretation and reporting?  

---
```bash
capstone-nb-job-trends
│
├── data
│   ├── raw/          # Original datasets (unchanged)
│   ├── interim/      # Intermediate cleaned datasets
│   └── processed/    # Final datasets ready for modeling
│
├── notebooks
│   ├── 01_data_cleaning.ipynb
│   ├── 02_eda_and_features.ipynb
│   └── 03_modeling_and_forecast.ipynb
│
├── src
│   ├── data_cleaning.py
│   ├── feature_engineering.py
│   ├── modeling.py
│   └── utils.py
│
├── models/           # Trained ML models
├── figures/          # Visualizations and plots
│
├── report
│   ├── capstone_report.md
│   └── capstone_slides.pdf
│
├── requirements.txt
└── README.md
```
---

## Data Sources

### Primary Dataset — Statistics Canada  
**Table 14-10-0416-01 — Labour force characteristics by occupation, annual**

Key dimensions:

- Province: New Brunswick  
- Occupation (NOC)  
- Employment (persons in thousands)  
- Year  

Dataset size: approximately **534,000 rows (~113 MB)**.

### Tech/STEM Occupations of Interest

- 212 — Professional occupations in applied sciences (IT, software, data)  
- 213 — Engineering occupations  
- 22 — Technical occupations in natural and applied sciences  

### Comparison Groups

- 11 — Finance and business  
- 31 — Health  
- 62–65 — Sales and services  
- 72–75 — Trades  

### Additional Economic Context (Statistics Canada)

- Income distribution  
- Income mobility  
- Employment income by age and sex  

These datasets support contextual modeling and interpretation.

---

## Tools and Technologies

- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn, Plotly  
- Scikit-learn  
- Statsmodels (optional)  
- Jupyter Notebooks  
- Generative AI (LLMs) for insights and reporting  

---

## Project Pipeline

### 1. Data Ingestion
- Import raw CSVs from Statistics Canada  
- Store in `data/raw/`  

### 2. Data Cleaning
- Filter for:
  - New Brunswick  
  - Total gender  
  - Employment as the labor force characteristic  
- Select relevant columns:
  - REF_DATE, Occupation, VALUE  

### 3. Feature Engineering
- Create analytical variables:
  - growth_rate  
  - tech_indicator  
  - sector_group  
  - rolling_mean  
  - year_over_year_change  

### 4. Exploratory Data Analysis
- Trend analysis by occupation  
- Sector comparisons  
- Time-series visualizations  
- Outlier detection and pattern identification  

### 5. Machine Learning & Forecasting
Models considered:

- Linear Regression  
- Random Forest Regressor  
- K-Means Clustering for occupation grouping  
- Time-series forecasting (regression-based or hybrid approaches)  

### 6. Generative AI Integration
LLMs are used to:

- Generate narrative insights from visualizations  
- Summarize trends and findings  
- Assist in writing the final report  
- Provide automated interpretations of model outputs  

---

## Expected Outcomes

- Identification of emerging tech occupations in NB  
- Clear comparison between STEM and non-STEM sectors  
- Forecasts of future employment trends  
- Professional visualizations  
- AI-generated insights and summaries  
- A complete, reproducible analytics workflow  

---

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/edhdevps/capstone-nb-job-trends.git
cd capstone-nb-job-trends

python -m venv venv
venv\Scripts\activate

pip install -r requirements.txt
jupyter notebook
```

