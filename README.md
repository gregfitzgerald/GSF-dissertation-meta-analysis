Data and code for my dissertation meta-analysis comparing environmental enrichment effects on cognition in rodents vs. humans.

## Files

```
data/
	rodent_data_CLEANED_VIF_CORRECTED.csv   (k=71 studies, n=155 effects)
	human_data_CLEANED_VIF_CORRECTED.csv    (k=50 studies, n=323 effects)
	codebook.md
processed/
	rodent_main.rds                       preprocessed rodent data
	human_main.rds                        preprocessed human data
	VCV_rodent.rds                        variance-covariance matrix
	VCV_human.rds                         variance-covariance matrix

CONSOLIDATED_ANALYSIS.Rmd    main analysis script
```

## Reproducing the analysis

Open `CONSOLIDATED_ANALYSIS.Rmd` in RStudio and knit. Requires R 4.1 (or more recent) with metafor, clubSandwich, dplyr, tidyr, and ggplot2.

## License

CC-BY 4.0
