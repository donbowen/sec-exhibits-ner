Generate a quick data profile / EDA summary for the dataframe or file specified below.

$ARGUMENTS

Produce a code cell (or script) that reports:
1. **Shape**: rows and columns
2. **Dtypes**: column names, types, and count of each type
3. **Missing values**: count and percentage per column, sorted descending
4. **Numeric summary**: `.describe()` for numeric columns (include median)
5. **Categorical summary**: value counts for columns with fewer than 20 unique values (show top 10)
6. **Duplicates**: total duplicate rows and duplicate counts on likely key columns
7. **Memory usage**: total and per-column

Use pandas by default. If the user specifies Polars or the data has >1M rows, use Polars instead.

Keep the output concise — this is a quick check, not a full report. Print results directly; do not save to file unless asked.
