# Loan Default Logistic Regression and Threshold Tradeoffs

**Author:** Cameron Batts

## Problem
Explain the tradeoff between default recall, specificity and accuracy in an imbalanced loan dataset.

## Approach
Reconstruct an R Markdown workflow from the available report concepts, using a stratified split, training-only median imputation, equal-row AIC comparisons and prespecified thresholds. Explicitly treat default (1) as the positive class.

## Reported results
The archived main confusion matrix contains TN=6,848, FP=760, FN=753 and TP=199: accuracy 82.32%, default precision 20.75%, default recall 20.90% and specificity 90.01%. Only 8,560 of 9,697 test rows had predictions; 1,137 were missing. The all-nondefault baseline accuracy on those evaluated rows was 88.88%.

## Limitations and corrections
The PDF used class 0 as positive, so its sensitivity is not default recall. Historical missing-value indicators did not impute the missing values; complete-case omissions reduced coverage. Some AIC comparisons used different row counts and cannot establish the best model. The new workflow changes preprocessing and will not reproduce historical scores. No original source notebook was present; this is a documented reconstruction, not a recovered file.

## Verification
Dataset dimensions, missingness and relevant counts were checked directly. R is unavailable in this environment, so revised R code was reviewed but not parsed, executed or rendered. No new fitted-model performance is claimed.

## Data
The included data have no documented upstream source or redistribution license in the original repository. Preserve provenance when it becomes available.

## Run
Install R and Pandoc (or use RStudio), then run from the repository root:
```r
source("install.R")
rmarkdown::render("Analysis/loan_default_logistic.Rmd")
```
Dependencies are unpinned.

## Files
- [R Markdown analysis](Analysis/loan_default_logistic.Rmd)
- [Readable report](Reports/loan_default_logistic.html)
- [Original PDF](Reports/Loan%20Default%20Prediction%20via%20Logistic%20Regression.pdf) — historical export; conclusions may predate the corrections above.
- [Live portfolio report](https://cameron-batts.github.io/loan_default_logistic.html)
