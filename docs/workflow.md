# Workflow

```mermaid
flowchart TD
    S0[0. Inputs<br/>site · focus page · 5–6 competitors · market · seed keywords · brand terms]
    S1[1. Check connections<br/>Semrush · Ahrefs · GSC via Supermetrics<br/>+ estimate API units]
    S2a[Scorecard<br/>traffic · AS · DR · ref. domains]
    S2b[Keyword universe + gap<br/>volume · KD · intent · consensus gaps]
    S2c[Own-site reality<br/>GSC clicks · CTR · positions]
    S2d[Content gap<br/>competitors' top pages]
    S2e[Backlink gap<br/>domains linking to 2+ competitors]
    S2f[SERP + on-page<br/>top 10 · page checks]
    S2g[AI visibility<br/>Brand Radar]
    S3[3. Analyse<br/>cross-check sources · striking distance · score impact × effort]
    S4[4. Write report<br/>12 sections · scorecard on page 1]
    S5[5. Verify<br/>spot-check · no blanks · no contradictions · report units used]

    S0 --> S1 --> S2a & S2b & S2c & S2d & S2e & S2f & S2g --> S3 --> S4 --> S5
```

## Step-by-step

| Step | What happens | Output |
|---|---|---|
| 0. Inputs | Collect site, competitors, market, keywords, brand terms | Brief |
| 1. Connections | Confirm each tool works; estimate cost | Go / no-go |
| 2. Data pulls | Run reports per `references/data-pull-map.md` | CSVs |
| 3. Analysis | Cross-check, find gaps, score opportunities | Opportunity matrix |
| 4. Report | Fill `references/report-template.md` | Shareable doc |
| 5. Verify | Quality checks | Final report + units used |

## Design decisions

- **Focus on one topic per run.** Whole-site comparisons get shallow; one commercial topic gives actionable depth.
- **Two sources per headline metric.** Third-party tools estimate. Showing both values builds trust with stakeholders.
- **First-party data wins.** Search Console overrides third-party estimates for your own site.
- **Consensus gaps over single-competitor gaps.** If three or more competitors rank for something, the demand is proven.
