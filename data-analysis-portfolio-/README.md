# Data Analysis & Visualization Portfolio

**Matias Freer** · Business Intelligence & Data Visualization · AN 306

I use data cleaning, statistical analysis, machine learning, and visualization to turn business questions into evidence-based recommendations. This portfolio presents my contributions to three academic group projects, along with runnable portfolio editions, saved results, and original presentations.

## Explore the projects

| Project | My contribution | Tools |
| --- | --- | --- |
| [Where should a startup recruit its data-science team?](01-hiring-location/) | Data cleaning and visualization | Python, pandas, NumPy, Matplotlib |
| [Can privacy and monetization differentiate a Comics app?](02-app-market/) | Privacy analysis, Random Forest feature importance, monetization analysis, visualization | Python, pandas, SciPy, scikit-learn, Matplotlib |
| [What do META prices reveal about stationarity and momentum?](03-meta-time-series/) | Stationarity, ACF/PACF and initial ARIMA setup, volatility/outliers, moving averages, visualization | Python, pandas, statsmodels, yfinance, Matplotlib |

### Recruiting-location strategy

Cleaned 672 job postings and compared compensation, posting activity, and represented employers. Reproduced the team's Colorado figures: **$103,650 average estimated salary, 10 postings, 6 employers**. The recommendation reflects a business trade-off rather than a uniquely optimal location.

![Screened hiring markets](01-hiring-location/results/market_comparison.png)

### Comics app-market analysis

Examined ratings and success across privacy tiers, compared monetization approaches, and trained a Random Forest to explore predictive features. The original comparison population contains **2,738 Comics apps with positive recorded permission counts**. Maintenance recency and app age have the strongest held-out permutation importance in the portfolio rerun.

![Predictive feature importance](02-app-market/results/feature_importance.png)

### META time-series analysis

Tested stationarity, examined daily returns, and visualized moving-average crossovers. A fixed-date portfolio rerun identifies **17 three-standard-deviation outlier days**. Differencing changes the stationarity-test conclusion; moving averages describe historical momentum rather than guaranteed future direction.

![META return outliers](03-meta-time-series/results/return_outliers.png)

## How to review this work

Each project contains a README, an executed `analysis.ipynb`, a matching `analysis.py`, result tables/charts, the original course notebook with saved outputs, and the original group presentation. The executed portfolio editions incorporate publication improvements; they are not represented as unchanged original submissions. Original group presentations may retain historical drafting artifacts and broader team results.

You can view the notebooks and charts without running anything. To rerun locally:

```bash
python -m pip install -r requirements.txt
cd 01-hiring-location
python analysis.py --input data/Uncleaned_DS_jobs.csv
```

Each project README lists its input and command. Full datasets and Drive archives are excluded. [Data sources and access](DATA-SOURCES.md) explain the course inputs, Kaggle references, and Yahoo Finance download. [Validation and revisions](VALIDATION.md) distinguish reproduced findings, portfolio changes, and limitations.

## Team credits

- **Project 1:** Kaia Hampton, Vincent Guerrero, and Matias Freer.
- **Project 2:** Andrew Bacarella and Matias Freer.
- **Project 3:** Sarah Bottom, Vincent Guerrero, and Matias Freer.

My responsibilities are listed explicitly in each project. Team recommendations remain credited to the team. Collaborators approved public sharing of the group presentations. Dataset authors retain their respective rights; no blanket license is applied to third-party data or shared coursework.
