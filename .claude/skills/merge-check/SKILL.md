---
name: merge-check
description: Diagnose merge/join quality. Use when writing or reviewing code that merges dataframes — check key uniqueness, match rates, and row count changes.
---

Diagnose the quality of a merge (join) operation on the dataframes or code specified below.

$ARGUMENTS

Generate code that checks:
1. **Pre-merge key diagnostics**:
   - Are the join keys unique in each dataframe? (identifies 1:1, 1:m, m:1, m:m)
   - Any nulls in the join keys?
   - Dtype mismatches on the join keys between the two dataframes?

2. **Post-merge diagnostics** (Stata `_merge` equivalent):
   - Count of matched rows (both), left-only, and right-only
   - Use `indicator=True` in pandas or equivalent
   - Flag if the merge changed row count unexpectedly (suggests duplicates in keys)

3. **Quick summary**:
   - Print a merge type recommendation (1:1, 1:m, m:1)
   - Warn if row count increased (fanout from duplicates)
   - Show sample unmatched rows from each side (head 5)

Use pandas by default. If the user specifies Polars, adapt accordingly (Polars uses `.join()` with `how="anti"` for unmatched diagnostics).
