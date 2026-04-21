# Linus Torvalds — On Web

## Honest Gap Note

Torvalds' documented views on web technologies specifically are sparse. He does not work in web development, rarely comments on it in technical forums, and his primary intellectual domain — operating system kernels and version control — is as far from front-end web development as software engineering gets. No substantial body of quotes exists where he analyzes web frameworks, browsers, HTTP, or JavaScript in depth. Any profile claiming detailed opinions from Torvalds on web technology specifically should be treated skeptically.

What does exist is documented below, along with his general principles on complexity and bloat that apply directly to web development problems.

## On Complexity and Bloat

Torvalds has spoken about Linux kernel bloat in terms that translate readily to web development. In September 2009, he acknowledged: "Sometimes it's a bit sad that we are definitely not the streamlined, small, hyper-efficient kernel that I envisioned 15 years ago... The kernel is huge and bloated, and our icache footprint is scary." He drew a distinction between "acceptable and avoidable" — bloat can be both real and structurally difficult to eliminate once it has accumulated.

His view on XML — "XML is crap. Really. There are no excuses" (Google+, 2014) — is a direct comment on a technology still widely used in web services and configuration. The criticism is about verbosity and unnecessary structural complexity when simpler formats would serve better.

His coding philosophy generally — favoring simple data structures, clean interfaces, and minimal abstractions — is a working framework for evaluating web architecture. Over-engineered front-end build systems, massive dependency trees, and frameworks that add abstraction without adding capability are all recognizable instances of the problems he has criticized in other contexts.

## What He Would Likely Notice

Based on his documented views, Torvalds would likely be concerned by web development patterns that: create fragile dependency chains (hundreds of npm packages for simple functionality), hide the underlying model from the developer behind "magic" abstractions, sacrifice performance for developer convenience, and accumulate backwards-incompatible changes that force users to constantly update. These are not speculative — they follow directly from his stated positions on software design and infrastructure. They are offered here as principled extrapolations, not documented opinions.

## Git and the Web

Torvalds' most direct contribution to the web development ecosystem is Git, which underpins GitHub, GitLab, and the overwhelming majority of web development workflows. Git's design — distributed, content-addressed, fast branching — has shaped how web development collaboration works at the infrastructure level. This is his most significant and well-documented relationship with the web technology ecosystem.
