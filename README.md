# uninsured-physical-activity
SAS analysis of uninsured rates and physical inactivity across U.S. regions, using regression diagnostics, ANOVA/ANCOVA, and stepwise selection.

# Uninsured Rates and Physical Inactivity: A Comparative Regional Study 

# Overview

This project analyzes county-level health measures across all 50 U.S. states to evaluate how uninsured rates relate to physical inactivity, including regional comparisons and multivariable modeling.

# Data

County-level health measures dataset (academic course dataset), averaged to the state level, covering physical inactivity rate, uninsured rate, obesity rate, preventable hospitalization rate, sexually transmitted disease rate, and mammogram screening rate

# Methods

Simple linear regression: physical inactivity ~ uninsured rate

Diagnostics and model refinement (residual analysis, normality tests, Cook's D for influential points, log and square-root transformations)

Regional comparisons using ANOVA and Tukey's HSD post-hoc tests

ANCOVA testing a region-by-uninsured interaction

Multivariable/stepwise modeling (PROC GLMSELECT) to identify additional significant predictors

# Key Results

The uninsured–inactivity association was weak in the simple model (R² = 0.067, p = 0.070).

Physical inactivity and uninsured rates both differed significantly by region (p < 0.0001), with the South showing the highest average of both.

The uninsured–inactivity relationship significantly differed by region (interaction p = 0.044) before adjusting for other covariates.

Stronger predictors emerged in the multivariable model - obesity rate and preventable hospitalization rate explained the majority of variability (R² = 0.87) and, once included, the regional interaction was no longer significant.

# Discussion

While uninsured rate alone was a weak predictor of physical inactivity, clinical factors like obesity and preventable hospitalizations proved far more informative, and appeared to explain much of the regional variation initially observed. This suggests regional differences in inactivity are driven more by underlying health conditions than insurance coverage directly. Limitations include the state-level (rather than individual-level) unit of analysis, which limits causal interpretation and may mask within-state variation.

# Files

uninsured_physical_inactivity.sas - Full analysis script, including the embedded dataset

# Tools

SAS 9.4 (PROC REG, PROC GLM, PROC GLMSELECT, PROC UNIVARIATE, PROC SGPLOT)
