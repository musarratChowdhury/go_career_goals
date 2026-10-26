# F3 — Wheel-projects are the community canon: rebuild a real system, spec-compatible, small and finished

**Status:** Confirmed for learning value; inferred (not directly evidenced) for CV value · **Confidence:** high / moderate
**Sources:** 06, 07 (primary), 08, 09, 10 (discussion), 12, 13, 14 (educational)

## Thesis
The Go community's canonical way to gain mastery is rebuilding real infra primitives in Go: database/Redis, container, load balancer, BitTorrent client, shell, Git — the 556k-star build-your-own-x canon [10], the basis of a YC company (CodeCrafters: "Build your own Redis, Git, Docker, and SQLite—in Go" [08]), and the projects HN threads praise [09]. The community rationale: "the most reliable way to understand a system is to directly implement the internals" [08, 09]. These projects force exactly the idioms Effective Go polishes — channels/select, defer, multi-return errors, Reader/Writer interfaces [06] — and match where Go is actually used (API/RPC, CLI, data processing per the Go team survey [07]).

## Two constraints the community attaches
1. **Finished beats impressive:** "something intentionally small and complete... clarity, constraints, and finishing the whole arc, not scale" [09]. Rough effort bands: Redis clone 20–40h, Git 20–40h, Kafka-lite 30–60h, RAFT 40–80h, SQLite 60–120h [09, AI-assisted estimate — treat as rough].
2. **Verifiable behavior is the anti-fraud marker:** "Given the same input, your program would behave the same way the official one would" [08] — spec-compatibility turns a self-description claim into a checkable one.

## Evidence gap
No hiring-manager source in the corpus specifically evaluates CodeCrafters-style clones on a CV ([10] digest, Channel B). The CV value of a wheel-project rests on F2 (hygiene + depth of narration in interviews), not on direct reviewer testimony.
