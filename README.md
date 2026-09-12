# Multivariate Analysis of Student Performance

Exploratory multivariate analysis of student habits and academic performance using **R** and **R Markdown**.

The project combines dimensionality-reduction, association-analysis, clustering, and predictive methods to study how behavioral and lifestyle variables relate to exam performance.

## Main methods

- Principal Component Analysis (PCA)
- Correspondence Analysis (CA)
- Cluster Analysis
- Correlation analysis
- Exploratory visualization
- Neural-network classification included in the full report

## Research focus

The analysis investigates relationships between `exam_score` and variables such as:

- study hours;
- social-media use;
- sleep;
- attendance;
- exercise frequency;
- mental-health rating.

The project also reduces the dimensionality of the quantitative and categorical information to identify broader student profiles.

## Repository structure

```text
multivariate-analysis-project/
├── README.md
├── student_multivariate_analysis.Rmd
├── student_habits_performance.csv
└── report/
    └── student_multivariate_analysis.html
```

## PCA

The quantitative section standardizes the numerical variables and studies their correlation structure before extracting principal components. Component selection is evaluated through eigenvalues, explained variance, and scree-plot interpretation.

One of the clearest relationships identified in the exploratory analysis is the positive association between daily study time and exam score.

## Correspondence Analysis

Categorical versions of selected variables are analyzed through contingency tables and Correspondence Analysis. The report includes manual matrix calculations as well as validation with `FactoMineR`.

This section is useful for interpreting associations between categories such as academic-performance level and mental-health level.

## Clustering

The project applies clustering techniques to identify groups of students with similar multivariate profiles and then interprets those groups in the reduced-dimensionality space.

## Full report

The complete analysis, including code, formulas, commentary, plots, and interpretations, is available in:

- `student_multivariate_analysis.Rmd` — editable R Markdown source;
- `report/student_multivariate_analysis.html` — rendered report.

## Tools

The project uses packages including:

- `FactoMineR`
- `factoextra`
- `ggplot2`
- `corrplot`
- `scatterplot3d`
- `readr`

## Notes

This repository was originally produced as a university multivariate-data-analysis project and is intended to demonstrate statistical reasoning and exploratory analysis rather than production modelling.

## Possible improvements

- simplify repeated manual calculations into reusable functions;
- make cluster-number selection more explicit with quantitative criteria such as silhouette score;
- separate exploratory code from final-report code;
- add a reproducible package/environment specification for R.
