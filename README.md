# OHLCV Snapshots

Last update: `2026-07-13T21:30:28.593008+00:00`

Daily snapshots of OHLCV data for the trading universe of [Manuel's IBKR Dip Scalper](https://github.com/AnacolutheSophistiquEe).
Used by the `equity-technical-analyst` Claude.ai skill via `web_fetch` — the only reliable network path from the claude.ai sandbox.

## Format

- File naming: `<TICKER>_<timeframe>.csv`
- Header: 4 comment lines starting with `#` (ticker, yfinance symbol, generation timestamp, bar count)
- Body: standard CSV with columns `Date,Open,High,Low,Close,Volume`

## Timeframes

| TF | Period | Interval | Resample | Usage |
|---|---|---|---|---|
| `daily` | 1y | 1d | — | Skill TA — Phases 2-8 (default, ~16 KB) |
| `daily_long` | 5y | 1d | — | Skill TA — Phase 9bis base rate uniquement (~80 KB) |
| `h4` | 3mo | 60m | 4h | Skill TA — multi-TF alignment |
| `h1` | 1mo | 60m | — | Skill TA — intraday confirmation |

> **Note (2026-05-14)** : split `daily` (1y, default) / `daily_long` (5y, base rate) introduit pour réduire la consommation tokens du skill `equity-technical-analyst`. Cf. `deploy/SETUP_OHLCV_SNAPSHOTS.md`.

## Tickers

(7 assets covered)

| Display | yfinance symbol |
|---|---|
| `000660` | `000660.KS` |
| `005930` | `005930.KS` |
| `267260` | `267260.KS` |
| `298040` | `298040.KS` |
| `012450` | `012450.KS` |
| `207940` | `207940.KS` |
| `326030` | `326030.KS` |

## Consumption

Skill TA fetches via:
```
https://raw.githubusercontent.com/AnacolutheSophistiquEe/ohlcv-snapshots/main/<TICKER>_<TF>.csv
```

Example: https://raw.githubusercontent.com/AnacolutheSophistiquEe/ohlcv-snapshots/main/MSTR_daily.csv
