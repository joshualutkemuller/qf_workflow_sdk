# Prompt: Model Card

## Purpose

Draft or update a model card for a forecasting, ranking, classification, risk, or portfolio model.

## Required Inputs

- Model name and owner.
- Intended use and decision.
- Training data and feature summary.
- Label or target definition.
- Model class and configuration.
- Validation design and metrics.
- Known limitations.
- Monitoring and retraining expectations.

## Prompt

Use `instructions/model_validation.md` and `instructions/documentation.md`.

Draft a model card from this context:

```text
{model_context}
```

Return a Markdown model card with:

- Model overview.
- Intended use and non-use.
- Inputs, outputs, and decision timing.
- Training, validation, and test data.
- Feature and label definitions.
- Methodology and configuration.
- Baselines and benchmarks.
- Validation results.
- Error analysis.
- Robustness and sensitivity checks.
- Limitations and risks.
- Monitoring plan.
- Ownership and handoff notes.
- Open questions.

## Checks

- Make time-aware validation explicit when data is temporal.
- Surface leakage risks from preprocessing, feature selection, or labels.
- Compare against a simple baseline when possible.
- Separate observed results from recommendations.
