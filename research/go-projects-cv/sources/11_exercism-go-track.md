# 11 — Exercism Go Track (167 exercises, 35 concepts) + Syllabus design docs
- URL: https://exercism.org/tracks/go (supplementary page fetched: https://exercism.org/docs/building/tracks/syllabus)
- Accessed: 2026-10-26
- Published: unknown (site © 2026; track has 167,720 students and 1,358 contributors as of access)
- Source type: primary
- Credibility: 5 — Exercism is a UK not-for-profit and self-declared "official GoBridge & GDN mentoring platform"; its syllabus docs are the canonical statement of how the Go concept curriculum is ordered.
- Recency: 5 — page shows © 2026 and live student/contributor counts.
- Bias: 5 — non-profit learning platform with no course to upsell besides optional Insiders; exercises and mentoring are free.

## Verbatim quotes
> "Join Exercism's Go Track for access to 167 exercises grouped into 35 Go Concepts, with automatic analysis of your code and personal mentoring, all 100% free." — track page, hero section
> "Get better at programming through fun, rewarding coding exercises that test your understanding of concepts with Exercism." — track page, "About Go" section
> "The Go track on Exercism has 35 concepts and 167 exercises to help you write better code." — track page, "Community-sourced Go exercises"
> "Our mentors will help you learn to think like a Go developer and how to write idiomatic code in Go. Once you've solved an exercise, submit it to our volunteer team, and they'll give you hints, ideas, and feedback on how to make it feel more like what you'd normally see in Go" — track page, "Get mentored the Go way"
> "A fully featured Exercism track has two types of exercises: Concept Exercises and Practice Exercises. They are fundamentally different and complement each other well." — syllabus docs page
> "Each individual Concept Exercise is very tightly focused. It is a small and highly-targeted step that moves the student towards understanding something about the language. It builds only on concepts that have been introduced previously." — syllabus docs page
> "By allowing non-idiomatic code in the earliest exercises, students are able to take many smaller steps in familiar territory rather than a few big steps in unfamiliar territory. The result is that they are able to reach the stage of idiomatic code more quickly and with less friction." — syllabus docs page
> "Exercises are structured as a tree with an introductory exercise at the top as the starting point. Later exercises teach concepts that depend on having understood concepts that are taught earlier." — syllabus docs page
> "A good Concept Exercise is extremely focused, and ideally teaches only one concept... This is in contrast to Practice Exercises, which are open ended and lend themselves to exploration." — syllabus docs page
> "For example, in Go there are no enums. Instead the Go concept tree introduces constants, and teaches how to use constants in the type of situation where you might use enums in other languages." — syllabus docs page (shows the syllabus is Go-specific, not a port)

## Relevance
- Bears on: learning axis + H4 (explicit concept-dependency ordering: a *tree* of concepts, each exercise building only on prior concepts) and H2 (practice exercises like POV, Grep, Markdown parser force stdlib depth at scale — 167 exercises).
- Exercism's Go curriculum separates *concept* exercises (one concept each, tightly ordered, tree-structured) from *practice* exercises (open-ended exploration); the platform explicitly optimizes for "comfortable reading and writing idiomatic code", with human mentoring as the idiom-correction mechanism.
- No project progression per se — this is drill-and-concept granularity (Hello World → basics → ... → concurrency/generics concepts), positioned in the ecosystem as the fundamentals layer *before* portfolio projects; the Go track is also the official GoBridge/GDN mentoring platform, so it carries ecosystem endorsement.
