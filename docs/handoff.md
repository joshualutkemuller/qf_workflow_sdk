# QF Workflow SDK Handoff

## Snapshot

This handoff describes the state of `qf_workflow_sdk` after the initial documentation and worktree cleanup pass. The SDK is intended to become an agentic workflow kit for quants and data scientists. It currently has a repo skeleton, hook examples, GitHub workflow templates, and seed agent files oriented around the SDK.

## What Was Added

- `docs/sdk_plan.md`: roadmap, target users, SDK surfaces, phases, backlog, and success criteria.
- `docs/handoff.md`: this continuation guide for the next implementer.
- `README.md`: top-level SDK overview and usage orientation.
- `agentic_dictionary.md`: shared vocabulary for agents, hooks, prompts, instructions, templates, and quant workflow artifacts.

## Existing Assets

```text
qf_workflow_sdk/
  .agents/
    general/
    git/
    design/
  .githooks/
    commit-msg
    pre-commit
    pre-push
  .github/
    workflows/ci.yml
    PULL_REQUEST_TEMPLATE.md
    GIT_GUIDELINES.md
    ISSUE_TEMPLATE/
    dependabot.yml
  agents/
  hooks/
  instructions/
  prompts/
  setup-hooks.sh
```

The public folders `agents/`, `hooks/`, `instructions/`, and `prompts/` are currently empty and are the right places to build the quant-focused SDK surface.

## Important Context

The current repo contains hidden agent files and hooks that act as seed examples. These should not be deleted blindly because they are useful examples of the intended structure. Promote them into quant/data-science equivalents in small steps:

- Replace project-specific language with SDK language.
- Preserve the pattern of `prompt.md`, `instructions.md`, and `tasks.md`.
- Move public, reusable agent definitions into `agents/`.
- Keep `.agents/` for tool-specific adapter files or internal metadata if needed.
- Keep Git hooks independent from any downstream app directory unless a package-specific hook is introduced intentionally.

## Recommended Next Move

Start with the public agent catalog. The first useful slice should be:

```text
agents/
  research_analyst/
    README.md
    prompt.md
    instructions.md
    tasks.md
  data_quality/
    README.md
    prompt.md
    instructions.md
    tasks.md
  backtest_review/
    README.md
    prompt.md
    instructions.md
    tasks.md
```

These three agents cover the workflow from hypothesis to data inspection to simulation review, which is the center of gravity for most quant research work.

## Suggested Implementation Order

1. Add the first three public agents: Research Analyst, Data Quality, and Backtest Review.
2. Add shared instruction files under `instructions/`.
3. Add task prompts under `prompts/`.
4. Add document templates under a new `templates/docs/` folder.
5. Add examples that show full workflows from hypothesis to handoff.
6. Add stronger CI checks for Markdown, links, and public agent contracts.

## First Public Agent Acceptance Criteria

Each public agent should include:

- `README.md` with purpose, when to use it, inputs, outputs, and examples.
- `prompt.md` with the durable role prompt.
- `instructions.md` with behavioral rules and review standards.
- `tasks.md` with common task requests and expected artifacts.

Each agent should be narrow enough that a human or orchestrator can pick it without reading every file.

## Documentation Standards

Every reusable prompt or instruction should specify:

- Purpose.
- Required inputs.
- Expected output.
- Checks the agent should perform.
- Assumptions that must be surfaced.
- Failure modes or risks to watch for.

For quant work, always make time alignment, data lineage, leakage risk, survivorship bias, overfitting, transaction costs, and reproducibility visible when relevant.

## Hook Migration Notes

Current hooks are SDK-friendly and intentionally lightweight:

- `commit-msg`: keeps Conventional Commits and uses quant SDK examples.
- `pre-commit`: validates required SDK docs and hook shell syntax.
- `pre-push`: validates required SDK docs.

Hooks should warn when optional tools are missing, unless the missing tool invalidates a required guarantee.

## CI Migration Notes

The current CI performs lightweight SDK validation. Future CI improvements could add:

- Check Markdown links and formatting.
- Validate shell scripts with `shellcheck` if available.
- Run any Python tests if a package is added later.
- Verify required files exist for every public agent folder.
- Prevent reintroduction of old project-specific references after migration.

## Open Questions For The Owner

- Should this SDK become a Python package, a CLI scaffold, or a copyable repo template?
- Which agent runtime should be treated as the primary target?
- Should hooks be strict by default, or advisory until a team opts into strict mode?
- What quant artifact should be the first complete example: alpha signal, risk model, forecast model, optimizer, or execution model?
- Should generated documentation follow a house style, such as model cards and dataset cards, or adapt per team?

## Risks

- The SDK may become too broad if agents are not kept role-specific.
- Hooks may frustrate exploratory research if they block too much too early.
- Prompts without output contracts will be hard to automate.
- Quant workflow docs can look complete while hiding weak assumptions; every template should force assumptions and limitations into the open.

## Definition Of Done For The Next Slice

The next slice is complete when:

- At least three quant-focused public agents exist.
- No user-facing guidance points to obsolete app-specific workflows.
- Hooks do not assume an app directory that does not exist.
- README links to the new agents, instructions, prompts, and templates.
- One end-to-end workflow example shows how a hypothesis becomes a reviewed handoff artifact.
