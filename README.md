# BTC credit-regime dashboard data

Generated files, refreshed each weekday by a scheduled run. Nothing here is
edited by hand. The dashboard is a Google Sheet that reads these three files
with `IMPORTDATA` off their raw URLs.

| file | what it is |
|---|---|
| `dashboard_state.csv` | one row per signal: the current reading, band, position, hold and staleness |
| `dashboard_history.csv` | one row per business day since 2015, append-only, with a `vintage` column saying whether the row was written live on the day or backfilled later |
| `dashboard_signals.csv` | one row per signal: sources, transform, condition, hold, expected staleness, provenance |
| `DASHBOARD_LEGEND.md` | how to read every column and band |

Everything is derived from public series (FRED, ECB reference rates, Deribit).
The code that produces it lives in a separate, private repository.
