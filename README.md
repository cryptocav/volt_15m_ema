# VOLT | EMA Crossover Strategy (BTCUSDT 15m)

This repository contains selected outputs from my custom-built strategy engine, VOLT — a system designed to discover real, executable crypto strategies that beat *buy and hold* using logic inspired by institutional trading flows.

## 📌 What This Repo Contains

- `volt_ema_crossover_indicator.pine`:  
  A TradingView-compatible Pine Script that visualizes the EMA crossover entry logic with optional filters (RSI, MACD, trend alignment), dynamic SL/TP, and trailing logic.

- `BTCUSDT_15m_ema_crossover_top_*.json`:  
  A series of JSON files ranking the top-performing parameter configurations from a full parameter sweep, evaluated across:
  - `pnl`: total net profit
  - `sharpe`: risk-adjusted return
  - `alpha_vs_hodl`: outperformance vs passive holding
  - `win_rate`: % of winning trades
  - `aggregate_score`: a combined metric for overall performance

These are real backtest outputs for BTCUSDT on the 15-minute timeframe, using a strategy that supports:
- EMA fast/slow cross detection
- ATR-based SL/TP
- Optional trailing stops and partial take-profits
- Macro trend alignment via higher-timeframe EMA
- RSI and MACD-based trade filters

## ⚙️ My Philosophy

Most retail strategies are too noisy, curve-fitted, or naive. VOLT is built on a simple principle:

> **Find configurations that actually beat buy-and-hold, and survive real-world constraints.**

I’m sharing these outputs publicly to contribute to more grounded, data-driven trading system exploration — and to track what actually works.

This repo is part of my personal learning and exploration. The full engine (strategy logic, parameter sweeper, and backtester) is still under development and not yet open-sourced.

## 📈 Example Result

One of the top configs in this sweep delivered:

- **PnL**: +27.45  
- **Sharpe**: 0.14  
- **Alpha vs HODL**: +1680.29  
- **HODL PnL (same period)**: -1652.85  
- **Win Rate**: 37.21%  
- **Drawdown**: 9.9%  
- **Trades**: 86  
- **Strategy**: Long+Short EMA crossover with:
  - Trend alignment filter
  - MACD confirmation
  - RSI window filter
  - 2x/3x partial take-profits
  - 20% trailing stop

---

## 🔒 About the Engine

The engine powering this output is built in Python and uses Binance OHLCV data, clean parameter sweep logic, realistic trade modeling (slippage, commission, risk sizing), and supports real-time signal detection + Telegram alerts.

The full architecture is still evolving and will be shared once hardened. I’m optimizing for:

- Transparency
- Robustness
- Signal quality over quantity
- Alignment with actual price action, not indicator noise

---

## 🧠 Connect

I'm sharing this as part of a longer-term vision to build open, grounded trading tools.

> All signal. No hype.

Feel free to fork, follow, or reach out if this kind of thing interests you.
