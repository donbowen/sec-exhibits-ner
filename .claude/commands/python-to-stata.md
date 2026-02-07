Translate the following Python (pandas/Polars) code to Stata.

$ARGUMENTS

Guidelines:
- Target modern Stata (17+). Use `frames` if multiple datasets are in play.
- Key Python-to-Stata mappings:
  - `pd.read_csv()` → `import delimited`
  - `pd.read_stata()` → `use`
  - `df.to_stata()` → `save`
  - Column assignment → `gen` / `replace`
  - `.groupby().agg()` → `gcollapse` (user has this package)
  - `pd.merge()` → `merge`
  - `.sort_values()` → `sort` / `gsort`
  - `.drop_duplicates()` → `distinct` (user has this package) or `duplicates drop`
  - `.value_counts()` → `tab`
  - `.describe()` → `sum`
  - `pyfixest` / `linearmodels` → `reghdfe` (user has this package)
  - Python loops → `foreach` / `forvalues`
  - f-strings / variables → locals/globals
  - `.astype('category')` → `encode`
  - Boolean indexing → `keep if` / `drop if`
- Note Stata's single-dataset-in-memory model (unless using frames).
- Add comments for any Python patterns that don't translate directly.
