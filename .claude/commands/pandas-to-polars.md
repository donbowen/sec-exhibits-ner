Convert the following pandas code to Polars.

$ARGUMENTS

Guidelines:
- Use lazy evaluation (`pl.scan_*` / `.lazy()`) where possible, calling `.collect()` only at the end or when the user needs to inspect results.
- Replace `groupby().agg()` with Polars expression syntax (`pl.col().sum()`, etc.).
- Replace `apply()` / `map()` with native Polars expressions wherever possible — `apply` is slow in Polars.
- Use `pl.when().then().otherwise()` instead of `np.where` or pandas `.where()`.
- For merges, use `join()` with explicit `on=`, `how=` parameters. Note: Polars uses `"left"`, `"inner"`, `"outer"` (not `"outer"` → use `"full"`).
- Replace `pd.read_csv()` with `pl.read_csv()` or `pl.scan_csv()`. For Stata .dta files, use `pl.read_pandas(pd.read_stata(...))` since Polars has no native .dta reader.
- Convert `df.loc[]` / `df.iloc[]` to `.filter()` and `.select()`.
- Note: Polars has no index. If the pandas code relies on index operations, restructure to use explicit columns.
- Add `import polars as pl` at the top if not present.
