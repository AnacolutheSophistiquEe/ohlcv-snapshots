# OHLCV Snapshots

Last update: `2026-05-14T08:27:01.735489+00:00`

Daily snapshots of OHLCV data for the trading universe of [Manuel's IBKR Dip Scalper](https://github.com/AnacolutheSophistiquEe).
Used by the `equity-technical-analyst` Claude.ai skill via `web_fetch` — the only reliable network path from the claude.ai sandbox.

## Format

- File naming: `<TICKER>_<timeframe>.csv`
- Header: 4 comment lines starting with `#` (ticker, yfinance symbol, generation timestamp, bar count)
- Body: standard CSV with columns `Date,Open,High,Low,Close,Volume`

## Timeframes

| TF | Period | Interval | Resample |
|---|---|---|---|
| `daily` | 5y | 1d | — |
| `h4` | 3mo | 60m | 4h |
| `h1` | 1mo | 60m | — |

## Tickers

(16 assets covered)

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
