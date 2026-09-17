# Architecture — Power BI DZ Webinar Landing

## Purpose
Free-webinar lead capture (30 Sept 2026, 19:00 Algiers, Zoom Live 45min) + free sales-tracking Template bonus. Audience: DZ shop owners, e-commerce, PME managers. Language: Arabic RTL, Algerian Darija + French terms (Chiffre d'affaires, Bénéfice, Stock).

## Stack
- Single static `index.html` (~674 lines), no build, no backend.
- Tailwind via CDN + inline `tailwind.config` (colors: power #F2C811, night #070B14, panel #0C1322, card/card2; fonts Cairo/Tajawal).
- Custom CSS in `<style>`: grid-bg, panel/panel-hover, eyebrow, btn-ghost, gold-text (static gradient), cta shine (slow), fade-up reveal, pulse-dot, chart-bar growBar, dash-frame, ticker, kpi/hero fixes, reduced-motion guard.
- Vanilla JS at end of body, no deps.

## Page map (index.html order)
1. Top bar urgency + sticky navbar (`#navbar`) → CTA `#inscription`.
2. Hero `#top`: copy + social proof + countdown (`#cd-d/h/m/s`) + spots (`#placesLeft`, `#placesBar`) + dashboard mockup (KPI cards, 8 bars, Top produits, floating badges) + tools ticker strip.
3. `#problem` (3 pain cards) → `#solution` (3 steps + before/after) → `#program` (01/02/03 timeline) → ROI benefits (4 cards) → `#bonus` Template gift → integrations grid (Excel/Shopify/WooCommerce/Odoo/Dolibarr) → `#faq` (4 `<details>`) → final CTA → `#inscription` form → footer + WhatsApp float + mobile sticky CTA.

## Critical conventions
- RTL: `<html dir="rtl" lang="ar">`; ticker/inner LTR islands use explicit `dir="ltr"`. Numbers/prices needing LTR get `dir="ltr"`.
- Visual tokens: `panel` for cards, `panel-hover` for lift-on-hover, `eyebrow` for section labels, `gold-text` (static) for key headline span, `cta` for primary buttons, `btn-ghost` for secondary buttons, `fade-up` + IntersectionObserver for reveal, `dash-frame` wrapper for dashboard.
- Overlap guards: `h1/h2/h3` line-height 1.6–1.7, `.kpi-card{min-width:0;overflow:hidden}`, `.kpi-num` tabular + break, `.hero-grid{overflow:visible}` + dashboard `mb-14 lg:mb-6` for floating badges.
- Countdown target is fixed: `2026-09-30T19:00:00+01:00`. Spots bar starts 73% / 27 left, JS decrements to min 14.
- Form `#registrationForm` (novalidate, custom DZ validation): name ≥3, phone `/^(0)(5|6|7)[0-9]{8}$/` after stripping spaces/dashes/dots, email regex, company ≥2, activity required. Success hides `#formContainer`, shows `#successMessage`, updates `#waShare`.
- Reading comfort: body copy floor is `slate-300` (muted `slate-400`, faint `slate-500`); motion is calm (ticker ~38s, CTA shine 6s, gentle float, no float on dashboard mockup, static gold gradient); anchored sections use `scroll-margin-top:88px` for the sticky navbar. Arabic readability: no letter-spacing (`tracking-*`) on Arabic text, weight 700 max on small (≤13px) labels, 900 reserved for display headings.

## Integrations (front-only, no backend)
- Form submit is simulated (setTimeout 1200ms) — no API call. WhatsApp links (`wa.me/213550000000`, `wa.me/?text=`) are placeholders.
- Tool mentions (Excel, Shopify, WooCommerce, Odoo, Dolibarr) are marketing copy only, no real connectors.

## What not to do
- Do not add build tools, frameworks, or backend without explicit request.
- Do not duplicate the tools strip content in two places without differentiating (hero ticker vs grid serve different roles).
- Do not break RTL when editing ticker/animations — keep `dir` attributes and line-height guards.
