# Project context and decision records

Use the project's established documentation locations and conventions. If `CONTEXT-MAP.md` exists, use it to locate the relevant domain context; otherwise use the root `CONTEXT.md`. Read relevant existing ADRs before recording decisions.

## Domain glossary: CONTEXT.md

- Record a term as soon as its definition is agreed. Create the file when there is a substantive first entry.
- Use a context title, a short description, and a terms section. Each entry contains the canonical term, a one- or two-sentence definition, and discouraged synonyms when useful.
- Test ambiguous terms against concrete scenarios and the current code. Surface differences between actual and desired behavior for discussion.
- Keep implementation details, task plans, and speculative hypotheses out of the glossary. Keep open questions in the chat summary or the project's existing requirements document.

## Decision records: ADRs

- Record an agreed decision when changing it would be costly, its rationale would be unclear to a future reader, and it involves a genuine trade-off. Recommendations are not accepted decisions.
- Unless the project establishes another convention, use `docs/adr/NNNN-short-title.md` with the next available number.
- Include a title, circumstances, the choice, and its rationale. Add alternatives and consequences when useful.
- When a decision changes, preserve the earlier ADR's history and link to its replacement.

If writing is unavailable, disclose that limitation and provide the proposed records in chat.
