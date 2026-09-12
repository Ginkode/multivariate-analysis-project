# Multivariate Analysis of Student Performance

Exploratory multivariate analysis of student habits and academic performance using **R** and **R Markdown**.

The project studies how variables such as study time, attendance, sleep, social-media use, exercise and mental-health rating relate to exam performance.

## Main analyses

- Principal Component Analysis (PCA)
- Correspondence Analysis (CA)
- Hierarchical clustering
- Correlation analysis
- Multivariate visualization

## PCA

The quantitative variables are standardized before PCA. The analysis uses eigenvalues, explained variance and graphical representations to interpret the main dimensions.

One of the clearest patterns in the exploratory analysis is the positive relationship between study time and exam score, while entertainment-related variables tend to point in the opposite direction in the PCA biplot.

## Clustering

The report compares single, complete and average linkage. Single linkage shows a clear chaining effect, while complete linkage gives more compact and interpretable groups and is used for the final four-cluster visualization.

A technical point identified while reviewing the project for the portfolio: the original coursework rounds the distance matrix before calling `hclust()`. That is not necessary and can alter distances slightly. The original R Markdown is kept unchanged as the submitted coursework artifact; `TECHNICAL_NOTES.md` documents the correction that should be used in a rerun.

## Correspondence Analysis

Categorical versions of selected variables are analyzed through contingency tables and Correspondence Analysis. The report combines manual matrix calculations with `FactoMineR` output to interpret associations between categorical student profiles.

## Files

```text
multivariate-analysis-project/
├── README.md
├── TECHNICAL_NOTES.md
├── student_multivariate_analysis.Rmd
├── student_habits_performance.csv
└── report/
    └── student_multivariate_analysis.html
```

The R Markdown and rendered report contain the full university analysis, including formulas, plots, code and written interpretation. They are mostly in Italian because that was the language of the original coursework; this README is in English for the portfolio.

## Main R packages

- `FactoMineR`
- `factoextra`
- `ggplot2`
- `corrplot`
- `scatterplot3d`
- `readr`

This is an exploratory statistical project rather than a production modelling pipeline.
