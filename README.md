# OHLCV Snapshots

Last update: `2026-05-22T16:02:05.313981+00:00`

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

(17 assets covered)

| Display | yfinance symbol |
|---|---|
| `RHM` | `RHM.DE` |
| `SRT3` | `SRT3.DE` |
| `EVT` | `EVT.DE` |
| `ENR` | `ENR.DE` |
| `MSTR` | `MSTR` |
| `SMCI` | `SMCI` |
| `PLTR` | `PLTR` |
| `IONQ` | `IONQ` |
| `RGTI` | `RGTI` |
| `CEG` | `CEG` |
| `SMR` | `SMR` |
| `HOOD` | `HOOD` |
| `SOFI` | `SOFI` |
| `SPY` | `SPY` |
| `QQQ` | `QQQ` |
| `IWM` | `IWM` |
| `EWG` | `EWG` |

## Consumption

Skill TA fetches via:
```
https://raw.githubusercontent.com/AnacolutheSophistiquEe/ohlcv-snapshots/main/<TICKER>_<TF>.csv
```

Example: https://raw.githubusercontent.com/AnacolutheSophistiquEe/ohlcv-snapshots/main/MSTR_daily.csv
