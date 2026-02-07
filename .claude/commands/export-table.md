Format and export a regression or summary table for publication.

$ARGUMENTS

Guidelines:
- Accept regression results from `pyfixest`, `statsmodels`, `linearmodels`, or a pandas DataFrame of summary statistics.
- Default output format: LaTeX. Also support HTML and markdown if requested.
- For regression tables:
  - Use `pyfixest.etable()` if results come from pyfixest.
  - Otherwise use `stargazer` (`pip install stargazer`) or manual formatting.
  - Include: coefficients, standard errors (in parentheses), significance stars, N, R-squared, fixed effects indicators (Yes/No row).
  - Label variables with readable names if a mapping is provided.
- For summary statistics tables:
  - Include: N, mean, SD, min, p25, median, p75, max.
  - Format numbers: round to 2-3 decimal places, use commas for thousands.
- Save output to a file (e.g., `outputs/table1.tex`) and also print to console.
- Add a note about any packages needed (`pip install stargazer` if applicable).
