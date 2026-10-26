# F2 — Hygiene beats domain: what reviewers read in a project is engineering process, not cleverness

**Status:** Confirmed · **Confidence:** high
**Sources:** 01 (primary JD), 03 (Atlassian first-party), 04 (n=13,732 survey), 05 (discussion), 06 (Go team primary)

## Thesis
Every hiring-side source that describes *reading* a project reads the same traits: does it run, are there tests, were requirements followed, are tech choices sane, is it documented, is the design defensible [03]. Atlassian explicitly warns against candidates "using some odd or shiny things in order to impress us" [03]. A real Go JD's must-haves are exactly this vocabulary — "automated testing, CI/CD pipelines... reliability, observability" — while the client's business domain is never a requirement [01]. HackerRank: relevant, real-world evaluation is tech leaders' #1 concern [04]. Go's own definition of competence is idiom-conformance (gofmt, naming, error style, defer) — mechanically checkable in any repo regardless of what the app does [06].

## Implication for project choice
Domain novelty (a "unique idea") is not the signal. A small, finished, idiomatic, tested, documented, CI-built, runnable project reads as senior Go craft; a big flashy one that can't be run reads as noise [03: "Yes, people have sent us things that don't work"]. Stdlib-first is itself a Go signal [14, 06].
