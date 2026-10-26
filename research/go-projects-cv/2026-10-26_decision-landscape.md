# Which Go Projects to Build — Learning Value × CV Signal

**Date:** 2026-10-26 · **Genre:** decision-landscape · **Depth:** medium
**Corpus:** 20 sources (primary 5, industry 9, discussion 4, educational 3 — one source carries two types) · `sources.csv` + `sources/NN_*.md` for verbatim grounding.

---

## Executive answer (read this if nothing else)

Build a **short list of small, finished, production-shaped, verifiable Go projects** — and package them so a reviewer can verify each claim in one click. Concretely, in order:

1. **A concurrent system** (worker pool / job queue / rate limiter / web crawler) — goroutines, channels, `context`, race detector. This targets new Gophers' #1 documented gap: concurrency [07].
2. **A production-shaped HTTP API using only `net/http`** — config, structured logging, graceful shutdown, SQL + migrations, middleware, tests, Dockerfile, CI. This targets gap #2: project layout [07], and it mirrors how Go is actually used (API/RPC is the #1 use case [07]) while reading as JD-vocabulary craft [01].
3. **A CLI tool you actually use** — flags, `io`, exit codes, shell completion. Breadth proof; CLI is a top-3 Go use case [07].
4. **One "build-your-own" systems project, spec-compatible, ~20–40h:** Redis clone first (or a BitTorrent client, load balancer, or message queue). Reserve SQLite/B+tree DB (60–120h) or RAFT (40–80h) for later [09, 10]. Spec-compatibility is what makes the claim checkable [08].
5. **From mid-level on: stop adding solo repos.** Contribute to a multi-contributor Go OSS project — merged PRs surviving someone else's review are the artifact reviewers actually reward [05, 18].

**Packaging decides most of the outcome** (see "Rules" below): finish small [09], link one-click-deep [02, 05], ship tests + README + CI [03, 06], and be able to narrate every line [18]. Do **not** expect projects alone to carry the job search — referrals produce 30–50% of hires [20]; projects are what you bring *to* the conversations a referral gets you, plus take-home/interview ammunition.

---

## Hypothesis verdicts

| # | Hypothesis | Verdict | Evidence |
|---|-----------|---------|----------|
| H1 | Hygiene signals beat domain novelty | **Confirmed** (high confidence) | [01, 03, 04, 05, 06] — 3 source types, converging: "odd or shiny things" actively annoy [03]; JDs demand process vocabulary, not domain [01] |
| H2 | Systems/wheel projects signal mastery better than CRUD clones | **Confirmed** for learning; **inferred** for CV | [06, 07, 08, 09, 10, 12, 13] — canon is unambiguous; no hiring-manager source explicitly grades a Redis clone (gap flagged) |
| H3 | Verifiability matters — reviewers open repos | **Confirmed in qualified form** (moderate-high) | "Almost never" is directionally right [17, 20, 16] but "never" is wrong: top-of-funnel scan + deep-dive [02], #1 stated non-interview signal [19], code-checks for juniors [05] |
| H4 | Portfolio shape should be level-dependent | **Confirmed** (high confidence) | [01, 02, 04, 05, 19] hiring side + [07, 11, 12, 13, 15] curriculum side, independently converging |

---

## What the hiring side actually does (F1, F2, F4)

**Nobody lives on your profile.** 83% of GitHub users have zero commits in a year; Dan Luu — top-1K-followed — got his code examined in 2 of 50 interviews [17]. ATS filters kill ~75% of cold resumes pre-human, and referrals (5–7% of applicants) produce 30–50% of hires [20]. A 2026 talent-vendor essay steel-mans the case that GitHub "creates visual activity" without evidence [16] — but note its commercial motive (it sells the replacement funnel; Bias score 2).

**But "never" is too strong.** The Holloway hiring guide (45+ contributor reference [02]) puts code output at the top of the funnel with a later deep-dive on "one or two projects." A Dec-2025 survey of 200+ engineering leaders (n>200, CodePath/Fortune [19]) ranks side projects/portfolios the **#1 non-interview signal (38%)**, above degrees (23%). Practitioners on HN: "we specifically asked for Github links and we checked the code... mostly for junior-level positions" [05].

**When they look, they read process, not plot.** Atlassian's take-home checklist [03]: Does it run? Tests? Requirements followed? Sane tech? Good design decisions? Explicit red flag: "odd or shiny things in order to impress us." A Grafana co-founder's 2026 description of reviewer click-paths [18]: green squares skipped, stars skipped — what's read is **merged PRs that survived someone else's review**, with red flags for oversized diffs, months-open PRs, and unnarratable merges. A live senior-Go JD [01] asks for "automated testing, CI/CD pipelines... reliability, observability" — and for no GitHub link at all.

**Synthesis:** the CV project's job is to (a) survive a 30-second skim — which means hygiene-visible from the outside (README, tests dir, CI badge, gofmt), and (b) be deep enough to carry a 30-minute interview walkthrough. Junior candidates get looked at more; seniors are presumed and judged on PR history instead.

## What the learning side converges on (F3, F4)

Four independent curricula — Exercism's 35-concept dependency tree [11], Learn Go with Tests [12], Gophercises [13], Let's Go [14] — plus community consensus [09, 10] agree on the same progression:

1. **Concept drills with tests** first (the "scales practice" layer — "you're unlikely to use goroutines to solve a kata" [12]).
2. **Guided mini-projects** calibrated so you struggle but aren't clueless [13], ~20–40h each [15].
3. **One substantial capstone**: a production net/http app (Let's Go's stdlib-only full build [14]) or a concurrent system (crawler/worker-pool/queue) [12, 13].
4. **Extend existing code** — Gophercises exercises chain (sitemap reuses the link parser [13]); Let's Go ends with 6 exercises extending the built app [14]. In OSS terms: this is the bridge to step 5 of the executive answer.
5. **Depth projects when ready**: rebuild real infra primitives [10, 08], sized honestly [09].

