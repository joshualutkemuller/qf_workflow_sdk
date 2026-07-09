# QF Workflow SDK

QF Workflow SDK is an agentic workflow kit for quants, researchers, and data scientists. It is designed to organize agents, prompts, instructions, hooks, and documentation templates that make quantitative research and model development more reproducible, reviewable, and easier to hand off.

The SDK is intentionally practical: it should help teams document assumptions, review data quality, reduce avoidable modeling mistakes, enforce lightweight workflow standards, and produce artifacts that another researcher or engineer can pick up later.

## What This SDK Is For

- Planning quant research from a hypothesis.
- Reviewing data lineage, joins, timestamps, missingness, and leakage risk.
- Documenting features, models, datasets, experiments, and backtests.
- Creating agent roles for common research and data-science workflows.
- Adding hooks that catch avoidable quality issues before commit or push.
- Giving teams a shared vocabulary for agentic quant workflows.

## Current Repository Shape

```text
qf_workflow_sdk/
  README.md
  agentic_dictionary.md
  setup-hooks.sh
  .agents/
  .githooks/
  .github/
  agents/
  hooks/
  instructions/
  prompts/
  docs/
```

Current state notes:

- `.agents/` contains seed agent examples for general, Git, and design-oriented workflows.
- `.githooks/` contains seed Git hooks.
- `.github/` contains seed GitHub workflow and contribution templates.
- `agents/`, `hooks/`, `instructions/`, and `prompts/` are the intended public SDK surfaces.
- The old app-specific assets have been removed from the working tree; the remaining seed files now describe the SDK workflow.

## Main Concepts

- Agents define durable roles such as Research Analyst, Data Quality Reviewer, Modeling Reviewer, Backtest Reviewer, Risk Reviewer, Documentation Agent, and Git/Release Agent.
- Instructions define reusable standards and behavioral rules that agents follow.
- Prompts define task-specific starting points with clear inputs and outputs.
- Hooks define local quality gates for commits, pushes, documentation, notebooks, tests, and sensitive files.
- Templates define repeatable artifacts such as research memos, dataset cards, model cards, experiment reports, and handoff memos.

See `agentic_dictionary.md` for the shared vocabulary.

## Suggested Quant Workflow

1. Start with a hypothesis and use a Research Analyst Agent to draft the research plan.
2. Use a Data Quality Agent to inspect source data, joins, timestamp alignment, coverage, and leakage risk.
3. Use a Feature Engineering or Modeling Agent to document transformations, model choices, validation design, and assumptions.
4. Use a Backtest Review Agent to inspect bias, costs, benchmarks, fragility, and robustness.
5. Use a Risk Agent to summarize exposures, concentration, drawdowns, stress behavior, and monitoring needs.
6. Use a Documentation Agent to produce a research memo, model card, dataset card, experiment summary, and handoff memo.
7. Use Git hooks and PR templates to keep changes reviewable and reproducible.

## Local Hook Setup

From inside `qf_workflow_sdk`, run:

```sh
./setup-hooks.sh
```

The current hooks are seed examples and should be updated before relying on them for production quant workflows. In particular, the current pre-commit and pre-push hooks still assume an older app layout.

## Documentation

- `docs/sdk_plan.md`: roadmap and proposed SDK architecture.
- `docs/handoff.md`: continuation guide for the next implementer.
- `agentic_dictionary.md`: definitions for the SDK vocabulary.

## Recommended Next Steps

- Build public agents under `agents/`.
- Add reusable instructions under `instructions/`.
- Add task prompts under `prompts/`.
- Add document templates under `templates/docs/`.
- Replace app-specific hooks and CI with SDK validation checks.

## Design Principles

- Make expert review easier, not optional.
- Keep agent roles narrow and inspectable.
- Surface assumptions, limitations, data lineage, and validation choices.
- Treat leakage, time alignment, survivorship bias, overfitting, and transaction costs as first-class review concerns.
- Prefer reproducible artifacts over conversational memory.
- Let exploratory work stay fast while making handoff work rigorous.
