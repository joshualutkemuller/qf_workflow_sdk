# Prompt: Handoff Memo

## Purpose

Create a handoff memo for a quant research, model, data, or backtest workflow.

## Required Inputs

- Project or artifact name.
- Current state.
- Decisions made.
- Source docs, code paths, data references, and experiment IDs.
- Validation status.
- Known risks and blockers.
- Next owner or reviewer.

## Prompt

Use `instructions/documentation.md`.

Create a handoff memo from this context:

```text
{handoff_context}
```

Return a Markdown memo with:

- Snapshot.
- Goal.
- Current state.
- Key decisions.
- Source references.
- Validation status.
- Known risks and limitations.
- Open questions.
- Next actions.
- Owner and reviewer notes.

## Checks

- Make it possible for another qualified person to continue without reconstructing context from chat history.
- Keep unresolved issues visible.
- Distinguish planned work from completed work.
