# Project Instructions for Claude

## Who I Am

I'm a finance professor. My work involves empirical research using SEC filings, financial datasets, and econometric analysis. I use **Python** and **Stata** as my primary tools.

## Languages and Tools

- **Python**: Data processing, NLP/NER, web scraping, API calls, machine learning. I use Jupyter notebooks heavily for exploratory work, and `.py` files for reusable code.
- **Stata**: Econometric analysis, panel data regressions, summary statistics, and publication-quality tables. Stata `.do` files should follow standard conventions.
- **Data formats**: CSV, Parquet, Excel, JSON, and Stata `.dta` files are all common.

## Python Conventions

- Use `pandas` for dataframes, not base Python data structures for tabular data
- Prefer `pathlib.Path` over `os.path` for file paths
- Use f-strings for string formatting
- Type hints are welcome but not required -- keep code readable for academic collaborators who may not be Python experts
- Virtual environments: use `conda` (environment.yml) or `pip` (requirements.txt)
- For notebooks: keep cells focused, add markdown cells explaining the "why" before code cells
- When writing functions, include a short docstring explaining what it does and what it returns

## Stata Conventions

- Use `local` and `global` macros appropriately
- Always `compress` data before saving
- Use `estout` / `esttab` for regression tables
- Comment `.do` files with `//` for inline and `/* */` for blocks
- Preserve sort order: use `sort` or `gsort` explicitly before operations that depend on order
- Use relative paths from the project root, not absolute paths

## Research Workflow Preferences

- I prefer reproducible workflows: scripts should run end-to-end without manual intervention
- Data cleaning and analysis should be separate steps/files
- Always preserve raw data -- never overwrite input files
- Output files should go in `outputs/` with clear naming (include date or version if relevant)
- When in doubt, ask me before making architectural decisions about the project structure

## Code Quality

- Prioritize **clarity over cleverness** -- this code will be read by research assistants and co-authors
- Keep functions short and single-purpose
- Use descriptive variable names (not `x`, `df2`, `temp`)
- When processing SEC filings or financial data, add sanity checks (row counts, null checks, value ranges)
- Print/log progress for long-running operations

## Git Practices

- Write clear commit messages describing what changed and why
- Don't commit large data files (add to `.gitignore`)
- Don't commit API keys or credentials

## Common Tasks I'll Ask For Help With

- Parsing and processing SEC EDGAR filings (HTML, XML, XBRL)
- Named Entity Recognition on legal/financial text
- Building datasets by merging firm identifiers (CIK, CUSIP, PERMNO, GVKEY)
- Running and interpreting regressions in Stata
- Creating publication-ready tables and figures
- Web scraping with appropriate rate limiting and politeness
- Cleaning messy real-world financial data

## What Not To Do

- Don't over-engineer: a clean script is better than a complex framework for a one-off analysis
- Don't add unnecessary dependencies -- prefer standard library or well-known packages (pandas, numpy, scipy, statsmodels, spacy, requests, beautifulsoup4)
- Don't silently drop data -- always flag when rows are lost in merges or filters
- Don't use LLM-style comments like "# This is a great approach!" in code

## Feedback and Improvement

Claude should periodically (roughly every 5-10 substantive interactions) offer brief observations about how we're working together. Examples:
- "I notice we keep running into X -- should we add a rule to CLAUDE.md about that?"
- "You tend to prefer Y approach -- want me to default to that going forward?"
- "I had to ask about Z several times -- should we document that decision?"

The goal is to continuously improve this file and our workflow. When suggesting updates, propose the specific edit to CLAUDE.md so I can approve it quickly.
