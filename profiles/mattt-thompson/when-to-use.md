# When to Use — Mattt Thompson

## Invoke Mattt Thompson When

**API design decisions** — When designing an interface that other developers will use: REST API surface, SDK design, framework architecture, CLI command structure. Thompson's core insight — that API design is UX design and that the Principle of Least Surprise (clear intent, reasonable defaults, control) is the governing standard — applies directly. Ask: what does the common case look like? Does the error message tell the developer what went wrong and how to recover? Does the default behavior match what most users need?

**Documentation strategy** — When deciding how much to document, in what format, and to what depth. Thompson's position is unambiguous: documentation is a first-class deliverable, not a support cost. His NSHipster model — comprehensive, opinionated, written for a reader who is capable of understanding the full depth — is a benchmark worth measuring against. Use his framework when there is organizational pressure to ship underdocumented features.

**iOS or Swift technical decisions** — When making architectural choices about iOS/macOS/watchOS development: framework selection, dependency management philosophy, Swift language feature adoption, migration timing (Objective-C to Swift, UIKit to SwiftUI). Thompson has written substantively about nearly every major iOS platform transition.

**Open source community questions** — When deciding whether to open source a library, how to handle maintenance commitments, how to communicate deprecations, or how to build a contributor community. His "Stewardship" framework is the clearest available articulation of what open source maintenance obligations actually entail.

**Understanding things deeply** — When the team's instinct is to copy a pattern without understanding it. Thompson's career is an argument for the value of understanding tools at the level of their design intent, not just their surface API. Invoke him when the pressure is toward "just make it work" and the risk is that working incorrectly will compound over time.

## Blind Spots

Thompson's perspective is narrowly focused on the Apple developer ecosystem and developer-facing products. He has limited public thinking about:

- Consumer app growth, acquisition, or retention strategy
- Non-Apple platforms (Android, web apps, cross-platform frameworks)
- Venture-backed startup dynamics, fundraising, or product-market fit
- Quantitative product analytics or A/B testing philosophy
- Enterprise software or B2B product concerns

His open source model — give away high-quality work, build reputation — works well for individuals and developer tools companies but does not translate directly to consumer product businesses.

## Good Pairings

**Paul Hudson** (on Swift education) — Hudson and Thompson share a commitment to making Swift deeply understandable, but Hudson's work is more tutorial-oriented and accessible to beginners. Pair them when the decision involves both technical depth (Thompson) and educational clarity (Hudson).

**Chris Eidhof** (on functional Swift and type-driven design) — Eidhof's functional programming perspective complements Thompson's emphasis on clear APIs and good defaults. Eidhof pushes further into type system expressiveness; Thompson anchors the discussion in practical developer experience. Pair them on API design decisions where elegance and usability are both at stake.

**Brent Simmons** (on indie iOS development and long-term software stewardship) — Simmons brings a consumer-facing perspective on Apple platform development that Thompson largely lacks. Together they cover both the developer-facing and user-facing dimensions of building lasting Apple software.
