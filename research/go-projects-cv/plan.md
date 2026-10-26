# Plan — Which Go projects to build (learning + CV signal)?

**Date:** 2026-10-26
**Genre:** decision-landscape (hybrid) — compare candidate projects on two axes: learning value (Go mastery) and CV signal value (recruiter/hiring-manager response).
**Depth:** medium — capability discovery, verification pass, refresh targets required.
**Status:** COMPLETE (2026-10-26) — 20 sources, 4 findings, report emitted; see `2026-10-26_decision-landscape.md`.

---

## 1. Reframe

**Question as asked:** "Which Go projects should I build to learn Go AND impress CV reviewers?"

**The real decision:** With finite build time (roughly 2–6 projects over weeks/months), which Go projects maximize *dual* ROI — (a) deep, transferable Go skill acquisition, and (b) CV/interview-call signal when a recruiter, hiring manager, or technical reviewer inspects the candidate — so the portfolio converts into interviews for Go backend roles?

Hidden sub-decisions the research must address:
- What do CV reviewers *actually* do with project links (do they click? do they read code? do they run it?)?
- Which project *types* signal Go-specific mastery vs. generic programming ability?
- How much do engineering-hygiene signals (tests, CI, README, Docker) matter vs. project domain?
- Does the answer differ by target level (entry vs. mid vs. senior)?

## 2. Falsifiable hypotheses

- **H1 — Hygiene over domain:** Production-grade engineering signals (tests, CI, Docker, README, benchmarks, clean history) discriminate more in CV review than the project's domain or originality.
- **H2 — Systems clones signal mastery:** "Build-the-wheel" systems projects (HTTP server, message queue, KV store, rate limiter, container/runtime lite) signal Go mastery better than app-level CRUD clones, because they force concurrency, interfaces, and `net/http`/stdlib depth.
- **H3 — Verifiability effect:** Public, deployed, verifiable artifacts (public repo with real history, live demo, real users/contributors/PRs) beat local-only repos because reviewers can check them — *or* reviewers never click at all (refutation path).
- **H4 — Level-dependent shape:** The optimal portfolio is breadth-first for entry-level (CLI + web API + DB + worker) and depth-first for mid/senior (one substantial systems/distributed project with scale evidence).

Each hypothesis will be marked **confirmed / refuted / under-determined** at synthesis, per evidence.

## 3. Sourcing strategy (channel → subtopic → hypothesis)

| Channel A (sub-agent) | Type | Subtopics | Hypotheses |
|---|---|---|---|
| A. Hiring side — recruiters, engineering managers, hiring guides, Go job postings | industry/professional | what reviewers look at in project sections; do they open repos; JD requirements | H1, H3, H4 |
| B. Go community — r/golang, forum.golang, Go team blogs, awesome lists, experienced Gophers | discussion/community + primary | canonical project advice; what signals Go-specific skill; tutorial-project reputation | H2, H4 |
| C. Learning pedagogy — project-based Go curricula, course authors, "learn Go by building" | educational/practitioner | which projects force which Go concepts; progression order; time-to-skill | learning axis, H2 |
| D. Adversarial/disconfirming — "portfolios don't matter", hiring data, counter-evidence | mixed | does anyone read GitHub; alternative signals; when projects backfire | H3 refute, H1 stress-test |

**Independence rule:** a thesis needs ≥3 sources of ≥2 different types; the ≥3-source/≥3-type triangulation applies to final report theses.

**Opposition queries (mandatory):**
- "portfolio projects hiring managers ignore"
- "does anyone actually look at your GitHub recruiters"
- "todo list project CV red flag"
- "GitHub contributions do not get you hired"
- "Go project ideas outdated tutorial"

**Search rounds:** Round 1 = 4 parallel sub-agents (one per channel). Round 2 (only if gaps) = targeted follow-ups for under-determined hypotheses.

## 4. Risk register

| Risk | Mitigation |
|---|---|
| Corpus is mostly opinion/listicle content, not controlled studies → causal claims unjustified | Frame findings as *expert consensus*, not proven effect sizes; flag evidence strength per thesis |
| SEO-farm listicles dominate "Go project ideas" queries | Score Credibility down; prefer named practitioners, companies, hiring docs, Go team sources |
| Recency: Go 1.22+ routing, 2025–26 hiring market changes | Prefer <24 months where it exists; note when older source is used because claim is time-invariant |
| Confirmation bias — only collecting "projects are great" evidence | Channel D dedicated to disconfirmation; opposition queries in every channel |
| User background assumptions wrong (level, target role) | H4 explicitly covers level-dependent answers; report includes a "if you are X" decision tree |

## 5. Stop criteria

- ≥10 saved sources across ≥3 source types, each with verbatim quotes + Credibility/Recency/Bias scores.
- Every hypothesis marked confirmed / refuted / under-determined with ≥3-source triangulation or explicit "insufficient evidence".
- Adversarial pass run (4 self-critique questions + counter-argument section in report).
- Final report + `findings/` + `sources.csv` + `refresh_targets.md` written.

## 6. Changelog

- 2026-10-26 — plan created; reframed, hypotheses fixed, channels mapped.
- 2026-10-26 — 4 channels executed in parallel (Channel A retried once after transient subagent error). 20 sources saved (01–20), all with verbatim quotes + scores. Two fetch-failures skipped per discipline: Reddit threads (403, all channels), one vendor report (transport error).
- 2026-10-26 — triangulation complete; all 4 hypotheses adjudicated (H1 confirmed, H2 confirmed/inferred split, H3 qualified-confirmed, H4 confirmed); adversarial pass run (4 counter-arguments steel-manned); report + findings + refresh targets emitted.

## 7. Outcome summary

- H1 confirmed (high), H2 confirmed-for-learning (CV value inferred), H3 confirmed-in-qualified-form (moderate-high), H4 confirmed (high).
- Key gaps: no causal callback-lift data anywhere; only one Go-specific JD in corpus; strongest disconfirming data is 2018-vintage; Reddit unfetchable.
- Actionable core: short list of small finished production-shaped projects (concurrency system → stdlib HTTP API → CLI → one spec-compatible wheel-project), packaging rules decisive, OSS PRs from mid-level on, projects as interview-ammo within a referral-heavy funnel.
