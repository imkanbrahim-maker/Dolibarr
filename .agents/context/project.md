# Project — Dolibarr DZ Landing Page

## Purpose

Arabic (Algerian Darja) lead-generation landing page for **Dolibarr ERP services in Algeria**.
Converts visitors into qualified leads via free demo/diagnostic request form.
100% services focus: installation, stock, invoicing, HR, custom modules, local support.
No training/webinar content. No Power BI content (removed by explicit decision).

## Audience

Decision-makers in Algeria: physical shop owners, e-merchants, boutique managers, SME founders.
They lose time on Excel/paper and lack visibility on real profit and stock.

## Offer (services sold)

1. Dolibarr installation + hosting (cPanel, 48h, DA currency, droit de timbre).
2. Stock + invoicing core (entries/exits, alerts, Factures/Devis in 1 min, Caisse/bank/client credit).
3. HR & payroll basics. 4. Sur-mesure modules. 5. Store liaison (Shopify/WooCommerce/Excel/barcode).
6. Local support in Darja (WhatsApp 7/7, backups). Trust: Dolibarr V24, Open Source, 150+ clients claim.

## Stack

Single static `index.html` (RTL, `lang="ar"`). Tailwind CSS via CDN + inline `tailwind.config`
(gold/navy palette). Cairo/Tajawal fonts, Font Awesome 6 icons, vanilla JS at page bottom.
No build step, no backend: open the file in a browser to test.

## Page sections (in order)

Top bar → navbar → hero (copy + `Dolibarr.jpg` photo + single proof line + inline trust row) →
problem → solution (navy band) → 6 services → benefits → offer (navy card) → integrations grid →
FAQ (5 `<details>`) → final CTA (navy) → lead form `#inscription` → footer →
sticky WhatsApp + mobile sticky CTA.

## Lead flow

Form `registrationForm`: name, phone (DZ `05/06/07` + 10 digits), email, company, activity, need.
JS validates inline (Darja errors), simulates submit (loading → personalized success + WhatsApp
share link), decrements scarcity counter. **No data leaves the browser** — backend wiring is
an open future task, not present.

## External references

- `https://www.dolibarr.org/` (official site, V24) and `/onlinedemo.php`, linked from hero/FAQ/footer.
  We are a local integrator, not the software editor (Open Source = free software; clients pay
  for setup/services only).
- CDN: Tailwind, Google Fonts, Font Awesome, Unsplash (image fallback only).

## Assets

- `index.html`, `Dolibarr.jpg` (hero, local relative path — deploy together),
  `PROMPT-Dolibarr-Services.md` (positioning spec, not user-facing).
