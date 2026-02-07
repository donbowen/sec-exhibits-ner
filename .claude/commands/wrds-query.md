Help me build a WRDS (Wharton Research Data Services) query. I need to:

$ARGUMENTS

When constructing the query:
- Use the `wrds` Python package for database access
- Specify the exact WRDS library and table names (e.g., `comp.funda`, `crsp.msf`, `tfn.s34`)
- Include appropriate filters (date ranges, share codes, exchange codes, etc.)
- Handle identifier linking correctly (CRSP-Compustat link via `crsp.ccmxpf_lnkhist`, etc.)
- Add standard screens (e.g., common shares only: shrcd in (10,11); US exchanges: exchcd in (1,2,3))
- Use efficient SQL -- filter early, select only needed columns
- Show how to download and save the result locally as CSV or Parquet
