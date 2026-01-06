# Scripts

## Files

| File | Description |
|------|-------------|
| `CONSOLIDATED_ANALYSIS.Rmd` | Complete analysis pipeline (all hypothesis tests) |
| `CONSOLIDATED_ANALYSIS.html` | Rendered output with results |

## Requirements

**R version:** 4.2.2 or later

**Required packages:**
```r
install.packages(c(
  "metafor",      # Meta-analysis models (Viechtbauer, 2010)
  "clubSandwich", # Robust variance estimation
  "dplyr",        # Data manipulation
  "tidyr",        # Data reshaping
  "ggplot2",      # Visualization
  "tibble"        # Data frames
))
```

## Running the Analysis

1. Open RStudio and set working directory to the repository root
2. Open `scripts/CONSOLIDATED_ANALYSIS.Rmd`
3. Click "Knit" or run chunks individually

**Input files** (must be in `data/processed/`):
- `rodent_main.rds` -- Rodent effect sizes (k=71 studies, n=155 effects)
- `human_main.rds` -- Human effect sizes (k=50 studies, n=323 effects)
- `VCV_rodent.rds` -- Variance-covariance matrix (155 x 155)
- `VCV_human.rds` -- Variance-covariance matrix (323 x 323)

**Output:**
- `CONSOLIDATED_ANALYSIS.html` -- Full results with figures

## Reproducibility

Random seed is set to `20241112` for reproducibility. VCV matrices were constructed with r = 0.7 for within-study correlations.
