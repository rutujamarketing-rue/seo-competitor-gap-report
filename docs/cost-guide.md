# Cost Guide

Estimates for one run (your site + 6 competitors, one focus topic). Unit prices can change, so check your own plan.

## Semrush API units

| Pull | Report | Rows | Approx. units |
|---|---|---|---|
| Scorecard | `domain_rank` × 7 | 7 | ~70 |
| Backlink comparison | `backlinks_comparison` | 7 | ~280 |
| Keyword gap | `domain_domains` × 2 runs | ~100 each | ~16,000 |
| Shared backlinks | `backlinks_matrix` | ~200 | ~8,000 |
| Keyword research + SERP | various | — | ~2,000–4,000 |
| **Total** | | | **~25,000–30,000** |

**To cut cost:** lower `display_limit` on the keyword gap (the biggest line), and use 5 competitors so a single gap run covers everyone.

## Ahrefs API units

Roughly **5,000–20,000** depending on row limits. Check before and after with `subscription-info-limits-and-usage`, which is free.

## Search Console via Supermetrics

This doesn't use Semrush or Ahrefs units. It counts toward your Supermetrics plan's query limits.

## Claude usage

A full run takes about 40–60 tool calls plus a long written report, so it's a heavy task. Tips:
- Start a **fresh conversation** for each run
- Skip the AI-visibility section if you don't need it
- Do a test run with 3 competitors and 1 keyword first
