# Prompt: Research Plan

## Purpose

Draft a research plan from a quant or data-science hypothesis.

## Required Inputs

- Hypothesis or research question.
- Target universe or population.
- Intended decision or output.
- Candidate data sources.
- Time horizon and evaluation window.
- Known constraints.

## Prompt

Use the Research Analyst Agent and `instructions/quant_research.md`.

Draft a research plan for the following hypothesis:

```text
{hypothesis}
```

Use this context:

```text
{context}
```

Return a Markdown plan with:

- Research question.
- Hypothesis and rationale.
- Target universe or population.
- Required data and lineage concerns.
- Feature, label, and horizon definitions if applicable.
- Baseline and benchmark.
- Experiment design.
- Metrics and acceptance criteria.
- Leakage, bias, and overfitting risks.
- Reproducibility requirements.
- Stop conditions.
- Open questions.
- Next actions.

## Checks

- Make assumptions explicit.
- Do not claim evidence that was not supplied.
- Include at least one simple baseline.
- Identify what would falsify or pause the idea.
