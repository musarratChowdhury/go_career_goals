# Refresh targets — update protocol

**Run `update go-projects-cv` when any trigger fires.** Output a delta to `diffs/YYYY-MM-DD_delta.md`; do not replay the investigation.

## Numbers to re-check
| Target | Current value | Source | Where it moves |
|---|---|---|---|
| HackerRank hiring asymmetry (senior vs entry) | +19–22% vs +7% | 04 (2025 report) | next annual report (~Q4 each year) |
| CodePath/Fortune non-interview signal ranking | portfolios #1 at 38% | 19 (Dec 2025) | follow-up surveys from CodePath; Fortune hiring coverage |
| Referral share of hires | 30–50% (40–50% tech) | 20 (aggregated benchmarks) | Jobvite/LinkedIn annual recruiting reports |
| GitHub activity sparsity | 83% zero commits/year | 17 (2018 data!) | **high priority** — rerun equivalent analysis; 2018 vintage is the corpus's weakest recency point |

## Entities to watch
- **Go Developer Survey** (go.dev/blog) — next results: does the concurrency-guidance gap for new Gophers persist? (bears on H4, F4)
- **CodeCrafters / build-your-own-x** — new languages/challenges, pricing, and any hiring-partner claims (bears on F3; watch for astroturf-flagged HN threads)
- **HackerRank report, Stack Overflow survey, JetBrains survey** — any question on portfolio/GitHub evaluation behavior
- **Atlassian-style take-home guidance** — modernized (AI-era) versions from major employers

## Hypothesis watch-list
- **H3** is the most fragile verdict (qualified "confirmed"). If a credible study measuring actual repo-open rates or callback-lift from portfolio links appears → reopen F1.
- **H2's CV-value half** stays "inferred" until a hiring-manager source explicitly grades wheel-projects. Watch HN/Reddit hiring threads for direct testimony.
- **Adversarial trigger:** if a major employer publishes "we no longer look at take-homes/portfolios" policy → re-run Channel A + D only (delta).

## Corpus gaps worth a follow-up round
1. Reddit r/golang fetch (blocked 403 this run) — human-fetch or alternative mirror.
2. Go-specific hiring survey (does not exist in corpus — search again in 12 months).
3. Academic study on portfolio signal effectiveness (hunted, not found — retry queries: "portfolio signal labor market developers", "side project resume callback experiment").
