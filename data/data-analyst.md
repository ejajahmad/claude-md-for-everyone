# CLAUDE.md: Data Analyst

<!-- For: analysts working with SQL, spreadsheets, pandas, and dashboards who need trustworthy numbers. -->

## About me
I answer business questions with data. A wrong number confidently reported is the worst outcome. Correctness and transparency come first.

## How to work
- Restate the business question and how you'll measure it before you query. Define each metric precisely (numerator, denominator, time window, filters).
- Inspect the data first: row counts, nulls, duplicates, date ranges, and unexpected categories. Report anything odd.
- State every assumption (timezone, how refunds and test accounts are treated, deduplication logic).
- Sanity-check the results: do totals reconcile? Are the magnitudes plausible? Compare against a known number if one exists.

## SQL
- Use readable SQL: CTEs over nested subqueries, one CTE per logical step, and meaningful aliases.
- Be explicit about join types, and check for join fan-out (row count before and after the join).
- Watch for `NULL` handling in filters and aggregates, integer division, and `COUNT(*)` versus `COUNT(DISTINCT …)`.
- Add a comment explaining any non-obvious filter.

## Python / pandas
- Keep the analysis reproducible: one script or notebook that runs top to bottom with no hidden state.
- Use vectorized operations, not row loops. Check dtypes after loading.

## Charts
- Choose the chart for the question: trends get lines, comparisons get bars, distributions get histograms.
- Every chart needs a title that states the takeaway, labeled axes with units, and a source or date range.
- Never truncate the y-axis on a bar chart.

## Reporting
- Lead with the answer and the key number, then the supporting detail, then caveats.
- Separate what the data shows from what it might mean. Don't imply causation from correlation.

## Project specifics
<!-- Warehouse/DB, key tables, metric definitions, BI tool. -->
