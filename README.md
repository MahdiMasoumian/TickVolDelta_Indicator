# TickVolDelta (MQL5 Indicator)

## Overview

TickVolDelta is a custom MetaTrader 5 (MQL5) indicator that visualizes the difference between current tick volume and its Simple Moving Average (SMA). The indicator plots a histogram that separates positive and negative deviations, helping traders identify unusual activity in market participation.

This tool is designed for volume-based analysis in algorithmic trading systems and quantitative research workflows.

---

## Concept

The indicator computes:

- A Simple Moving Average (SMA) of tick volume over a configurable period
- The difference (Delta) between current tick volume and this moving average

\[
\text{Delta} = \text{Tick Volume}_t - SMA(\text{Tick Volume}, period)
\]

Positive and negative deviations are plotted separately to improve visual interpretation.

---

## Features

- Tick volume deviation analysis using SMA baseline
- Dual-color histogram:
  - Blue: Positive volume deviation (above SMA)
  - Red: Negative volume deviation (below SMA)
- Configurable smoothing period
- Zero-line reference for easier interpretation
- Lightweight and fast execution inside MetaTrader 5

---

## Input Parameters

| Parameter | Type | Description |
|----------|------|-------------|
| `period` | int | Lookback period for Simple Moving Average of tick volume |

---

## How It Works

1. The indicator calculates the SMA of tick volume over the defined period.
2. It compares current tick volume with the SMA value.
3. The difference (delta) is plotted:
   - Above zero → positive histogram (blue)
   - Below zero → negative histogram (red)

Only one buffer is active at each point to ensure clear visualization.

---

## Installation

1. Open MetaTrader 5
2. Go to `File → Open Data Folder`
3. Navigate to:
4. Copy `TickVolDelta.mq5` into this folder
5. Compile the file in MetaEditor
6. Attach the indicator to a chart

---

## Use Cases

- Detecting abnormal volume spikes
- Confirming price movements with volume behavior
- Filtering trade signals in algorithmic strategies
- Market microstructure analysis (tick-level activity)

---

## Notes

- This indicator uses tick volume, not real traded volume (depends on broker feed).
- Best used in combination with price action or other volatility-based indicators.
- Suitable for intraday and short-term strategies.

---

## License

Recommended: MIT License (see LICENSE file)

---

## Author

Mohammad Mahdi Masoumian  
Quantistan Project
