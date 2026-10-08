# Codex agent roles and skills

Reusable Codex subagent roles and two companion skills.

## Roles

| Role | Purpose |
| --- | --- |
| `analyst` | Clarifies requirements and trade-offs through focused questions using `grill-me`. |
| `developer` | Implements scoped changes and uses `refactor` for behavior-preserving refactoring. |
| `reviewer` | Reviews changes for actionable defects and regressions. |
| `qa` | Checks observable behavior and reports reproducible defects. |
| `orchestrator` | Coordinates specialist work, ownership, review, and verification. |

## Skills

| Skill | Purpose |
| --- | --- |
| `grill-me` | Pressure-tests ideas and scope one consequential question at a time. |
| `refactor` | Guides structural code changes while preserving observable behavior. |

## Install

Copy the roles and skills into your global Codex configuration:

```sh
mkdir -p ~/.codex/agents ~/.codex/skills
cp ./*.toml ~/.codex/agents/
cp -R ./skills/grill-me ./skills/refactor ~/.codex/skills/
```

The roles and skills contain no project-specific instructions. Follow each repository's `AGENTS.md` for project rules.

## Use

Assign a role when starting a Codex subagent task. Invoke a skill by name for a focused workflow, for example `$grill-me` or `$refactor`.
