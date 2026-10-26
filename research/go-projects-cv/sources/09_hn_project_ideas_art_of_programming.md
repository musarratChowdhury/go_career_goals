# 09 — HN: Project ideas to appreciate the art of programming (discussion)
- URL: https://news.ycombinator.com/item?id=46439027
- Accessed: 2026-10-26
- Published: thread opened ~Jan 2026 (comments "9 months ago" relative to access date; linked article is the CodeCrafters "programming project ideas" post)
- Source type: discussion
- Credibility: 4 — Hacker News thread, 224 points, 79 comments; commenters include working engineers critiquing a project-idea list. Not Go-specific, but the projects discussed (Redis clone, BitTorrent client, Kafka broker, SQLite clone) are the canonical Go wheel-projects.
- Recency: 5 — very recent thread; reflects current (AI-era) thinking about building from scratch.
- Bias: 3 — the linked article is CodeCrafters marketing (commenters call it possible AI slop / astroturf), but the comment discussion is independent and largely skeptical, which makes the consensus remarks more trustworthy.

## Verbatim quotes

> "Build something intentionally small and complete a tiny tool or protocol you can understand end-to-end. The satisfaction comes from clarity, constraints, and finishing the whole arc, not scale." — commenter xthe

> "This is a strange list. #58 is make your own malloc, ok. That's a moderately difficult project for a new developer… Followed by #59 where they suggest you build your own streaming protocol from scratch… There are some good projects in there, but the levels of difficulty are all over the place." — commenter Jtsummers

> "My only critique is that it would help to group projects by difficulty. But AI genned or not, it does have decent ideas and the follow ups I clicked on for 'getting started' all at least seem non-AI genned." — commenter johnnyanmac

> "The OP very much comes off to me as a 'here are 100 books you need to read before you die' recommendation porn type of post where the author has done none of the things listed." — commenter fxwin (on why curated short lists beat 100-item listicles)

> "I've seen your list before and find it much easier to appreciate than the OP tbh. It is very concise, the descriptions actually describe what one might learn or struggle with and each project comes with resources to get started with" — commenter fxwin, on Austin Henley's "Challenging programming projects" list

> "I think the most reliable way to understand a system is to directly implement the internals of a library. In particular, hands-on experience with networks and file systems is incredibly helpful when writing high-level code." — commenter fredisbusy

> "Highly recommend writing a BitTorrent client. The spec is easy to grok, it has a bunch of fun subproblems that you can go as deep or as shallow as you want into, and it's super rewarding being able to download something like the Debian kernel after all of your hard work." — commenter sanufar

> "As part of undergrad we had to implement space invaders on a Zync FPGA… It was a blast seeing what people came up with as you could do 'extras' that gave you bonus points." — commenter matthewfcarlson (project-with-extensions pedagogy)

> "I ask Gemini 3 Pro about the relative difficulty of each project in the list… Redis Clone 20–40h… Git 20–40h… Kafka Broker 30–60h… RAFT 40–80h… SQLite Clone 60–120h" — commenter lifthrasiir (difficulty/time framing for the wheel-projects; AI-assisted estimate, treat as rough)

## Relevance

- Bears on hypotheses: H2 (systems/wheel projects signal mastery), H4 (level-dependent shape), H1 (hygiene > domain)
- H4 is the headline: the single most repeated criticism of the project-idea genre is ungraded difficulty ("levels of difficulty are all over the place", "would help to group projects by difficulty"). The community consensus is that project lists must be *level-calibrated* — a Redis clone is a 20–40h moderate project; RAFT and SQLite clones are 40–120h expert projects. Choosing a project above one's level produces the "feels well beyond my capabilities" paralysis visible in the thread (irishloop, rramadass).
- H2: the projects the thread praises (BitTorrent client, Redis, database internals) are all build-from-scratch re-creations of real systems, and fredisbusy's maxim — implement the internals to understand the system — is the community rationale. xthe's "small and complete… clarity, constraints, finishing the whole arc, not scale" is the counterweight: impressive means *finished and comprehensible*, not big.
- H1 adjacent: the thread's sneering at 100-item listicles ("recommendation porn") is the mandated opposition evidence — quantity of tutorial projects signals nothing; a short list of completed, deep projects is what the community respects.
