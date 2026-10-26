# 14 — Let's Go (Alex Edwards) — book teaching Go via start-to-finish build of one production web app
- URL: https://lets-go.alexedwards.net/
- Accessed: 2026-10-26
- Published: last updated August 26th, 2026; version 2.27.0, written for Go 1.27, 416 pages
- Source type: educational
- Credibility: 4 — the best-known project-based Go web book, used for team onboarding at companies named on the page (Atlassian, Walmart, ESL; testimonial from Bitrise engineering manager); independently reviewed on Goodreads/Reddit. It is a commercial product.
- Recency: 5 — explicitly updated for Go 1.27, August 2026.
- Bias: 3 — vendor page selling a $34.95-$59.95 book; testimonials are curated, though publication metadata and syllabus are factual.

## Verbatim quotes
> "Let's Go is a clear, concise and easy-to-follow guide to web development with Go. It packs in everything you need to know about best practices, project structure and practical code patterns — without skimping on important details and explanations." — hero section
> "Go is a great language for building web applications. But teaching yourself from blog posts and the standard library documentation can be a big time-sink and leave you with more questions than answers." — problem statement
> "You might be wondering things like: Where can I see a concrete example of a real-world web application? How is it best to structure and organize my code? How do I manage and version control dependencies? And how do I effectively test my web application?" — problem statement
> "The book walks through the start-to-finish build of a complete working application, helping you to *learn by doing*. You'll get practical experience implementing common real-life code patterns, the topics that you're learning about are put in context, and you'll end up with a well-structured codebase that you can adapt for your own future work." — hero section
> "Logging and error handling — How to implement leveled logging and centralized error handling." — "What You'll Learn" item 5 (of a 17-item list that includes: starting a server/handlers/routing/static files; idiomatic project structure; Go modules; command-line flags and dependency injection; SQL databases & connection pools; HTML templating; middleware; form validation; sessions; HTTPS; embedding files; preventing SQL injection/CSRF/XSS/clickjacking/slow-client attacks; authentication & authorization; request context; unit/integration/e2e tests with mocks and coverage)
> "Does the book use a framework or the standard library? Let's Go teaches you to build web applications using the Go standard library (rather than a specific framework like Buffalo, Echo or Gin). A few small external packages are used where it makes sense for security reasons and to reduce complexity." — FAQ
> "Is this suitable for Go beginners? Yep! The book deliberately takes a 'learn as you code' approach, starting slowly with the basics of building a web application and gradually adding additional features and functionality. So long as you have a basic understanding of the Go syntax, you shouldn't have trouble following along" — FAQ
> "In the *Professional Package*, at the end of the book there are 6 exercises which extend the application build. Each exercise is broken down into high-level steps for you to work through, and there are suggested answers for each step." — FAQ (guided exercises)
> "You'll get practical experience implementing common real-life code patterns... you'll end up with a well-structured codebase that you can adapt for your own future work." — hero section

## Relevance
- Bears on: learning axis + H2 (a single large net/http + database/sql project — not many small ones — as the vehicle for stdlib depth: context, middleware, sessions, security, testing) and H4 (ordered chapter progression inside one growing application: server → structure → modules → config/DI → logging & error handling → SQL → templates → middleware → forms → sessions → HTTPS → embedding → security → auth → context → testing).
- Key pedagogical claim: one start-to-finish production-grade build, "learn as you code", stdlib-only (frameworks explicitly rejected) — the argument that depth of one real app beats breadth of toy apps for learning professional Go.
- Explicit order: features are added cumulatively to the same codebase, and the book ends with 6 guided exercises that *extend* the built application — i.e., the recommended next step after finishing is modifying/extending a real app, not starting a new toy.
