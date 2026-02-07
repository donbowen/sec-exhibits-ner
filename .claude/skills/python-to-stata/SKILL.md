---
name: python-to-stata
description: Translate Python (pandas/Polars) code to Stata.
disable-model-invocation: true
---

Convert the specified Python code to Stata. When translating:

- Translate `pandas` operations to native Stata commands (`gen`, `replace`, `merge`, `reshape`, `collapse`, etc.)
- Use `reghdfe` for fixed effects regressions where appropriate
- Use `gcollapse` instead of `collapse` for grouped aggregations (user has this package)
- Use `distinct` instead of `duplicates drop` where appropriate (user has this package)
- Use `estout`/`esttab` for table output
- Add comments noting where behavior might differ (e.g., merge diagnostics, missing value treatment, index handling)
- Note Stata's single-dataset-in-memory model (unless using frames)
- If the Python code uses features with no direct Stata equivalent, note the gap and suggest workarounds

Translate: $ARGUMENTS
