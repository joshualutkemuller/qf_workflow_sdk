# Prompt: Experiment Summary

## Purpose

Summarize a completed experiment so it can be reviewed, reproduced, and used in future decisions.

## Required Inputs

- Experiment goal.
- Code path and commit or version.
- Data sources and windows.
- Configuration and parameters.
- Metrics and results.
- Observations, decisions, and follow-up work.

## Prompt

Use `instructions/quant_research.md` and `instructions/documentation.md`.

Create an experiment summary from this context:

```text
{experiment_context}
```

Return a Markdown summary with:

- Goal.
- Hypothesis or question.
- Code, data, and configuration references.
- Experiment design.
- Results.
- Baseline and benchmark comparison.
- Error or failure analysis.
- Risks and limitations.
- Decision.
- Reproducibility steps.
- Follow-up actions.

## Checks

- Include enough detail for another person to rerun the experiment.
- State negative, inconclusive, or failed results plainly.
- Do not collapse results and interpretation into one section.
