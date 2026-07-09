# Prompt: Backtest Review

## Purpose

Review a backtest or historical strategy simulation for validity, robustness, and production-readiness.

## Required Inputs

- Strategy or model description.
- Universe construction rules.
- Data sources and timestamps.
- Signal, rebalance, and execution timing.
- Portfolio rules and constraints.
- Cost, slippage, borrow, and capacity assumptions.
- Performance and risk metrics.
- Existing report or summary.

## Prompt

Use the Backtest Review Agent and `instructions/backtesting.md`.

Review the following backtest:

```text
{backtest_context}
```

Return a Markdown review with:

- Simulation contract.
- Findings ordered by severity.
- Bias and leakage review.
- Universe and survivorship review.
- Cost, slippage, borrow, and capacity review.
- Benchmark and baseline review.
- Robustness review.
- Risk review.
- Required follow-up tests.
- Production blockers.
- Decision recommendation.

## Checks

- Treat unusually strong performance as a risk signal.
- Reconstruct timestamp boundaries before assessing results.
- Identify tests that would most reduce uncertainty.