New Gophers report wanting more *concurrency* guidance than experienced Gophers, and everyone wants *project layout* guidance [07] — so every early project should double as a concurrency + layout lesson.

## The recommended portfolio (decision by target level)

**Entry-level / Go-switcher (the "breadth" portfolio, ~4 repos):**
| Project | Skills proven | Effort |
|---|---|---|
| Concurrent worker pool / job queue / crawler | goroutines, channels, `context`, race detector, backpressure | 20–40h |
| Production-shaped `net/http` API (stdlib) | routing, middleware, SQL, config, logging, graceful shutdown, e2e tests, Dockerfile, CI | 30–50h |
| CLI tool you use daily | `flag`/`os/exec`, `io`, packaging, releases | 15–30h |
| Redis-compatible server or BitTorrent client | TCP, protocols, persistence, spec-compatibility | 20–40h |

**Mid-level (the "depth" portfolio):** replace breadth items 1–3 with **one** 60–120h systems project (B+tree/SQLite-lite, or a Kafka-like broker [09]) *plus* 2–5 merged PRs in active multi-contributor Go OSS repos [05, 18] — the PRs now outweigh the solo project.

**Senior:** don't build for the CV at all — your signal is the production track record [01]. Build only what you'd maintain, and make any public work narratable [18].

## Packaging rules (the part everyone skips — and the part the evidence most supports)

1. **One-click verify.** Pin the 2–3 best repos; link the exact file/PR, not the profile [02, 05].
2. **Small and complete beats big and abandoned** [09]. Three finished repos > ten half-built.
3. **Runnable == honest.** "Yes, people have sent us things that don't work" [03]. One-command `make run` / Docker compose; README with screenshots/GIF + architecture note.
4. **Tests + CI + gofmt, visibly** [03, 06, 01]. This is F2 — the 30-second skim reads process.
5. **Stdlib-first** [14, 06]. Reaching for a framework hides the Go signal; effective-use of `net/http`, `database/sql`, `context` *is* the signal. Also dodges the "shiny things" red flag [03].
6. **Spec-compatibility for wheel-projects** [08]: "passes the official Redis test suite" is checkable; "a fast key-value store" is marketing.
7. **Narrate everything public** [18]: "the worst merge is still public." Every public PR you can defend in an interview; no typo-spray.
8. **Commit history tells a story** — incremental, referenced issues, honest messages. Green-square padding is a known fake [05, 16].
9. **AI-era caveat:** with AI-generated repos flooding the pool [16], reviewers increasingly probe *understanding*. Only build what you can explain line-by-line; "Don't have ChatGPT write your code for you! You won't learn that way" [15] — and expect the interview to probe your repo's trade-offs.
10. **Projects are one funnel input, not the funnel** [20, 19]: spend comparable time on referrals/community; bring the projects *into* the conversations.

## Adversarial pass (steel-manned counter-arguments)

1. **"This whole answer is wrong — projects don't move CV callbacks at all."** Best version of the case: [17]'s interview audits (2/50), [20]'s funnel arithmetic, [16]'s noisy-signal argument. Resolution: for *cold* applications, plausibly true; the portfolio's demonstrated value is in take-homes, interview walkthroughs, junior-level scrutiny [05], and the top-of-funnel scan [02] — and it's the best substitute for experience you don't have yet [02, 19].
2. **"The portfolio arms race is now unwinnable."** With AI flooding GitHub, visible activity is worth less every quarter [16, 19 AI-fluency expectation]. Counter-counter: that inflates the value of *verifiable depth* — spec-compatible builds [08], narration ability [18], and finished-ness [09], none of which scale with generation cost.
3. **"Referrals dominate; build the network, not the repo."** Statistically solid [20] — but it's not either/or: a referral gets you the read; the project is what survives the read [02, 03]. The report's step-10 rule addresses this directly.
4. **"Wheel-projects are résumé-driven development cosplay."** The corpus contains no hiring-manager testimony that a Redis clone specifically impresses (explicit gap, [10], F3). Honest position: it's the community's proven *learning* vehicle [08, 09, 10] that *indirectly* earns CV credit via the hygiene + narration channel [03, 18].

## Limitations & evidence gaps

- **No causal data anywhere:** nothing measures callback lift attributable to a portfolio link. All hiring evidence is stated-preference surveys, vendor guides, forum testimony, or one 2018 platform analysis.
- **Not Go-specific:** only [01] is a real Go JD. Hiring-side findings are general-backend; Go-specificity comes from the learning side and [07].
- **Recency spread:** strongest disconfirming data is 2018 [17]; strongest confirming is Dec 2025 [19]; Atlassian's process piece is 2016/17 [03].
- **Unfetchable sources:** Reddit (403 across all channels) — r/golang consensus is inferred from HN + official sources instead; noted per-channel.

## Refresh triggers → `refresh_targets.md`

See `refresh_targets.md` for the watch-list (HackerRank 2026 report, Go Developer Survey 2026, new hiring-side repo-read studies, CodeCrafters pricing/positioning changes).

---

**Index:** findings → `findings/F1_verifiability-funnel.md`, `F2_hygiene-over-domain.md`, `F3_wheel-projects-canon.md`, `F4_level-dependent-portfolio.md`. Sources → `sources.csv`, `sources/01–20`. Plan → `plan.md`.
