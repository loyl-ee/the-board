# The Board — Engineering Advisor System

> 33 curated advisors for code review, architecture decisions, and plan critique.  
> Inject into any coding project to get advisory voices that challenge your thinking.

**Repo:** https://github.com/loyl-ee/the-board  
**Raw file pattern:** `https://raw.githubusercontent.com/loyl-ee/the-board/main/profiles/{folder}/{file}.md`

---

## Setup

**Method 1 — GitHub URL (no download)**

Add this to your project's `CLAUDE.md`:

```markdown
## The Board
When asked to consult The Board, fetch:
https://raw.githubusercontent.com/loyl-ee/the-board/main/BOARD.md
Advisor files follow this pattern:
https://raw.githubusercontent.com/loyl-ee/the-board/main/profiles/{folder}/{file}.md
```

**Method 2 — Local copy**

Copy or clone `profiles/` into your project, then reference it in your project's `CLAUDE.md`:

```markdown
## The Board
Advisor profiles are in the-board/profiles/. See the-board/profiles/CLAUDE.md for the index.
```

---

## How to Invoke

```
"Read profiles/dhh/on-engineering.md and profiles/linus-torvalds/on-engineering.md,
then review this architecture decision: [describe it]"

"Read on-security.md from simon-willison, dario-amodei, and linus-torvalds.
Find the risks in this approach: [describe it]"

"Read on-testing.md from dhh, chris-eidhof, and mattt-thompson.
I'm deciding whether to go TDD — give me three different takes."

"Read the on-engineering.md files from pieter-levels and dhh.
Am I over-engineering this? [describe your approach]"

"Read on-architecture.md from dhh and simon-willison, then read their on-engineering.md.
Challenge this system design before I build it: [paste design]"
```

---

## Engineering Files (per profile)

Every profile has `on-engineering.md`. Select profiles also have:

| File | Available for |
|---|---|
| `on-architecture.md` | dhh, mattt-thompson, chris-eidhof, linus-torvalds, simon-willison, brent-simmons, marco-arment, swyx-shawn-wang |
| `on-backend.md` | dhh, linus-torvalds, simon-willison, mattt-thompson, pieter-levels, swyx-shawn-wang |
| `on-frontend.md` | oliver-reichenstein-ia, amelia-wattenberger, dhh, brent-simmons, jordan-singer, pieter-levels |
| `on-mobile.md` | marco-arment, david-smith, brent-simmons, steve-troughton-smith, sal-soghoian, algoriddim-djay, chris-eidhof |
| `on-security.md` | simon-willison, dario-amodei, linus-torvalds, david-smith, marco-arment, demis-hassabis, amber-case, pieter-levels |
| `on-testing.md` | linus-torvalds, chris-eidhof, dhh, mattt-thompson, simon-willison |

Original 11 files in every profile: `overview.md`, `philosophy.md`, `on-business.md`, `on-product.md`, `on-design.md`, `on-ux.md`, `on-customer-journey.md`, `on-web.md`, `on-safety.md`, `quotes.md`, `when-to-use.md`

---

## Engineering Decision Matrix

```
Architecture decisions          → dhh, mattt-thompson, chris-eidhof, linus-torvalds, simon-willison
Frontend engineering            → oliver-reichenstein-ia, amelia-wattenberger, dhh, brent-simmons, jordan-singer
Backend engineering             → dhh, linus-torvalds, simon-willison, mattt-thompson, pieter-levels
Security & privacy              → simon-willison, dario-amodei, linus-torvalds, david-smith, marco-arment
Mobile / iOS engineering        → marco-arment, david-smith, brent-simmons, steve-troughton-smith, sal-soghoian
Testing strategy                → linus-torvalds, chris-eidhof, dhh, mattt-thompson, simon-willison
API design                      → mattt-thompson, chris-eidhof, dhh, simon-willison, linus-torvalds
Code review & quality           → linus-torvalds, andy-hertzfeld, mattt-thompson, chris-eidhof
Tech debt                       → dhh, linus-torvalds, pieter-levels, simon-willison
Shipping vs. refactoring        → pieter-levels, dhh, steve-jobs, linus-torvalds, marco-arment
Monolith vs. microservices      → dhh (monolith) | simon-willison (pragmatic) | linus-torvalds (simple)
Automation & scripting          → sal-soghoian, simon-willison, linus-torvalds
AI engineering in products      → simon-willison, ethan-mollick, swyx-shawn-wang, amelia-wattenberger
Over-engineering check          → pieter-levels, dhh, oliver-reichenstein-ia
```

---

## Advisor Roster

| Folder | Who | Engineering superpower |
|---|---|---|
| `bill-campbell` | Bill Campbell | Engineering team culture, psychological safety |
| `steve-jobs` | Steve Jobs | Ship or don't — "Real Artists Ship" |
| `dhh` | DHH | Monolith-first, Rails, opinionated conventions |
| `reid-hoffman` | Reid Hoffman | Scale architecture, network-effects systems |
| `tim-ferriss` | Tim Ferriss | 80/20 applied to technical decisions |
| `kevin-rose` | Kevin Rose | Consumer app architecture, habit mechanics |
| `sal-soghoian` | Sal Soghoian | Automation APIs, Shortcuts, user scriptability |
| `andy-hertzfeld` | Andy Hertzfeld | Software as craft, humanist computing |
| `brent-simmons` | Brent Simmons | Mac-native Cocoa, open web, long-term code |
| `steve-troughton-smith` | Steve Troughton-Smith | Platform internals, iOS/iPadOS capabilities |
| `marco-arment` | Marco Arment | Native iOS quality, audio engineering, privacy |
| `mattt-thompson` | Mattt Thompson | API design, documentation-driven development |
| `paul-hudson` | Paul Hudson | Swift best practices, accessibility-first |
| `chris-eidhof` | Chris Eidhof | Functional Swift, type-driven architecture |
| `david-smith` | David Smith | Widget engineering, privacy-first iOS |
| `jony-ive` | Jony Ive | Invisible complexity, craft in implementation |
| `oliver-reichenstein-ia` | Oliver Reichenstein | Typography-as-engineering, radical simplicity |
| `jordan-singer` | Jordan Singer | AI-native interfaces, design systems as code |
| `amelia-wattenberger` | Amelia Wattenberger | Human-AI interface engineering |
| `amber-case` | Amber Case | Calm tech, minimal data, accessibility |
| `linus-torvalds` | Linus Torvalds | Systems quality, never break userspace, code review |
| `jensen-huang` | Jensen Huang | Hardware-software co-design, platform engineering |
| `demis-hassabis` | Demis Hassabis | AI systems, scientific software engineering |
| `dario-amodei` | Dario Amodei | Safe AI engineering, responsible deployment |
| `simon-willison` | Simon Willison | Practitioner AI, prompt injection, SQLite, docs |
| `ethan-mollick` | Ethan Mollick | Human-AI collaboration, LLM system design |
| `swyx-shawn-wang` | Swyx / Shawn Wang | AI product stack, defensible AI engineering |
| `zach-gage` | Zach Gage | Game systems, ethical app engineering |
| `lucas-pope` | Lucas Pope | Constraint-driven systems, solo engineering |
| `team-alto-snowman` | Team Alto / Snowman | Minimalist engineering, one-mechanic systems |
| `algoriddim-djay` | Algoriddim / djay | Real-time audio, Core ML, native Apple platform |
| `procreate-savage-interactive` | Procreate | Privacy-first architecture, GPU canvas, no telemetry |
| `pieter-levels` | Pieter Levels | Ship fast, simple stack, solo-maintainable code |
