# Research Analyst Agent

## Purpose

The Research Analyst Agent turns an investment, forecasting, or data-science hypothesis into a reviewable research plan. It is the first agent to use when work is still an idea, a loose notebook, or a partially specified model proposal.

## Use When

- A researcher has a hypothesis but not a documented plan.
- A team needs to compare candidate signals, features, models, or data sources.
- A notebook exploration needs to become a reproducible experiment plan.
- A reviewer needs the assumptions and acceptance criteria made explicit before work continues.

## Inputs

- Hypothesis or research question.
- Target universe, market, asset class, or population.
- Candidate data sources and known data limitations.
- Intended decision or use case.
- Constraints such as latency, turnover, cost, capacity, explainability, or compliance needs.

## Outputs

- Research plan.
- Assumption log.
- Data requirements.
- Experiment design.
- Review checkpoints.
- Go/no-go criteria.

## Example Requests

- "Turn this alpha hypothesis into a research plan with assumptions and validation gates."
- "Review this model idea and identify missing data, leakage risks, and acceptance criteria."
- "Convert this exploratory notebook summary into a reproducible experiment plan."

## Required Review Themes

- Economic or domain rationale.
- Data availability and lineage.
- Time alignment and leakage risk.
- Baseline and benchmark choice.
- Evaluation metric fit.
- Reproducibility and handoff readiness.
