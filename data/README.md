# Data

## Directory Structure

```
raw/         Extracted study data (CSV)
processed/   Analysis-ready R objects (RDS)
codebook.md  Variable definitions
```

## Raw Data Files

| File | Description |
|------|-------------|
| `rodent_data.csv` | Rodent study data (115 columns, 161 effect sizes) |
| `human_data.csv` | Human study data (134 columns, 323 effect sizes) |

Data includes effect sizes (Hedges' g), sampling variances adjusted for multi-arm studies, and all study-level covariates.

## Processed Data Files

| File | Description |
|------|-------------|
| `rodent_main.rds` | Rodent data as R object (k=71 studies, n=155 effect sizes) |
| `human_main.rds` | Human data as R object (k=50 studies, n=323 effect sizes) |
| `VCV_rodent.rds` | Variance-covariance matrix for rodent data (155 x 155) |
| `VCV_human.rds` | Variance-covariance matrix for human data (323 x 323) |

VCV matrices were constructed assuming r = 0.7 for within-study correlations using the `clubSandwich::impute_covariance_matrix()` function.

## Variable Documentation

See `codebook.md` for complete variable definitions for both datasets.
