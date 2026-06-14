# NDXalgo — Automated NDX Signal System

An algorithmic system that generates daily Nasdaq 100 (NDX) direction signals,
executed automatically before the US market close.

**→ [Performance Dashboard](https://pupa1419-blip.github.io/Trading-signals/)**

---

## How It Works

**Model A — Daily Direction**
Generates an UP or NEUTRAL signal at 3 PM ET each trading day, based on a 9-indicator
vote system measuring bearish market conditions.
Executed via TQQQ (3× leveraged NDX ETF).

**Model B — Weekly Bear Risk**
Weekly bear risk detection. When triggered, all Model A trades are suspended for up to
12 weeks. Resolved early if NDX drops ≥ 10% from the call level.

---

## Live Record Files

| File | Description |
|------|-------------|
| [signal_log.jsonl](signal_log.jsonl) | Daily 3 PM signals — immutable GitHub timestamps |
| [trade_log.jsonl](trade_log.jsonl) | Daily 4 PM trade decisions with KIS fill prices |
| [performance.json](performance.json) | All-time accuracy statistics |
| [weekly_summary.json](weekly_summary.json) | Latest weekly snapshot (regime + signals) |
| [episode_summary.json](episode_summary.json) | Model B bear call track record |

> Signals are committed to this repository at the time of generation.
> GitHub commit timestamps serve as tamper-evident proof that signals precede market outcomes.

---

*Last updated: 2026-06-13 — Past performance does not guarantee future results. Not financial advice.*
