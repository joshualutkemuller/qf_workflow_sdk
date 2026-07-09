# Production Readiness Checklist Template

## Artifact

`{model_signal_strategy_or_dataset}`

## Required Before Promotion

- [ ] Research memo is complete and reviewed.
- [ ] Dataset card exists for each material dataset.
- [ ] Model card or backtest report exists when applicable.
- [ ] Data lineage and point-in-time assumptions are documented.
- [ ] Reproducibility steps have been run by someone other than the original author or are scheduled before promotion.
- [ ] Leakage, survivorship, overfitting, and benchmark risks have been reviewed.
- [ ] Monitoring plan is documented.
- [ ] Owner and escalation path are documented.

## Data Checks

- [ ] Source permissions are compatible with intended use.
- [ ] Schema and grain are documented.
- [ ] Row counts, missingness, duplicates, and stale records are checked.
- [ ] Joins are validated.
- [ ] Timestamp availability is documented.

## Model Or Strategy Checks

- [ ] Baseline comparison is documented.
- [ ] Validation design matches deployment setting.
- [ ] Robustness tests are documented.
- [ ] Costs and constraints are realistic when trading is involved.
- [ ] Risks and limitations are visible.

## Operational Checks

- [ ] Runtime dependencies are documented.
- [ ] Configuration is versioned.
- [ ] Alerts and dashboards are identified.
- [ ] Rollback or disable path is documented.
- [ ] Expected refresh or retraining cadence is documented.

## Final Decision

- Decision:
- Approver:
- Date:
- Conditions:
