# 13 — Gophercises (Jon Calhoun) — ~20 mini-projects with per-exercise topic mappings
- URL: https://gophercises.com/
- Accessed: 2026-10-26
- Published: unknown (course launched 2017; site still live with all 20 exercises; author bio notes prior Google SWE + founder of EasyPost)
- Source type: educational
- Credibility: 4 — curated free course by a recognized Go educator (Jon Calhoun, guest on Go Time, speaker at GothamGo 2018); every exercise lists explicit Go topics and duration; exercises have public source repos.
- Recency: 2 — content largely from 2017-2019 era (pre-generics, some archived deps), though the pedagogy and topic mappings remain valid.
- Bias: 4 — free course but functions as marketing for the author's paid courses (Web Development with Go); topic mappings themselves are not exaggerated.

## Verbatim quotes
> "You are just starting to pick up a new programming language (like Go!) and things are going great. The tutorials are clicking and you are making great progress... and then you run out of tutorials." — intro section
> "'What should I build next?' you ask, and inevitably everyone tells you to 'Pick a side project and work on it!' Great, but what side project should you work on? What project will provide you with the best learning experience? What happens if you pick something too challenging and get stuck?" — intro section
> "You need to find projects that will challenge you, but won't leave you clueless about how to proceed." — intro section
> "In the course we will build roughly 20 different mini-applications, packages, and tools that are each designed to teach you something different." — intro section
> "In the course we will learn about and practice using: Channels, Mutexes, Goroutines, Functional Options, Chaining Interfaces, Various parts of the standard library (io, time, and many other packages), Reading input from the command line" — intro section, topic list
> "By completing the exercises in Gophercises you will slowly become more confident using the Go programming language. You will start to learn how to read the standard docs and make sense of them. You will even start to learn how to evaluate the difficulty of a project before doing much coding." — intro section
> "Exercise 13 — Quiet HN: Given an existing web application that displays stories from Hacker News, we will look at ways to add concurrency and caching to the application while looking for race conditions and other potential issues. Topics: concurrency channels caching race flag" — exercise 13 listing
> "Exercise 11 — Blackjack AI: Refactor the blackjack exercise into a package with an exported AI anyone can implement to create a bot that plays blackjack in a simulated game. Topics: interfaces simulation bot" — exercise 11 listing
> "Exercise 14 — Recover Middleware: Build HTTP middleware that will recover from any panics in an application, even if the response write has been partially written to, and then output the stack trace if the application is in development mode. Topics: panic recover defer middleware stack traces" — exercise 14 listing
> "Exercise 2 — URL Shortener: Code an http.Handler that forwards paths to other URLs (similar to Bitly). Topics: YAML middleware maps http-handlers" — exercise 2 listing

## Relevance
- Bears on: learning axis + H2 (systems/CLI/web project types each tagged with the exact Go concepts they teach — the clearest concept→project-type mapping found) and H4 (implied progression: quiz CLI w/ goroutines+channels → URL shortener (net/http handler, middleware) → HTML parser package (io readers) → sitemap builder (reuses ex.4 package) → task manager (BoltDB) → deck-of-cards package (functional options, go generate) → blackjack → blackjack AI (interfaces) → Quiet HN (concurrency, caching, race conditions) → recover middleware (panic/recover/defer) → secrets API (crypto, interface chaining) → image/PDF services).
- Explicit project-progressions recommended: exercises build on each other (ex.5 reuses ex.4's link parser; exs. 10-11 extend ex.9's deck package; ex.15 extends ex.14) — teaching incremental extension of an existing codebase, not just greenfield.
- Also the source that most explicitly frames the pedagogical problem this investigation cares about: choosing projects calibrated to difficulty so learners don't get stuck, and using mini-projects specifically to learn to read Go stdlib docs.
