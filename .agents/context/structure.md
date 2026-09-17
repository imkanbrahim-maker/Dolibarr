# Context Structure Specification

Project: Dolibarr DZ landing page (single static file). No framework, no backend, no database.
Template: none (generic fallback — structure derived from the actual project).

## Files

- `README.md` — entry point and navigation. Routes, never contains project knowledge.
- `config.md` — update mode, detail level, scope, template. Only file that defines maintenance behavior.
- `structure.md` — this specification. Changes only when context organization changes.
- `project.md` — project-wide knowledge: purpose, audience, offer, stack, page sections, lead flow,
  external references, assets. The only home for "what this project is".
- `conventions.md` — rules for safely modifying the page: copy, design, RTL, section/JS contracts,
  assets, deployment. The only home for "how to change this project".

## What does not belong

- Per-section copy dumps, class lists, or line-by-line file inventories.
- Generic Tailwind/HTML/JS documentation (only this project's usage).
- Temporary details (phone numbers, counts, scarcity values change often — never context).
- `domains/` — scope is `project`; no domain files unless scope changes via deliberate structure change.

## Creation conditions

- New file only when knowledge appears that fits no existing file AND recurs across tasks.
- `decisions.md` (detailed level only): created if/when detail level is raised to `detailed`,
  to record architectural/marketing decisions with reasons.
- Never create speculative files.

## Per-detail-level structures

```text
minimal:   README.md, config.md, structure.md, project.md
standard:  + conventions.md
detailed:  + decisions.md
```

Current level is `standard`: all five core files exist except `decisions.md` (detailed-only).
Files outside the current level's set must not exist.
