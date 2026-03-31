# Title IX & Gender Equity in NCAA Athletics: Data Analysis

**Team:** Caraher, Korvink, Therrien, Zhu, Pawar
**Data:** NCAA EADA (Equity in Athletics Disclosure Act) dataset, 2015–2019

---

Title IX is 50+ years old. The law is clear. And yet the gap between men's and women's athletics funding at American universities remains enormous. We wanted to understand what's actually driving that gap, not just confirm it exists, but figure out *why*, and whether it's getting better or worse.

The EADA data is publicly filed by every university that receives federal funding. It covers participation counts by gender and sport, revenue, expenditure, and recruiting budgets for every year. It's one of the most complete longitudinal datasets on institutional gender equity that exists in public data, and it's almost never used for anything beyond basic compliance reporting.

## The headline finding

**The gender funding gap in college athletics is primarily a revenue sport problem, not a structural discrimination problem.**

When you look at Division III schools, with no football and no major basketball revenue, the gender expenditure gap is relatively small. When you look at Division I schools with major football programs, the gap is enormous: men's programs received on average **2.3x the expenditure** of women's programs, and recruiting budgets were **3.1x** higher.

Football and basketball generate most of the revenue at large programs. That revenue gets classified as sport-specific and cycled back into football and basketball. Everything else, including all women's sports, gets funded from the general athletics budget.

The implication: you can mandate equal treatment across individual sports all you want, but until you change how football and basketball revenue gets distributed within athletics departments, the structural imbalance remains.

## Year by year

Women's participation grew faster than men's from 2016–2018 in both absolute numbers and rate of change — Title IX working as intended. But the absolute gap didn't close much. Male participation was consistently ~100,000 athletes higher across all years.

The 2018–2019 data showed a drop in participation across both genders. Our time series model (trained on 2015–2018) overestimated 2019 participation by ~8% — a meaningful miss. It suggests 2018–2019 was a structural break rather than random noise, likely tied to budget pressures and Title IX compliance restructuring at mid-size programs. A linear trend model can't capture that kind of discontinuity.

## The regression

We predicted the gender participation ratio and expenditure gap from institutional characteristics.

Athletic classification (Division I/II/III) was the single strongest predictor, contributing about 41% of the explained variance in expenditure ratios. Football revenue was also a significant predictor after controlling for classification, directly supporting the revenue-sport thesis. Private institutions showed more balanced ratios than public institutions at the same classification level, possibly because they face less political pressure around football programs.

## Caveats

EADA data is self-reported, which means it's as good as each institution's accounting practices. There's real variation in how schools classify revenues and expenses across sports, which limits direct comparisons. We normalized for inflation and used classification-level controls to reduce this, but it's worth keeping in mind.

Five years (2015–2019) is enough to identify trends and build a regression, but not enough to make confident long-range forecasts. A 10-year dataset would be significantly more useful for the time series component.

## Running the analysis

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
Jupyter Notebook "DS Project.ipynb."
```

`sports.csv` should be in the same directory. Run notebooks in order — `DS Project.ipynb` for the main analysis, `code for trends.ipynb` for time series, `rev_exp_partic.ipynb` for the revenue deep dive.

## Files

| File | Description |
|---|---|
| `DS Project.ipynb` | Main EDA, regression, visualizations |
| `code for trends.ipynb` | Time series analysis and forecasting |
| `rev_exp_partic.ipynb` | Revenue, expenditure, and participation deep-dive |
| `sports.csv` | The EADA dataset |
| `DS Project Slides.pptx` | Final presentation deck |
| `Project_CaraherKorvinkTherrienZhuPawar.docx` | Written report |
