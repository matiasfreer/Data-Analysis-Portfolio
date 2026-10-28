# Data sources and access

Raw datasets and full price snapshots are excluded from this repository. The saved result tables and figures document the runs. Run commands below assume you work inside the relevant project folder.

## Job-posting analysis

Input: `data/Uncleaned_DS_jobs.csv`, 672 rows in the supplied course file. This is the input used for the verified portfolio rerun. Matias supplied these course references:

- [Data cleaning and transformation (DataScienceJobs)](https://www.kaggle.com/code/ikromjonovhojiakbar/data-cleaning-and-transformation-datasciencejobs), ikromjonovhojiakbar.
- [Data Cleaning - Data Science Job Posting](https://www.kaggle.com/code/erastusirungu/data-cleaning-data-science-job-posting), erastusirungu.

These are notebook references; the exact underlying dataset version and redistribution license were not verified. They are not represented as two separate input datasets. Obtain the original course CSV or the corresponding input dataset through those notebook pages. Any adapted reference code should retain its attribution.

## App-market analysis

Upstream sources supplied by Matias:

- [Google Play Store Apps](https://www.kaggle.com/datasets/gauthamp10/google-playstore-apps), gauthamp10.
- [Android Permissions Dataset](https://www.kaggle.com/datasets/gauthamp10/app-permissions-android), gauthamp10.

**Matias began with the already-joined dataset supplied by the professor.** He does not claim the upstream join as his individual work. The portfolio script uses the corresponding cleaned/engineered file `data/Andrew_Clean_Dataset.csv` (2,312,832 rows). The original notebook documents feature construction from the joined CSV. The course-derived cleaned file is not hosted here; its exact transformations and historical counts should not be inferred from a new Kaggle download alone.

The supplied cleaned input has duplicate permission-flag column names. The portfolio script uses only unambiguous feature/label columns, reads in chunks, validates app uniqueness and success labels, and explicitly selects Comics apps with positive recorded permission counts. It does not repair or infer raw join membership.

There are 2,862 Comics apps in this input; 2,738 have positive recorded permission counts and match the population used in the original analysis. Monetization results for all 2,862 apps are saved separately as a sensitivity comparison.

The two later ZIP uploads were duplicate copies of Google-Playstore.csv; neither contained the raw permissions JSON. Raw sources are not necessary to rerun from the supplied cleaned course input, but are necessary to independently rebuild the upstream join.

Check the license accompanying the exact Kaggle download version before redistributing raw or derived data. Dataset licenses and this repository's authorship are distinct; no blanket repository license is asserted for the group materials.

## META time series

Source: Yahoo Finance via `yfinance`, ticker META. The original course notebook downloaded prices with an open-ended request. Its original full price snapshot was not supplied, so the historical saved outputs are preserved separately.

The portfolio edition was downloaded and run on October 28, 2026 with start 2021-01-01, exclusive end 2026-10-28, and `auto_adjust=True`. The resulting 1,461 observations span January 4, 2021 through October 27, 2026. Retrieval metadata is in `03-meta-time-series/results/data_provenance.json`.

Use `python analysis.py --download` to obtain a new snapshot, or pass a CSV with Date, Close, and Volume using `--input`. A later download may reflect provider restatements; a fixed date range alone does not freeze the vendor's historical values.
