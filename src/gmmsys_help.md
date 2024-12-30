# GMMSYS - System GMM Estimation Package for Gretl

## Overview
GMMSYS implements system GMM estimation for simultaneous equation models in Gretl. It provides a flexible interface for estimating multiple equations with different regressors while sharing common instruments.

## Main Function
```
bundle gmmsys(list Endog, lists Regressors, list Instruments, bundle Options[null])
```

### Arguments
- `Endog`: List of endogenous variables (one per equation)
- `Regressors`: Array of lists containing equation-specific regressors
- `Instruments`: List of instruments shared across equations
- `Options`: Optional bundle for customization
  - `initcoeff`: Initial coefficient values (default: OLS estimates)

### Returns
Bundle containing estimation results including:
- Estimation output (produced by gretl's built-in `gmm` command) (`Model`)
- List of fitted values (`yhats`)
- List of residuals (`uhats`)
- Matrix of R-squared values (`rsq`)
- Matrix of residual correlation matrix (`corr_uhat`)
- Matrix residual standard errors (`std_uhat`)


## Changelog
- **v0.1** (2025-01-01)
  - Initial release
