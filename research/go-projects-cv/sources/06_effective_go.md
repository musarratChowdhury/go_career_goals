# 06 — Effective Go (official Go team documentation)
- URL: https://go.dev/doc/effective_go
- Accessed: 2026-10-26
- Published: 2009 (written for Go's release; page carries an update note referencing issue 28782, current as of Go 1.26-era site)
- Source type: primary
- Credibility: 5 — official documentation published by the Go project itself; the canonical statement of what "idiomatic Go" means.
- Recency: 3 — written in 2009 and explicitly "not actively updated"; the core idioms it describes (gofmt, naming, error handling, concurrency vocabulary) remain the community's quality bar, but it omits generics/modules.
- Bias: 4 — official self-description of the language, so it flatters Go, but it makes no career/hiring claims and sets concrete, checkable code standards.

## Verbatim quotes

> "**Note:** This document was written for Go's release in 2009 and is not actively updated. While it remains a good guide for using the core language, it does not cover significant changes to the language (generics), ecosystem (modules), or libraries added since." — page header note

> "Go is an open-source programming language that focuses on simplicity, reliability, and efficiency, specifically designed to make it easy to build software at scale." — Introduction

> "A straightforward translation of a C++ or Java program into Go is unlikely to produce a satisfactory result—Java programs are written in Java, not Go. On the other hand, thinking about the problem from a Go perspective could produce a successful but quite different program. In other words, to write Go well, it's important to understand its properties and idioms. It's also important to know the established conventions for programming in Go, such as naming, formatting, program construction, and so on, so that programs you write will be easy for other Go programmers to understand." — Introduction

> "With Go we take an unusual approach and let the machine take care of most formatting issues. The `gofmt` program (also available as `go fmt`, which operates at the package level rather than source file level) reads a Go program and emits the source in a standard style of indentation and vertical alignment" — Formatting section

> "The [Go package sources](https://go.dev/src/) are intended to serve not only as the core library but also as examples of how to use the language. […] If you have a question about how to approach a problem or how something might be implemented, the documentation, code and examples in the library can provide answers, ideas and background." — Examples section

> "For programmers accustomed to block-level resource management from other languages, `defer` may seem peculiar, but its most interesting and powerful applications come precisely from the fact that it's not block-based but function-based." — Functions / Defer section

> "Deferring a call to a function such as `Close` has two advantages. First, it guarantees that you will never forget to close the file, a mistake that's easy to make if you later edit the function to add a new return path. Second, it means that the close sits near the open, which is much clearer than placing it at the end of the function." — Functions / Defer section

> "It's helpful if everyone using the package can use the same name to refer to its contents, which implies that the package name should be good: short, concise, evocative." — Names / Package names section

## Relevance

- Bears on hypotheses: H1 (hygiene > domain), H2 (systems/wheel projects signal mastery), H4 (level-dependent shape)
- The Go project's own definition of competence is *conformance to shared conventions* — gofmt, exported/unexported naming, doc comments, error-return style, defer discipline — not the domain of the app. This is direct primary-source support for H1: a reviewer scanning a Go repo can check hygiene mechanically, which is why a small idiomatic CLI reads as more "Go" than a large non-idiomatic web app.
- It also implies a floor for H2: wheel-projects (Redis clone, HTTP server, load balancer) are exactly where the idioms Effective Go polishes — multiple return values + error, defer for resource cleanup, interfaces named Reader/Writer, concurrency via channels/select — actually get exercised. A CRUD todo app barely touches them.
- For H4, the doc is level-agnostic; it defines a fixed target ("easy for other Go programmers to understand") that beginners and experts are both judged against, so project shape can vary while the hygiene bar stays constant.
