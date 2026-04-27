# Quizr

A minimal, browser-based flashcard app. Upload a spreadsheet of terms, then draw them one at a time in random order without replacement.

## Usage

Open `index.html` directly in a browser — no server or installation required.

### Spreadsheet format

Quizr reads the first sheet of any `.xlsx` file. The sheet should have a header row with at least a **Term** column. An optional **Answer** column will be displayed below each term in smaller text when present.

| Index | Term | Answer |
|-------|------|--------|
| 1 | genetic drift | Change in allele frequency due to random sampling |
| 2 | Hardy-Weinberg equilibrium | ... |

- The **Index** column is ignored.
- Column names are matched case-insensitively.
- If no **Term** header is found, the first column is used.
- Rows with a blank term are skipped. Missing or blank **Answer** values are silently ignored.

### Controls

| Button | Action |
|--------|--------|
| **Draw term** | Reveal the next randomly selected term |
| **Shuffle & restart** | Re-shuffle the full list and start over |
| **Load new file** | Return to the upload screen to load a different file |

A progress bar tracks how many terms have been shown out of the total. When all terms have been drawn, the app indicates completion.

## Dependencies

[SheetJS](https://sheetjs.com/) is loaded from the SheetJS CDN and is the only external dependency.
