# 08 — Launch HN: CodeCrafters (YC S22) — Practice writing complex software (discussion)
- URL: https://news.ycombinator.com/item?id=32342334
- Accessed: 2026-10-26
- Published: 2022-08-04
- Source type: discussion
- Credibility: 4 — Hacker News front-page Launch thread (403 points, 206 comments); the founder's post is first-party but the comment body is where the community signal is. Note: CodeCrafters has been accused of astroturfing on HN (see item 38236285), so treat marketing claims skeptically.
- Recency: 3 — 2022 thread; the "build your own real tool" pedagogy it describes has only grown since.
- Bias: 3 — the OP is a founder selling courses; the commenters are independent, with a mix of enthusiasts and skeptics.

## Verbatim quotes

> "We make interactive courses for software engineers, where you get to recreate popular developer tools from scratch. Build your own Redis, Git, Docker, and SQLite—in Go, Python, Rust, etc." — founder post (rohitpaulk / Paul Kuruvilla), opening

> "The projects you'll build are always end to end compatible with the official spec. Given the same input, your program would behave the same way the official one would." — founder post, describing what makes the projects verifiable

> "First, we cater to people with programming experience. There are tons of introductory 'learn to code' resources out there, but surprisingly little once you get past the basics. Good programmers want to get better and to develop in areas where they're not strong yet, and that's what we help with." — founder post, positioning

> "Second, the coursework involves writing actual code instead of consuming videos. You handle concurrency, develop statecharts, traverse B-trees, etc." — founder post, on what skills the projects exercise

> "I think the most reliable way to understand a system is to directly implement the internals of a library. In particular, hands-on experience with networks and file systems is incredibly helpful when writing high-level code." — commenter fredisbusy, on why rebuild-from-scratch projects teach

> "Highly recommend writing a BitTorrent client. The spec is easy to grok, it has a bunch of fun subproblems that you can go as deep or as shallow as you want into, and it's super rewarding being able to download something like the Debian kernel after all of your hard work." — commenter sanufar (on the companion project-ideas thread; same pedagogy)

## Relevance

- Bears on hypotheses: H2 (systems/wheel projects signal mastery), H1 (hygiene > domain), H4 (level-dependent shape)
- H2 evidence: the ecosystem's most visible Go-learning product is built entirely on wheel-projects — Redis, Git, Docker (container runtime), SQLite — and the pitch is explicitly that these exercise *concurrency, statecharts, B-trees*, i.e. the internals Gophers respect. Compatibility with the official spec is the community-accepted proxy for "you actually built it," which is also an anti-fake-it hygiene signal.
- H4: the founder's own framing — "good programmers want to get better and to develop in areas where they're not strong yet" — says the project choice should target a *skill gap*, which varies by level, not a fixed project list. A beginner's gap is concurrency + TCP; an experienced dev's gap may be B-tree storage or consensus.
- Caution for synthesis: this is a commercial source; the pedagogy is echoed by independent commenters (fredisbusy, sanufar), but the "CodeCrafters on your CV" value claim is marketing, not hiring-manager testimony.
