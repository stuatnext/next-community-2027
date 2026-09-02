# marketingNEXT (next-community-2027) — membership brochure

Single-page React (Vite + Tailwind v4) app selling the marketingNEXT annual
membership. All content lives in `src/App.jsx` as plain arrays near the top
(`WHY`, `FORMAT`, `STANDARD`, `PROGRAMME`, `INCLUDES`, `TERMS`, `APPLY_STEPS`)
plus the `CONTACT` and `PRICE` constants — edit the arrays, not the markup.

## Deploying to gh-pages — ALWAYS

After any change that affects the site, **redeploy to gh-pages** so the live
site stays current. Do this without being asked, as part of finishing the work:

```
npm run deploy   # = vite build && npx gh-pages -d dist
```

Confirm it prints `Published` before reporting done. Publishes to
`https://stuatnext.github.io/next-community-2027/` once Pages is enabled
for this repo.

## Workflow

- Develop on branch `claude/2027-ticket-pricing-brochure-p79mqg`.
- Run `npm run build` to verify changes compile.
- Redeploy gh-pages (see above).
- Commit with a clear message and push the branch.
- Open a fresh PR into `main` only when asked.

## Branding — marketingNEXT, not NEXT.io house style

Communities carry their own identity (same rule as HR Connect). Do **not**
restyle this toward the summit dark-grey/yellow system.

- Editorial paper-and-ink palette with a single vermilion accent: paper
  `#f5f1e8`, ink `#191511`, vermilion `#c73e1d` — defined as `mn-*` tokens in
  `src/index.css`. Vermilion is the only accent; never add a second.
- Type is Fraunces (display, loaded with italics) + Archivo (text), via
  Google Fonts in `index.html`.
- The wordmark is live text via the `<Wordmark>` component: Fraunces italic
  "marketing" + Archivo black "NEXT". There is no logo file; if brand assets
  ever arrive, swap inside `<Wordmark>` so every usage follows.
- The `.mark-sweep` / `.mark-sweep-paper` utilities are the red marker stroke
  behind key words — the signature device. Use sparingly (once per section
  at most).

## Content rules — what the page sells

- **One product only**: annual membership, `PRICE` = €4,000 per company per
  year, flat, no tiers, no per-seat uplift (Stuart, 2 Sep 2026 — the brochure
  sells paid membership; the project brief's "free in 2027" framing is
  superseded for this page).
- The includes list is the validated set from the brief's membership block:
  2 senior seats (company-held), all monthly sessions, 4 guest passes,
  peer-on-demand, 2 Valletta Full Event passes, the annual benchmarking
  report. Two further items from the brief (group buying rates, collaborative
  tool discounts) are **deliberately excluded** — Alina flagged them as
  unvalidated ("I don't know how it works in practice"). Do not add them
  until the mechanics are confirmed.
- `CONTACT` is the enquiry address used by every mailto (application CTA is a
  templated mailto). Set on the firstname@next.io pattern — confirm with
  Alina before first external send.

## Internal-only material — never publish

The marketingNEXT project brief is an internal document. These must not
reach the site: the €50k ARR target and paying-company count, the projected
budget (community-manager headcount, activation spend), KPI tables and
targets (attendance, NPS, conversion), team responsibilities and time
allocations, the commercialisation framing ("prove the format before
commercialising", 2028 pricing rationale), sponsorship/Q4 monetisation
plans, and the founding-member list — **names, companies, emails and
statuses stay internal**; founding members are described, never named,
and naming one needs their written permission first.

Also note: the brief says "operators only" but the founding cohort is
supplier-heavy — the page deliberately says "senior iGaming marketers"
and doesn't gate by company type. If that gate is ever decided for real,
update the STANDARD array, not just the hero.
