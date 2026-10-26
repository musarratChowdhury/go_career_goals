# 10 — build-your-own-x (CodeCrafters, curated GitHub list) — "Master programming by recreating your favorite technologies from scratch"
- URL: https://github.com/codecrafters-io/build-your-own-x
- Accessed: 2026-10-26
- Published: continuously updated (616 commits; README as fetched 2026-10-26)
- Source type: discussion (community-curated GitHub awesome-list; ~556k stars, 52k forks)
- Credibility: 4 — the single most-starred "build from scratch" curriculum on GitHub, curated by the same team that runs CodeCrafters; a genuine community norm statement rather than SEO listicle spam, though it does link to CodeCrafters products.
- Recency: 5 — actively maintained; includes 2024+ entries (LLMs-from-scratch, Build Deep Learning From Scratch).
- Bias: 3 — curated by a company that monetizes these challenges, but the list is mostly third-party tutorials and the curation judgment is transparent.

## Verbatim quotes

> "Master programming by recreating your favorite technologies from scratch." — repository tagline (About section)

> "This repository is a compilation of well-written, step-by-step guides for re-creating our favorite technologies from scratch." — README intro

> "What I cannot create, I do not understand — Richard Feynman." — README epigraph

> "It's a great way to learn." — README, one-line evaluation of the approach

> "Build your own `Database` — **Go**: *Build Your Own Database from Scratch: From B+Tree To SQL in 3000 Lines* … **Go**: *Code a database in 45 steps: a series of test-driven small coding puzzles* … **Go**: *Build Your Own Redis from Scratch*" — Database section, Go entries (verbatim list entries)

> "Build your own `Docker` — **Go**: *Build Your Own Container Using Less than 100 Lines of Go* … **Go**: *Building a container from scratch in Go*" — Docker section, Go entries (verbatim list entries)

> "Build your own `Command-Line Tool` — **Go**: *Visualize your local git contributions with Go* … **Go**: *Build a command line app with Go: lolcat* … **Go**: *Go CLI tutorial: fortune clone*" — Command-Line Tool section, Go entries (verbatim list entries)

> "Build your own `Web Server` … **Go**: *Let's Create a Simple Load Balancer* … **Go**: *Build A Simple Terminal Emulator In 100 Lines of Golang*" — Web Server / Uncategorized sections, Go entries (verbatim list entries)

## Relevance

- Bears on hypotheses: H2 (systems/wheel projects signal mastery), H1 (hygiene > domain), H4 (level-dependent shape)
- H2: this repo is the community's canonical canon of wheel-projects, and its Go sections concentrate on exactly the "rebuild a real infra primitive" genre — database/Redis, container/Docker, load balancer, terminal emulator, BitTorrent client, shell, regex engine, compiler, neural net. 556k stars is strong revealed preference: Gophers (and programmers generally) treat rebuilding these systems as the archetypal way to learn.
- H1: the curation criterion is *what you build and understand*, not the business domain; every listed project is judged by the internals it exposes (B+trees, event loops, cgroups, RESP protocol), consistent with hygiene/depth over app-domain novelty.
- H4: the list's spread — from a 100-line terminal emulator and lolcat CLI up to B+tree-to-SQL databases and Ray Tracing books — is itself level-graded material; the same "rebuild a real thing" pattern scales from beginner (tiny CLI, shell) to expert (SQLite clone, RAFT), supporting level-dependent project *depth* with a constant project *shape*.
- Note: no evidence found in this channel for how *hiring managers specifically* weigh CodeCrafters-style clones on a CV (the HN threads debate learning value, not resume impact); that claim would need recruiter-side sources from another channel.
