---
name: seo-competitor-gap-report
description: Build a data-backed SEO competitor gap report comparing one website against 5–6 competitors, cross-checking Semrush, Ahrefs and Google Search Console (via Supermetrics). Use when asked for a competitor analysis, gap audit, SEO benchmark or "how do we beat X in search".
---

# SEO Competitor Gap Report

Produces a decision-ready report: your site vs 5–6 competitors on one focus topic, covering keyword, content, backlink, on-page and AI-search gaps, with every opportunity scored on impact and effort and turned into a 90-day plan.

**Principles**
- Every number comes from a tool call. Never estimate a figure to fill a cell.
- Two sources for headline metrics (Semrush + Ahrefs). Show disagreements; don't hide them.
- Real first-party data (Search Console) beats third-party estimates for your own site.
- Every recommendation cites the data point behind it.

## Step 0 — Collect inputs (ask once)

1. Your website URL and the focus page / service
2. 5–6 competitor domains (or permission to discover them)
3. Target market → Semrush database (`us`, `uk`, `ae`, `in`, `de`, …) and Ahrefs country
4. 3–5 seed keywords or the focus topic
5. Brand terms (to split branded vs non-branded queries in Search Console)

If running unattended, discover competitors with Semrush `domain_organic_organic` (top relevance, excluding marketplaces and directories) and state which were chosen.

## Step 1 — Check connections and budget

| Tool | Check | If it fails |
|---|---|---|
| Semrush | `domain_overview` discovery → reports `available: true` | Ask the user to connect Semrush |
| Ahrefs | `subscription-info-limits-and-usage` → note units left | Ask the user to connect Ahrefs |
| Supermetrics | `data_source_discovery(ds_id="GW")` → `AUTHENTICATED` | Share the login link; continue without GSC and label own-site numbers as estimates |

Tell the user the expected API-unit cost before pulling (see `references/data-pull-map.md`). Keep `display_limit` tight.

## Step 2 — Pull data

Follow `references/data-pull-map.md` for the exact reports. Save every pull as a CSV in the working directory so numbers can be re-checked.

1. **Scorecard** – all 7 domains: traffic, keywords, Authority Score, DR, referring domains
2. **Keyword universe** – seed + related keywords: volume, KD, CPC, intent
3. **Keyword gap** – shared / missing / unique keywords (Semrush max 5 domains per call → run twice)
4. **Own-site reality** – Search Console, last 90 days: queries, pages, clicks, impressions, CTR, position
5. **Content gap** – competitors' top pages by traffic, grouped into topics
6. **Backlink gap** – referring domains linking to 2+ competitors but not to you
7. **SERP + on-page** – top 10 for the main keyword; fetch your page and the top competitor pages
8. **AI search visibility** (optional) – Ahrefs Brand Radar mentions / citations / share of voice

## Step 3 — Analyse

- **Cross-check**: where Semrush and Ahrefs differ by more than 30%, show both and note it.
- **Striking distance**: GSC queries at positions 8–20 with meaningful impressions.
- **Low CTR**: high-impression queries with CTR well below the position average.
- **Consensus gaps**: keywords where 3+ competitors rank in the top 20 and you don't.
- **Link targets**: drop scraper, spam and PBN-looking domains before listing them.
- **Score** every opportunity with `references/prioritisation.md`.
- **Consistency pass**: word counts, targets and timelines must match across sections.

## Step 4 — Write the report

Use the structure in `references/report-template.md`. Put the scorecard and top 5 opportunities on page 1. Deliver as a shareable doc unless the user asks for Word or PDF.

## Step 5 — Verify before delivering

- Spot-check 5 numbers against the raw CSVs
- No empty cells: write "no data (tool)" where a tool returned nothing
- No contradictions between sections
- Every recommendation cites a data point
- Forecasts are labelled as estimates, not guarantees
- Tell the user the actual API units used
