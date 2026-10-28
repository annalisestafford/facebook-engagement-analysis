# Facebook Engagement Analysis

**R | tidyverse | ggplot2 | Linear Regression | Logistic Regression | Model Evaluation**

An exploratory analysis of **500 Facebook posts from a cosmetics brand** to investigate how posting time, content type, and paid promotion relate to engagement.

## Questions

1. Do hour, weekday, and month help predict total post interactions?
2. How does the association between paid promotion and engagement differ by post type?
3. How are post reach and interactions related?

## Methods

- Clean and transform post-level Facebook metrics.
- Explore engagement distributions and posting-time heatmaps.
- Compare eight linear regression models using an 80/20 train/test split and **MAE, MSE, and RMSE**.
- Fit logistic regression for the probability of reaching the training-set top quartile of engagement; evaluate with a test-set Brier score.
- Compare paid and organic posts by type and estimate a promotion × post-type interaction model.
- Explore a quadratic association between lifetime reach and interactions.

## Findings and interpretation

The analysis illustrates substantial variation in interactions across posts and content types. Posting-time and promotion patterns are explored using both descriptive charts and regression models. **Run the report to view the numerical model comparisons and fitted results**; no numerical findings are claimed here without executing the R analysis.

**Important limitations:** These are observational data from one brand, so associations should not be interpreted as causal effects. The dataset does not contain advertising spend; therefore, it cannot identify advertising ROI or diminishing returns to spending. The sample is relatively small for detailed time-by-type comparisons.

## Repository structure

```text
facebook-engagement-analysis/
├── README.md
├── analysis/
│   └── facebook_engagement.Rmd
├── data/
│   └── facebook_posts.csv
├── figures/
│   └── .gitkeep
└── .gitignore
```

## How to run

1. Install [R](https://www.r-project.org/) and [RStudio](https://posit.co/download/rstudio-desktop/) (optional).
2. Install packages:
   ```r
   install.packages(c("tidyverse", "broom", "rmarkdown", "knitr"))
   ```
3. Open R from the **repository root**, then run:
   ```r
   rmarkdown::render("analysis/facebook_engagement.Rmd", output_dir = "figures")
   ```
4. Open `figures/facebook_engagement.html` to see the tables, charts, and analysis.

## Data attribution

Source: [UCI Machine Learning Repository — Facebook Metrics](https://archive.ics.uci.edu/dataset/368/facebook+metrics). Originally associated with Moro, Rita, and Vala (2016). Dataset redistributed here for reproducibility; consult the source for metadata and usage terms.

