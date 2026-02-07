Translate the following Stata code to Python.

$ARGUMENTS

Guidelines:
- Use pandas for data manipulation by default. Use Polars if the user specifies or if the dataset has >1M rows.
- Key Stata-to-Python mappings:
  - `use` / `save` → `pd.read_stata()` / `df.to_stata()`
  - `gen` / `replace` → direct column assignment
  - `collapse` / `gcollapse` → `groupby().agg()`
  - `merge` → `pd.merge()`
  - `keep` / `drop` → column/row selection or `.drop()`
  - `sort` / `gsort` → `.sort_values()`
  - `bysort` → `.groupby()`
  - `distinct` / `duplicates drop` → `.drop_duplicates()`
  - `tab` → `.value_counts()`
  - `sum` / `summarize` → `.describe()` or specific aggregations
  - `reghdfe` → `pyfixest` (preferred) or `linearmodels`
  - `foreach` / `forvalues` → Python loops or list comprehensions
  - `local` / `global` macros → Python variables
  - `preserve` / `restore` → `df.copy()`
  - `encode` → `.astype('category')` or `pd.Categorical`
  - `destring` → `pd.to_numeric()`
  - `tostring` → `.astype(str)`
- Preserve the logic and intent, not just literal syntax.
- Add comments noting any Stata behaviors that differ in Python (e.g., Stata sorts are stable, missing values sort last).
