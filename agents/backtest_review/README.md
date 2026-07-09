# Backtest Review Agent

## Purpose

The Backtest Review Agent reviews strategy simulations, alpha tests, portfolio construction experiments, and historical model evaluations for validity, bias, robustness, and handoff quality.

## Use When

- A backtest result is ready for review.
- A strategy appears unusually profitable.
- A researcher changes costs, universe, rebalance rules, labels, or execution assumptions.
- A backtest report or production handoff needs review.

## Inputs

- Strategy or model description.
- Universe, rebalance schedule, and holding period.
- Data sources and point-in-time assumptions.
- Signal generation logic.
- Portfolio construction and constraints.
- Cost, slippage, borrow, and market impact assumptions.
- Performance and risk metrics.

## Outputs

- Backtest review.
- Bias and fragility checklist.
- Required robustness tests.
- Production-readiness blockers.
- Backtest report updates.

## Example Requests

- "Review this backtest report for lookahead bias and robustness gaps."
- "Identify the assumptions that could make this strategy fail out of sample."
- "Suggest the next validation tests before this signal moves to paper trading."

## Required Review Themes

- Lookahead and leakage.
- Survivorship and universe construction.
- Costs, slippage, borrow, and capacity.
- Benchmark and baseline choice.
- Robustness across windows, sectors, regimes, and parameter choices.
- Risk, drawdown, turnover, and exposure behavior.
