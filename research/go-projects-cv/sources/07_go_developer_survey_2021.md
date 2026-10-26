# 07 — Go Developer Survey 2021 Results (official Go team blog)
- URL: https://go.dev/blog/survey2021-results
- Accessed: 2026-10-26
- Published: 2022-04-19 (Alice Merrick, The Go Blog)
- Source type: primary
- Credibility: 5 — official Go team blog reporting the largest Go Developer Survey to date (11,840 responses), with an explicit methodological note about random sampling to counter self-selection bias.
- Recency: 3 — data is from late 2021; the "areas to invest in best practice docs" findings have been re-confirmed in later surveys, but generics/modules pain points predate Go 1.18/1.20 workspaces.
- Bias: 4 — run by the Go team with an interest in a healthy ecosystem, but it reports respondent verbatims and gaps (e.g., where Go docs are weak) candidly.

## Verbatim quotes

> "In 2021, we ran the Go Developer Survey from Oct 26th to Nov 16th and had 11,840 responses—the largest turnout so far in the 6 years we've been running the survey!" — Opening

> "The vast majority of respondents (88%) agree that they regularly reach a high level of productivity and 85% agree they're often able to achieve a flow state when writing in Go. The proportion of agreement increases as experience with Go increases." — Learning Go section

> "Half of respondents wanted more guidance on best practices on performance optimization and project directory structure. Unsurprisingly, new Gophers (using Go for less than 1 year) need more guidance than more experienced Gophers, though the top areas were consistent across both groups. Notably, new Gophers asked for more guidance in concurrency than more experienced Gophers." — "In which areas should we invest in best practice docs?" section

> "About half of respondents learned a new language at work, but almost as many (45%) learn outside of school or work. Respondents most often (90%) reported learning alone." — "How do developers learn a new language?" section

> "API/RPC services was by far the most common use, but surprisingly, data processing was the second most common intended use case." — A closer look at challenges to Go adoption

> "API/RPC services and CLI apps are most common" — chart caption on the "uses for Go" figure

> "Many of the top resources highlight the importance of good documentation, but live instruction stands out as a particularly useful resource for language learning as well." — "How do developers learn a new language?" section

## Relevance

- Bears on hypotheses: H1 (hygiene > domain), H2 (systems/wheel projects signal mastery), H4 (level-dependent shape)
- Strong H4 evidence: the Go team's own data says new Gophers (<1yr) disproportionately ask for *concurrency* guidance, while all levels ask for *project directory structure* and *performance optimization*. That maps to level-dependent project shape — a beginner's project should be a vehicle for concurrency + layout discipline (a worker-pool/queue/proxy), not a bet-the-company distributed system.
- Indirect H1 support: the top "best practice" gaps (layout, performance, concurrency) are precisely the hygiene dimensions a CV reviewer can probe in a small repo; the actual application domain (todo vs. metrics pipeline) is not what Go devs report struggling with or judging.
- For H2, the survey shows where real Go work lives (API/RPC services, CLI apps, cloud/Kubernetes deployment) — a learner's wheel-project that reproduces an API/RPC or infra primitive (Redis, queue, proxy, container) is congruent with how the language is actually used at work, which 76% of respondents do.
