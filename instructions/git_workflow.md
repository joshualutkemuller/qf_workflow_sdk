# Git Workflow Instructions

## Purpose

Use this instruction set when making repository changes for quant workflow assets, including agents, prompts, instructions, templates, hooks, examples, and documentation.

## Required Inputs

- Intended change scope.
- Current branch and worktree status.
- Files to modify.
- Validation commands or checks.
- Commit or pull request target.

## Expected Output

- Focused change set.
- Clear commit message.
- Validation summary.
- Handoff notes for reviewers.

## Standards

- Keep changes small and reviewable.
- Use Conventional Commits.
- Do not mix unrelated SDK surfaces in one change unless the handoff explains why.
- Preserve user changes that are outside the current task.
- Keep public agent contracts consistent: `README.md`, `prompt.md`, `instructions.md`, and `tasks.md`.
- Update README or handoff docs when public SDK surfaces change.

## Checks

- Is the worktree status understood before editing?
- Are only intended files staged?
- Do hooks and CI still match the repository structure?
- Are new public assets linked from README or docs?
- Are validation results reported?

## Common Failure Modes

- Staging unrelated local work.
- Letting docs drift from folder structure.
- Adding prompts without expected inputs and outputs.
- Adding hooks that assume a downstream app structure.
