# Example Research Plan: Revision Breadth Alpha

## Research Question

Does improving short-horizon earnings revision breadth predict sector-neutral one-month equity returns after costs?

## Hypothesis And Rationale

Analyst revisions can proxy for changing expectations. If revisions diffuse gradually, a breadth signal may capture information not fully reflected in prices at the decision time.

## Universe

- Liquid US equities.
- Sector-neutral evaluation.
- Exclude names without point-in-time analyst revision coverage.

## Required Data

- Point-in-time analyst estimate revisions.
- Daily security master with historical identifiers.
- Point-in-time sector classifications.
- Daily prices, corporate actions, and volume.
- Trading cost model.

## Experiment Design

- Form signal after close using only revisions available by that decision time.
- Rank stocks within sector.
- Rebalance monthly.
- Compare top-minus-bottom and long-only constrained variants.
- Include simple baselines: sector-neutral momentum and equal-weight sector benchmark.

## Validation Metrics

- Information coefficient.
- Long-short return and Sharpe.
- Drawdown.
- Turnover.
- Cost-adjusted return.
- Sector, size, liquidity, and beta exposure.

## Key Risks

- Revision publication time may be later than source timestamp.
- Current ticker or sector mappings can introduce survivorship bias.
- Signal may be proxying for momentum or size.
- Turnover may erase gross edge.

## Stop Conditions

- Results disappear after realistic costs.
- Performance is concentrated in one period, sector, or liquidity bucket.
- Point-in-time revision availability cannot be verified.

## Next Actions

- Draft dataset card for revisions source.
- Run data quality checks on timestamps and entity mapping.
- Build first no-cost baseline backtest, then add cost stress.
