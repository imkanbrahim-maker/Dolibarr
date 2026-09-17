# Project Context — Dolibarr DZ Landing Page

Compact AI memory for this project. Derived knowledge only: the real files win over
anything written here. If context conflicts with the project, trust the project,
fix the context, continue.

## Files

- `config.md` — how this context is maintained (automatic / standard / project).
- `structure.md` — which context files exist, what belongs where, level rules.
- `project.md` — what the project is: purpose, offer, stack, sections, lead flow.
- `conventions.md` — how to modify the page safely (copy, design, JS contracts, deploy).

No `domains/` (scope is `project`).

## Reading workflow (before substantial work)

```text
config.md → structure.md → project.md → conventions.md → index.html (verify)
```

Task shortcuts:

- Copy/text task → `project.md` (offer/audience) + `conventions.md` (copy rules), then `index.html`.
- Design/UI task → `conventions.md` (design + classes), then `index.html`.
- Form/JS task → `conventions.md` (JS contracts) + `project.md` (lead flow), then `index.html`.
- Trust/links task → `project.md` (external references), then verify in `index.html`.

Never edit source to match stale context. After meaningful changes, update only the
affected file(s) per `config.md` (automatic mode).
