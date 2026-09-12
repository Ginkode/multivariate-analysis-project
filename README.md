# Multivariate Analysis of Student Performance

University project in **R / R Markdown** exploring relationships between student habits and academic performance with multivariate statistical methods.

The analysis focuses on a student-performance dataset containing variables such as study time, social-media use, sleep, attendance, exercise, mental-health rating, and exam score.

## Methods used

- Principal Component Analysis (PCA)
- Correspondence Analysis (CA)
- hierarchical clustering
- correlation analysis
- exploratory visualization

## Main observations

The exploratory analysis shows a strong positive relationship between daily study time and exam score. PCA is then used to study the structure of the quantitative variables and reduce dimensionality.

For categorical variables, Correspondence Analysis is used to study associations between grouped levels of performance and behavioral or wellbeing variables.

The clustering section compares single, complete, and average linkage and uses the resulting groups to describe different student profiles.

## Repository structure

```text
multivariate-analysis-project/
├── README.md
├── student_multivariate_analysis.Rmd
├── student_habits_performance.csv
└── report/
    └── student_multivariate_analysis.html
```

## Source and report

- `student_multivariate_analysis.Rmd` contains the complete analysis and R code.
- `report/student_multivariate_analysis.html` is the rendered report.

The original university report and code comments are mostly **in Italian**. This README is in English so that the project can be reviewed quickly in an international portfolio without rewriting the original academic material.

## Tools

Main R packages used in the analysis include `FactoMineR`, `factoextra`, `ggplot2`, `corrplot`, `scatterplot3d`, and `readr`.

## Methodological notes

The project contains both manual matrix calculations and package-based implementations. This was intentional in the original coursework: the manual steps were used to understand the underlying PCA and Correspondence Analysis calculations, while the package implementations were used for interpretation and visualization.

One point still worth improving is the clustering workflow: distances should be used at full numerical precision during hierarchical clustering, with rounding reserved only for display. A future revision could also use a quantitative criterion such as silhouette width to support the choice of the number of clusters.

## Scope

This is an exploratory/statistical-analysis project rather than a production machine-learning system. Its main purpose in the portfolio is to show multivariate reasoning, dimensionality reduction, clustering, and interpretation of statistical results.
