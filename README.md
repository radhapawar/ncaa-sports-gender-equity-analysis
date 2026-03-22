# College Sports Analytics — Title IX & Gender Equity in NCAA Athletics

**Course:** MSBA Data Science Project
**Team:** Caraher, Korvink, Therrien, Zhu, Pawar

## Overview

This project analyzes NCAA college sports data to examine gender equity in athletic participation, revenue, and expenditure across U.S. universities. Motivated by Title IX legislation, the analysis explores trends in men's vs. women's sports participation, financial investment patterns, and predictive modeling of program outcomes.

## Key Analyses

- **Participation Trends:** Year-over-year changes in men's and women's college sports participation (2015–2019)
- **Revenue & Expenditure Analysis:** Comparison of financial investment across gender and sport classification
- **Gender Participation Ratio:** State-level and classification-level breakdown of men-to-women participation ratios
- **Regression Modeling:** Linear regression to predict participation or financial outcomes from program characteristics
- **Trend Forecasting:** Time-series analysis of participation growth rates

## Files

| File | Description |
|------|-------------|
| `DS Project.ipynb` | Main analysis notebook (EDA, modeling, visualization) |
| `code for trends.ipynb` | Trend analysis and time-series code |
| `rev_exp_partic.ipynb` | Revenue, expenditure, and participation deep-dive |
| `sports.csv` | NCAA college sports dataset |
| `title9.pdf` | Title IX reference document |
| `DS Project Slides.pptx` | Final presentation slides |
| `Project_CaraherKorvinkTherrienZhuPawar.docx` | Written project report |

## Technologies

- Python (pandas, numpy, matplotlib, seaborn, scikit-learn)
- Jupyter Notebook

## How to Run

1. Install dependencies: `pip install pandas numpy matplotlib seaborn scikit-learn`
2. Open `DS Project.ipynb` in Jupyter or VS Code
3. Ensure `sports.csv` is in the same directory (or update the data loading path)
4. Run all cells top to bottom

## Key Findings

- Women's sports participation grew faster than men's from 2016–2018, though overall male participation remained higher by 100k+
- A decline in participation was observed in 2018–2019, possibly linked to budget cuts and Title IX compliance pressures
- Significant variation in gender participation ratios across states and athletic classifications
