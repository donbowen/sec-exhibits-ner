---
name: regression-table
description: Create a publication-quality regression table. Use when the user is setting up regressions, formatting results, or preparing tables for a paper.
---

Help me create a publication-quality regression table from the current analysis. Consider:

1. **Format**: Use `esttab`/`estout` in Stata or `stargazer`/manual formatting in Python
2. **Standard elements**: Include coefficient estimates, standard errors (clustered if appropriate), R-squared, N, fixed effects indicators
3. **Presentation**:
   - Stars for significance levels (*, **, *** for 10%, 5%, 1%)
   - Standard errors in parentheses below coefficients
   - Clear variable labels (not raw variable names)
   - Panel labels if multiple panels
4. **Export**: Output as LaTeX (preferred for papers) and/or CSV for quick review

If the regressions haven't been run yet, help me set them up first.

Context: $ARGUMENTS
