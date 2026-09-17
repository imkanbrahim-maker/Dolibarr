# Conventions — How to Modify This Page Safely

## Copy (hard rules)

- All visible copy in **Algerian Darja (Arabic script)**, professional/persuasive/direct.
- Always name **Dolibarr** explicitly in major headings/CTAs; never generic "système" alone.
- Never reintroduce: formation/webinar/course content, Power BI, English-baked visuals as copy.
- Keep PAS structure (problem → agitation → solution) and benefit-led headings.

## Design

- Light premium SaaS: white/slate surfaces, navy `#0A1633` bands
  (hero, solution, offer, final CTA). White text + `gold-text-light` on navy only.
- Reused classes: `glass` (white card), `glass-strong` (navy card), `gold-text` /
  `gold-text-light` (use light variant on navy only), `cta` + shine, `fade-up`
  (needs IntersectionObserver in JS), `floating`, `ticker`, `chart-bar`, `dash-frame`.
- RTL: page is `dir="rtl"`; use logical/mirrored layouts, `dir="ltr"` only for
  refs/phone/email/numbers. Keep `h1/h2/h3` line-height overrides (Arabic overlap fix).

## Section/JS contracts (do not break)

- IDs read by JS: `registrationForm`, `fullname/phone/email/company/activity/need`,
  `.err` messages, `submitButton/buttonText/buttonArrow`, `formContainer`,
  `successMessage/successDetail/waShare`, `placesBar/placesLeft`.
- FAQ uses native `<details>` (first open by default); do not replace with custom JS accordion
  without reason. `prefers-reduced-motion` must keep working.

## Assets & deploy

- `Dolibarr.jpg` must ship next to `index.html` (relative `src`); keep Unsplash `onerror`
  fallback chain on the hero `<img>`. One `<img>` total unless a task adds imagery.
- WhatsApp number `213550000000` appears twice (sticky button + final CTA note) — update both.
- Scarcity values and client counts are volatile marketing numbers, not context facts.
- Verify after edits: tags balanced, no Power BI/formation leftovers, form validates,
  page opens directly from disk.
