# Deleveraging Detection Score (DDS)

A TradingView Pine Script indicator that estimates market deleveraging / liquidation stress on a 0-100 score.

## What It Evaluates

- Price shock severity (standardized log returns / crash sigma)
- Volatility expansion (ATR Z-score spike)
- Stress cascade behavior (count of recent stress bars)
- Synchronicity with a liquidity proxy (correlation + both assets selling off)

## How To Read It

- `0-19`: Normal conditions
- `20-39`: Recovery / elevated caution
- `40-69`: High stress
- `70-100`: Forced liquidation conditions

The dashboard also shows the current stress cascade count as `current / threshold` and a suggested action (`ATTACK`, `WATCH`, or `DEFEND / EXIT`).
