# Loan Default Logistic Regression and Threshold Tradeoffs

**Author:** Cameron Batts

## Validation update - October 22, 2026

The reconstructed workflow executed and rendered with 19,395 training and 9,696 test rows. All AIC comparisons used the same training rows, and every test row received a prediction.

| Fixed threshold | Accuracy | Default precision | Default recall | Specificity |
| --- | ---: | ---: | ---: | ---: |
| 0.1 | 0.5105 | 0.1523 | 0.7479 | 0.4809 |
| 0.2 | 0.8563 | 0.2287 | 0.1247 | 0.9476 |
| 0.5 | 0.8890 | 0.0000 | 0.0000 | 0.9999 |

At 0.5, default recall was zero despite high accuracy. The all-nondefault baseline accuracy was 0.8891; Brier score was 0.0955. Thresholds were prespecified, not tuned on test labels. New preprocessing differs from the archived report, so the new metrics are a separate validation analysis.

[Aggregate validation record](Reports/validation_results.json). [Executed R workflow](Reports/executed_workflow.html) · [Recorded R environment](Reports/validated_session.txt).

Run `Rscript validation/rerun_analysis.R` from the project root.

## Problem
Explain the tradeoff between default recall, specificity and accuracy in an imbalanced loan dataset.

## Approach
Reconstruct an R Markdown workflow from the available report concepts, using a stratified split, training-only median imputation, equal-row AIC comparisons and prespecified thresholds. Explicitly treat default (1) as the positive class.

## Reported results
The archived main confusion matrix contains TN=6,848, FP=760, FN=753 and TP=199: accuracy 82.32%, default precision 20.75%, default recall 20.90% and specificity 90.01%. Only 8,560 of 9,697 test rows had predictions; 1,137 were missing. The all-nondefault baseline accuracy on those evaluated rows was 88.88%.

## Limitations and corrections
The PDF used class 0 as positive, so its sensitivity is not default recall. Historical missing-value indicators did not impute the missing values; complete-case omissions reduced coverage. Some AIC comparisons used different row counts and cannot establish the best model. The new workflow changes preprocessing and will not reproduce historical scores. No original source notebook was present; this is a documented reconstruction, not a recovered file.

## Verification
Dataset dimensions, missingness and relevant counts were checked directly. The revised R workflow was executed and rendered during this pass. Fresh revised-workflow metrics are reported separately from the archive; no operational benefit is claimed.

## Data
The included data have no documented upstream source or redistribution license in the original repository. Preserve provenance when it becomes available.

## Run
Install R and Pandoc (or use RStudio), then run from the repository root:
```r
source("install.R")
rmarkdown::render("Analysis/loan_default_logistic.Rmd")
```
Tested numerical/NLP packages are recorded in requirements-validation.txt.

## Files
- [R Markdown analysis](Analysis/loan_default_logistic.Rmd)
- [Readable report](Reports/loan_default_logistic.html)
- [Original PDF](Reports/Loan%20Default%20Prediction%20via%20Logistic%20Regression.pdf) — historical export; conclusions may predate the corrections above.
- [Live portfolio report](https://cameron-batts.github.io/loan_default_logistic.html)
