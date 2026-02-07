---
name: sanity-check
description: Review data pipeline or analysis code for integrity issues. Use when writing or reviewing data processing code, merges, or analysis pipelines — especially before finalizing results.
---

Review the current state of the data pipeline or analysis code I'm working on. Check for:

1. **Data integrity**: Are there merges that might silently drop rows? Filters that could lose data unexpectedly?
2. **Identifier matching**: If joining financial datasets, are CIK/CUSIP/PERMNO/GVKEY identifiers handled correctly (leading zeros, type mismatches, etc.)?
3. **Reproducibility**: Can this code run end-to-end without manual steps? Are file paths relative?
4. **Output validation**: Are there sanity checks on output (row counts, value ranges, null rates)?
5. **Common pitfalls**: Date parsing issues, timezone problems, encoding errors in SEC filings, etc.

Summarize findings as a checklist of items to fix, ordered by severity.
