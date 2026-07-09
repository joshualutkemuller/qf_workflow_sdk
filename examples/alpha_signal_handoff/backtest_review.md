# Example Backtest Review: Revision Breadth Alpha

## Simulation Contract

- Signal formation: after market close using revision events available by decision time.
- Rebalance: monthly.
- Universe: liquid US equities with point-in-time sector membership.
- Portfolio: sector-neutral top-minus-bottom decile spread.
- Costs: placeholder spread and commission model.

## Findings

1. High severity: availability time for revision events is not yet verified.
2. Medium severity: cost model is too simple for names near liquidity cutoff.
3. Medium severity: result must be tested against momentum, size, and earnings announcement proximity.
4. Low severity: report needs clearer reproduction commands.

## Required Tests

- Re-run using ingestion timestamp as conservative availability time.
- Double cost assumptions.
- Delay execution by one trading day.
- Split performance by sector, liquidity, size, and market regime.
- Compare with sector-neutral momentum baseline.

## Production Blockers

- Point-in-time availability unresolved.
- No monitoring plan.
- No paper trading runbook.

## Decision Recommendation

Do not advance to production. Continue research after timestamp validation and cost robustness testing.
