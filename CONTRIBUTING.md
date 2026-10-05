# Contributing to perplexity-scenario-factory

Thanks for your interest in improving the Scenario Factory!

## How to Contribute

### 1. Request or write a scenario
- Check `catalog/000-master-table.md` for the full list of planned scenarios.
- Unwritten scenarios (no guide in `catalog/guides/`) are open for contribution.
- Use `UC-XXX-topic.md` naming and follow the structure of existing guides.

### 2. Fix or improve an existing guide
- Keep guides additive: corrections are welcome, wholesale rewrites are not.
- Preserve the front-matter structure so tooling and the master table stay in sync.

### 3. Add agent instructions or skills
- New agent instruction sets go in `agent-instructions/`.
- Skills follow the existing category folders in `skills/` (research, web, productivity, commerce).

## Ground Rules

- Nothing gets deleted — improvements supersede, they never remove.
- Every meaningful change updates the LLM-Wiki (`memory/wiki/`) and, if task-related, the backlog.
- Be specific: a scenario should be executable by someone other than its author.

## Commit Style

`<area>: <what changed> (iteration YYYY-MM-DD)` — e.g. `catalog: add UC-011 supplier-scouting scenario (iteration 2026-10-06)`
