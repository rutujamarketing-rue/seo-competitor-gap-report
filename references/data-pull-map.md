# Data Pull Map

Which tool and report answers each question, and roughly what it costs. Unit prices are what Semrush reported via its MCP at the time of writing; always re-check with `get_report_schema`.

## Semrush (MCP)

Flow: discovery tool → `get_report_schema(report)` → `execute_report(report, params)`.

| Question | Toolkit → report | Approx. cost |
|---|---|---|
| Traffic, keyword count, traffic value per domain | `domain_overview` → `domain_rank` | 10 units / line |
| Trend over time | `domain_overview` → `resource_rank_history` | 10 units / line |
| Authority Score, backlinks, referring domains for all domains | `competitors_research` → `backlinks_comparison` | 40 units / line |
| Who are the organic competitors? | `competitors_research` → `domain_organic_organic` | 40 units / line |
| Shared / missing / unique keywords (max 5 domains) | `competitors_research` → `domain_domains` | 80 units / line |
| Referring domains shared across competitors | `competitors_research` → `backlinks_matrix` | 40 units / line |
| Volume, KD, CPC, intent, SERP results | `keyword_research` reports | varies |
| Keywords a page / domain ranks for | `organic_research` reports | varies |

**Typical run (7 domains):** ~25,000–30,000 units. The keyword gap (`domain_domains`) is the biggest cost, so cap `display_limit` at ~100.

## Ahrefs (MCP)

Call `doc` before using a tool for the first time. Monetary values are returned in USD cents.

| Question | Tool |
|---|---|
| Domain Rating | `site-explorer-domain-rating` |
| Organic traffic, keywords, traffic value | `site-explorer-metrics` |
| Top pages by traffic (content gap) | `site-explorer-top-pages` |
| Referring domains (backlink gap cross-check) | `site-explorer-referring-domains` |
| Organic competitors | `site-explorer-organic-competitors` |
| SERP snapshot | `serp-overview` |
| Keyword metrics | `keywords-explorer-overview` |
| AI search mentions / citations / share of voice | `brand-radar-*` |
| Units left | `subscription-info-limits-and-usage` (free) |

**Typical run:** ~5,000–20,000 units depending on row limits.

## Google Search Console (via Supermetrics MCP)

1. `data_source_discovery(ds_id="GW")` → confirm `AUTHENTICATED`
2. `accounts_discovery(ds_id="GW")` → pick the site property
3. `field_discovery(ds_id="GW")` → use field IDs only
4. `data_query(... date_range_type="last_90_days", settings={"brand_keywords": "brand|brand name"})`
5. `get_async_query_results(schedule_id=...)` → poll until data

Pull: query × page with clicks, impressions, CTR, average position.

## On-page checks

Fetch your focus page and the top 3–5 competitor pages. Record: title, meta description, H1, H2/H3 structure, word count, exact-phrase use, schema types, `og:type`, internal links in, proof elements (case studies, logos, testimonials, named experts).
