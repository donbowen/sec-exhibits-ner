---
name: clean-html
description: Strip HTML from files and return clean plain text. Use when processing SEC filings or other HTML documents.
---

Strip HTML from the specified file(s) or text and return clean plain text.

$ARGUMENTS

Guidelines:
- Use BeautifulSoup (`bs4`) with the `lxml` or `html.parser` backend.
- Remove all HTML tags, scripts, styles, and comments.
- Decode HTML entities (`&amp;` -> `&`, `&nbsp;` -> space, etc.).
- Collapse excessive whitespace and blank lines (no more than one consecutive blank line).
- Preserve paragraph breaks (convert `<p>`, `<br>`, `<div>` closings to newlines before stripping tags).
- If processing SEC filings specifically, also handle:
  - SGML/XBRL wrapper tags
  - `<SEC-HEADER>` blocks (optionally extract metadata from these)
  - Page break markers and header/footer repetitions
- If the input is a file path, read and process it. If it's a directory or glob pattern, process all matching files and save cleaned versions to an output directory.
- Output: print the cleaned text or save to file (e.g., same filename with `.txt` extension in `outputs/`).
