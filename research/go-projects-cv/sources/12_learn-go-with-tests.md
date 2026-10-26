# 12 — Learn Go with Tests (Chris Quinn / quii) — free book, TDD-first Go curriculum
- URL: https://quii.gitbook.io/learn-go-with-tests (chapter index fetched: https://quii.gitbook.io/learn-go-with-tests/llms.txt)
- Accessed: 2026-10-26
- Published: unknown (continuously updated; 11 official translations listed on the landing page)
- Source type: educational
- Credibility: 4 — de-facto standard free Go+TDD resource, widely referenced in the Go community, MIT-licensed, actively maintained (includes modern chapters on generics and testing/synctest); single-author.
- Recency: 5 — index includes Generics, "Revisiting time, with testing/synctest", WebSockets chapters (post-Go-1.24 material).
- Bias: 5 — free, MIT-licensed, no product to sell (only optional donate links).

## Verbatim quotes
> "Explore the Go language by writing tests" — landing page, "Learn test-driven development with Go"
> "Get a grounding with TDD. Go is a good language for learning TDD because it is a simple language to learn and testing is built-in" — landing page
> "Be confident that you'll be able to start writing robust, well-tested systems in Go" — landing page
> "Katas are fun but they are usually limited in their scope for learning a language; you're unlikely to use goroutines to solve a kata." — Background section, "What didn't work"
> "This ends up making the learning feel quite *unstructured* and *ad hoc*." — Background section (on ad-hoc team learning)
> "By far the most effective way was by slowly introducing the fundamentals of the language by reading through [go by example](https://gobyexample.com/), exploring them with examples and discussing them as a group." — Background section, "What did work"
> "This to me seems analogous to practicing scales when trying to learn guitar. It doesn't matter how artistic you think you are, you are unlikely to write good music without understanding the fundamentals and practicing the mechanics." — Background section
> "Learning the fundamentals by writing small tests so that you can then take your existing software design skills and ship some great systems." — "What works for me"
(Chapter-order quotes from the llms.txt index, verbatim titles in order: "Hello, World", "Integers", "Iteration", "Arrays and slices", "Structs, methods & interfaces", "Pointers & errors", "Maps", "Dependency Injection", "Mocking", "Concurrency", "Select", "Reflection", "Sync", "Context", "Intro to property based tests", "Reading files", "Templating", "Generics", then "HTTP server", "JSON, routing and embedding", "IO and sorting", "Command line & package structure", "Time", "WebSockets")

## Relevance
- Bears on: learning axis + H4 (one of the few sources with a fully explicit, chapter-level ORDER covering exactly the target skills: interfaces → pointers/errors → DI/mocking → concurrency → select → sync → context → generics → net/http application) and H2 (the "build an application" section — HTTP server, JSON/routing/embedding, CLI, WebSockets — shows how systems projects pull in stdlib depth).
- Explicit pedagogical stance: katas/small-tests are the "scales practice" layer that must come first, and structured test-driven micro-chapters beat ad-hoc tutorials; the author's own evidence section documents that unstructured team learning "feel quite unstructured and ad hoc".
- Progression it recommends: (1) go-by-example style fundamentals, (2) test-driven concept chapters (functions, slices, interfaces, pointers+errors, DI, mocking, concurrency, select, sync, context, reflection, generics), (3) testing-fundamentals (acceptance tests, working without mocks), (4) "build an application" capstone: HTTP server → JSON/routing/embedding → IO/sorting → CLI & package structure → time → WebSockets.
