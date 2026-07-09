# Prompt: Quant PR Review Checklist

## Purpose

Generate a review checklist for a pull request that changes quant research, data, model, backtest, or workflow artifacts.

## Required Inputs

- PR summary.
- Changed files.
- Relevant docs or templates.
- Validation commands and outputs.
- Known risks or tradeoffs.

## Prompt

Use `instructions/git_workflow.md`, plus the relevant domain instructions for the changed files.

Create a PR review checklist from this context:

```text
{pr_context}
```

Return a Markdown checklist with:

- Scope confirmation.
- Data and lineage checks.
- Model or research checks.
- Backtest checks if applicable.
- Documentation checks.
- Reproducibility checks.
- Operational risk checks.
- Required reviewer questions.
- Suggested approval criteria.

## Checks

- Tailor the checklist to the files that changed.
- Do not ask irrelevant generic questions.
- Include validation evidence reviewers should expect.
