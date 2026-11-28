# The Maintainability Gap: AI Code Quality in 2026

Source: https://www.gitclear.com/the_ai_code_quality_maintainability_gap  
Author: GitClear (code-analytics company; research report)  
Date: 2026 (figures for 2026 are year-to-date; the page does not show an exact publication date)  
Verified: HTTP 200, full text read on 27 November 2026

## Key points

- Data set: 623 million analysed code changes, 2023–2026, tracking quality signals as AI authorship grows.
- Risk signals up versus 2023: duplicated code blocks +81% (40.3 to 73.0 per million changed lines), within-commit copy/paste +41%, error-masking constructs +47%, two-week code churn +15%.
- Reuse signals down: cross-file function calls −35%, refactoring ("moved" code) −70% versus 2022 levels, and long-term legacy maintenance −74%.
- "Long-term update percent" is the share of changes that remove or update code last touched more than twelve months ago. It fell from 1.7% in 2023 to 0.46% year-to-date in 2026. GitClear's reading: old code is "not gone, just forgotten"; consolidating, documenting and retiring old code is increasingly not happening.
- Headline in their words: not "AI writes bad code", but the default AI workflow delivers happy-path code, a passing test and a closed ticket while "quietly taxing" reuse, consolidation and error-surfacing, which decide how expensive a codebase is to own in year three.
- Five moves they develop: budget for refactoring and legacy maintenance, tripwire on duplicate blocks, review for error-masking, targeted coaching, measure structure and not just volume. The page only lists them; the full report is behind the page.
- Caveat: GitClear sells code-analytics tooling, and its metrics are proxies (e.g. "moved lines" as refactoring). The post only uses the two headline numbers above.
