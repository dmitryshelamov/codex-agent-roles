# Codex agent roles

Five reusable agent roles for Codex:

| Role | Purpose |
| --- | --- |
| `analyst` | Clarifies requirements and trade-offs through focused questions. |
| `developer` | Implements scoped changes and verifies them. |
| `reviewer` | Reviews changes for actionable defects and regressions. |
| `qa` | Checks observable behavior and reports reproducible defects. |
| `orchestrator` | Coordinates specialist work, ownership, review, and verification. |

## Install

Copy the role files into your global Codex agents directory:

```sh
mkdir -p ~/.codex/agents
cp ./*.toml ~/.codex/agents/
```

The roles contain no project-specific instructions. Follow each repository's `AGENTS.md` for project rules.

## Use

Assign a role when starting a Codex subagent task. The `orchestrator` role can coordinate the other specialists when delegation is appropriate.
