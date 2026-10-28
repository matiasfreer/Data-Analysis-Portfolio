# Validation and portfolio revisions

Verified on October 28, 2026. `requirements.txt` records the versions used for the portfolio reruns. Code and visual cleanup performed for publication are separate from the original academic submission. The original notebooks and group PDFs retain historical results.

## Job-posting analysis

Reran from the supplied 672-row raw CSV. Confirmed zero duplicate rows and no hourly salary records. Reproduced Colorado's $103,650 average salary estimate, 10 postings, and 6 distinct employers.

The portfolio edition detects salary units before removing labels, uses the final comma-separated state token for irregular locations, and keeps original job titles rather than broadly collapsing them. It validates salary bounds and state formatting. These are publication revisions; hourly handling did not change this dataset because no hourly records were present.

Colorado is a defensible team selection, not a unique mathematical optimum: Tennessee also has lower salary estimates and fewer represented employers while meeting the screening threshold. No unsupported composite optimum is claimed.

## App-market analysis

Reran from the intact uncompressed cleaned course input. The supplied gzip copy failed its internal CRC check and was not used.

Confirmed 2,312,832 rows, 2,862 Comics apps, and 2,738 Comics apps with positive recorded permission counts. Reproduced privacy-tier sample sizes (1,104 / 936 / 698), successes (117 / 93 / 80), reported mean ratings to rounding, monetization rates, and 50K versus 5K median minimum installs. Reproduced the Kruskal-Wallis p-value 0.0000790736 and pairwise test conclusions.

Reran a 300-tree balanced Random Forest with an 80/20 stratified split, seed 42, and held-out ROC-AUC permutation importance over 20 repeats. All imputation is now fitted within the training pipeline. Portfolio ROC-AUC is 0.7947 versus 0.791 reported in the original notebook. Preprocessing and library versions differ; the difference is not attributed solely to one change. Permutation importance still ranks days since update and app age highest.

Figures now derive labels and values from computed results, preserve negative permutation values, and display permutation standard deviations. Those bars are descriptive variation over repeats, not confidence intervals.

The positive-permission filter is explicit. Zero counts cannot distinguish missing joins from genuine zero-permission apps in the cleaned input. The deck's broader matched-record counts are not adopted as verified. This limitation is documented rather than silently changing the original study population. All-Comics monetization results are supplied separately.

## META analysis

Reran the fixed-date portfolio script using a fresh adjusted-price download: 1,461 observations, raw-price ADF p=0.77124, first-difference p below numerical display precision, 17 outlier days, and three Golden/three Death Crosses.

The original notebook reports raw-price ADF p=0.87018 and the deck displays 0.8707. Both imply failure to reject the unit-root null at 5%. The new run is a separate, explicitly dated analysis, not an exact reproduction of the original unspecified snapshot. Original charts and notebook outputs are retained and labeled accordingly.

The portfolio script removes the repeated download overwrite, uses explicit adjusted-price settings, saves local snapshot/provenance on download, and defines crossovers using consecutive signs with valid rolling windows. Raw downloaded series is excluded from the public package.

SARIMAX, AR(30), forecast-error figures, and business-event/financial statements appear only in the original team presentation. The relevant team implementation was not supplied and these results are not claimed as independently verified or as Matias's individual work.

## Scope and checks

All three analysis scripts ran successfully on the supplied/fetched inputs. Result CSV/JSON files were saved. The figures were visually inspected. The package contains no full Drive archive, raw app dataset, credentials, or environment files. Relative Markdown links and notebook JSON structure are checked before delivery. Original presentations are included unchanged and may contain historical drafting artifacts; the verified portfolio findings are in the project READMEs.
