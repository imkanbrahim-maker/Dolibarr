# Context Structure Specification

Generic fallback — no framework template applies (static single `index.html`, no build, no backend).

## Available files
- `README.md` — entry point, navigation. Never duplicates other files.
- `config.md` — update mode, detail level, scope, template.
- `structure.md` (this file) — organization contract.
- `architecture.md` — stack, page sections, styling system, JS behaviors, critical conventions.

No `domains/` at current scope.

## Purpose / belongs / not belongs
- `architecture.md`:
  - Belongs: project purpose, stack (Tailwind CDN + vanilla JS + Cairo/Tajawal), section map of `index.html`, shared visual system (glass, gold-text, cta, fade-up, dash-frame), JS behaviors (reveal, countdown to 2026-09-30T19:00+01:00, spots scarcity, DZ form validation), RTL/Arabic conventions.
  - Not belongs: per-class CSS inventory, full copy of HTML, generic Tailwind docs, temporary copy tweaks.

## Conditions for creating files
- Create a new file only when a persistent, project-wide knowledge area appears that does not fit `architecture.md` (e.g. backend/API added → `api.md`; real DB added → `database.md`; second landing/funnel added → `workflows.md`).
- Never create per-section, per-component, or per-function files for this single-file page.
- `domains/` only if scope widens beyond `project` AND a meaningful business domain needs its own home (e.g. registration + payment + delivery as separate systems). Not now.

## Per-detail-level structures
- `minimal` (current): `README.md, config.md, structure.md, architecture.md`
- `standard`: `+ conventions.md, workflows.md` — only if page gains reusable patterns / multi-step funnels worth capturing separately.
- `detailed`: `+ decisions.md, integrations.md` — only if complex decisions or real integrations (CRM, email, WhatsApp API) appear.

Files outside the current level must not exist.
