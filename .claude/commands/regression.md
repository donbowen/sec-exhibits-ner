Set up a regression in Python that mirrors Stata's `reghdfe` style.

$ARGUMENTS

Guidelines:
- Use `pyfixest` as the primary package (closest to reghdfe syntax). Fall back to `linearmodels` if the user prefers or pyfixest can't handle the spec.
- Parse the user's specification. Accept Stata-style syntax like `reghdfe y x1 x2, absorb(fe1 fe2) cluster(cl1)` or a plain English description.
- Include fixed effects via `absorb()` / the formula's `| fe1 + fe2` syntax in pyfixest.
- Include clustered standard errors when specified.
- Show how to print a summary table and extract coefficients.
- If multiple specifications are requested, use `pyfixest.etable()` to display them side by side.
- Add a note about installing the package (`pip install pyfixest`) if it's not in the environment.
- Mention key differences from Stata's reghdfe:
  - Singleton observations: pyfixest drops them by default (same as reghdfe)
  - Multiway clustering syntax
  - How to add interaction terms
