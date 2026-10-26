# F4 — The portfolio is level-dependent: breadth for entry, depth + contributions for mid/senior

**Status:** Confirmed · **Confidence:** high
**Sources:** 01 (primary), 02, 04 (industry), 05, 07 (primary), 09, 15, 19

## Thesis
Published projects are the "notable exception" route for "students or other nontraditional candidates" [02]; repo code-checks are "mostly done for junior-level positions" [05]; senior JDs demand a production track record instead, with no portfolio link requested [01]. Meanwhile entry-level hiring is structurally worse (senior/lead hiring +19–22%, entry ~+7% [04]; 38% of firms cut entry-level hiring [19]) — so juniors must prove more with less attention.

## Learning-side convergence on progression
Curricula agree on an order: concept drills first (Exercism's 35-concept dependency tree [11]; Learn Go with Tests: interfaces → errors → DI/mocking → concurrency → sync → context → generics [12]), then guided mini-projects calibrated to difficulty ("challenge you, but won't leave you clueless" [13]; "20–40 hours... deliberately get stuck" [15]), then one substantial capstone — a production net/http app [14] or a concurrent system [12, 13] — then extending existing code rather than starting new toys [13, 14]. New Gophers' biggest gap is concurrency; all levels' gap is project layout [07] — early projects should be vehicles for exactly those two skills.

## Implication
Entry-level: 3–4 finished projects spanning CLI + HTTP API + concurrent system (breadth proof). Mid/senior: one deep systems project + merged PRs in multi-contributor codebases — "It's contributions to projects with other contributors that really matter" [05]; "This person shipped a specified change and survived review" [18].
