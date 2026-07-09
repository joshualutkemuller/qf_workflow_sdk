# Example: Alpha Signal Handoff Workflow

This example shows how the SDK pieces fit together for a hypothetical equity alpha signal. It is intentionally lightweight and uses placeholders instead of real proprietary data.

## Workflow

1. Use `prompts/research_plan.md` with `agents/research_analyst/` to draft the research plan.
2. Use `prompts/dataset_card.md` with `agents/data_quality/` to document the required data.
3. Use `prompts/backtest_review.md` with `agents/backtest_review/` to review the historical simulation.
4. Use `templates/docs/experiment_summary.md` to capture each experiment.
5. Use `templates/docs/handoff_memo.md` to create the final continuation memo.

## Example Hypothesis

Stocks with improving short-horizon earnings revision breadth outperform sector-neutral peers over the next month after realistic turnover and cost assumptions.

## Example Artifacts

- `research_plan.md`
- `dataset_card.md`
- `backtest_review.md`
- `handoff_memo.md`

These files demonstrate artifact shape, not validated investment evidence.
