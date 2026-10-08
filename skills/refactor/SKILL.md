---
name: refactor
description: Restructure existing code without changing observable behavior when refactoring is requested, following the project's architecture and cleanup conventions.
---

# Refactor

Improve the assigned code structure while preserving observable behavior. A planning
or audit assignment stays read-only and does not authorize implementation or cleanup.

- Establish the structural goal, owned scope, and behavior to preserve before editing.
  Identify relevant public contracts, errors, state changes, ordering, and numerical
  results. Use the current implementation as the regression baseline; report existing
  behavior that conflicts with requirements separately instead of silently correcting it.
- Follow applicable AGENTS.md and its references to architecture, accepted decisions,
  test conventions, and shared cleanup settings. Read the affected layer boundaries.
  Resolve the current repository's sources, such as docs/architecture.md and checked-in
  Rider/ReSharper .sln.DotSettings; do not replace them with personal style preferences.
- Make focused, independently verifiable transformations toward the stated structural
  goal. Keep feature work, bug fixes, contract changes, and unrelated cleanup outside
  this assignment unless separately authorized. If a needed change crosses ownership
  or an agreed boundary, return that decision to the parent or user before proceeding.
- Check callers and runtime discovery before deleting or renaming apparently unused
  code; absence of direct references alone is insufficient for reflection, registration,
  serialization, or externally consumed APIs.
- Establish relevant checks before editing and rerun them on the same scenarios after
  the change. Add focused characterization tests only where meaningful behavior lacks
  coverage. Adapt tests to internal moves without weakening their behavioral expectations;
  compilation alone does not demonstrate unchanged behavior.
- Apply the project's shared cleanup profile only to assigned files. Inspect its diff
  for changes beyond formatting; cleanup output still needs behavioral verification.
  If the configured tool cannot run, follow the documented rules where feasible and
  report the missing cleanup check without claiming the profile was executed.
- Report the structural improvement, preserved contracts, checks actually performed,
  and remaining verification gaps. Stop when the assigned structural goal is met.
