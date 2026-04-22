# The Board — Dream Team Knowledge System

## What This Is

The Board is a curated database of 33 people and studios whose documented philosophies serve as advisory voices across every product, business, and design decision. Each profile lives in `profiles/<name>/` and contains 11 topic files covering their thinking on business, product, design, UX, customer journey, web, safety, and more.

**How to use it:** Read the Decision Matrix below to identify who to consult. Then ask Claude to read specific topic files from those profiles. You can pull one file from one person, or read the same topic (e.g., `on-ux.md`) across five people simultaneously.

**How to invoke them:** Tell Claude: *"Read the `on-business.md` files from `dhh`, `pieter-levels`, and `marco-arment`, then advise me on pricing."*

---

## The Team (33 profiles)

### Founders & Business Philosophers
| Folder | Person | Superpower |
|---|---|---|
| `bill-campbell` | Bill Campbell | The Coach — people, culture, trust, and the human side of building companies |
| `steve-jobs` | Steve Jobs | Product vision — insanely great products, focus, and the premium market |
| `dhh` | DHH (David Heinemeier Hansson) | Calm company — bootstrapping, saying no, opinionated software, anti-VC |
| `reid-hoffman` | Reid Hoffman | Blitzscaling — network effects, viral growth, and when to move fast |
| `tim-ferriss` | Tim Ferriss | Systems thinking — 80/20, minimum effective dose, launch strategy |
| `kevin-rose` | Kevin Rose | Community products — habit formation, building what you use, early adoption |

### Apple / Mac Ecosystem Insiders
| Folder | Person | Superpower |
|---|---|---|
| `sal-soghoian` | Sal Soghoian | Automation — Shortcuts, AppleScript, scriptability as a product feature |
| `andy-hertzfeld` | Andy Hertzfeld | Software as art — craft, humanism, and the original Mac philosophy |
| `brent-simmons` | Brent Simmons | Mac-native development — open source stewardship, the open web |
| `steve-troughton-smith` | Steve Troughton-Smith | Platform internals — what Apple's platforms can and should become |

### Apple Community Developers & Educators
| Folder | Person | Superpower |
|---|---|---|
| `marco-arment` | Marco Arment | Indie iOS business — quality, pricing, podcasting, native-over-web |
| `mattt-thompson` | Mattt Thompson | Documentation as craft — API design, deep understanding before use |
| `paul-hudson` | Paul Hudson | Swift education — accessible learning, 100 Days, free-to-paid models |
| `chris-eidhof` | Chris Eidhof | Functional Swift — types as documentation, small well-bounded components |
| `david-smith` | David Smith | Indie iOS sustainability — widgets, health apps, App Store economics |

### Design Legends
| Folder | Person | Superpower |
|---|---|---|
| `jony-ive` | Jony Ive | Industrial design — materials, simplicity, emotional product experience |
| `oliver-reichenstein-ia` | Oliver Reichenstein / iA | Writing tools — typography, focused software, "the web is 95% typography" |
| `jordan-singer` | Jordan Singer | AI design tools — design systems, AI-native interfaces, fast iteration |
| `amelia-wattenberger` | Amelia Wattenberger | Human-AI interfaces — designing the layer between humans and AI systems |

### Calm, Ethical & Accessible Design
| Folder | Person | Superpower |
|---|---|---|
| `amber-case` | Amber Case | Calm technology — minimum viable attention, notification ethics, designing for ADHD |

### Open Source & Infrastructure Philosophy
| Folder | Person | Superpower |
|---|---|---|
| `linus-torvalds` | Linus Torvalds | Quality standards — open source governance, never breaking userspace |

### AI Leaders (Foundation Models)
| Folder | Person | Superpower |
|---|---|---|
| `jensen-huang` | Jensen Huang | Platform strategy — hardware-software co-design, 30-year technology bets |
| `demis-hassabis` | Demis Hassabis | Scientific AI — long-termism, AGI safety, science as AI's highest application |
| `dario-amodei` | Dario Amodei | Responsible AI — safety-first development, Constitutional AI, scaling ethics |

### AI Practitioners (Building WITH AI)
| Folder | Person | Superpower |
|---|---|---|
| `simon-willison` | Simon Willison | Practitioner AI — building real things with LLMs, prompt injection safety |
| `ethan-mollick` | Ethan Mollick | Human-AI collaboration — the jagged frontier, what AI is actually good at |
| `swyx-shawn-wang` | Swyx / Shawn Wang | AI Engineer discipline — AI product stack, building defensible AI products |

### Indie Game Designers
| Folder | Person | Superpower |
|---|---|---|
| `zach-gage` | Zach Gage | Mobile game design — reimagining classics, systems thinking, ethical monetization |
| `lucas-pope` | Lucas Pope | Games as communication — mechanics inseparable from meaning |
| `team-alto-snowman` | Team Alto / Snowman | Emotional minimalism — atmosphere, one-button simplicity, game as feeling |

### App Studios (Products as Philosophy)
| Folder | Person | Superpower |
|---|---|---|
| `algoriddim-djay` | Algoriddim / djay | AI in creative tools — Neural Mix, native Apple integration, professional accessibility |
| `procreate-savage-interactive` | Procreate / Savage Interactive | Creative tool ethics — bootstrapped dominance, one-time purchase, anti-generative-AI |

### Indie Hackers / Solo Builders
| Folder | Person | Superpower |
|---|---|---|
| `pieter-levels` | Pieter Levels | Radical shipping — build in public, charge from day one, solo to $1M ARR |

---

## Decision Matrix

Use this to identify which profiles to read for a given decision. Read `when-to-use.md` in each profile for nuance on pairing and blind spots.

### Starting Something New
```
Starting a new app idea              → steve-jobs, bill-campbell, marco-arment, pieter-levels
Validating a product idea quickly    → pieter-levels, tim-ferriss, david-smith
Solo founder, where to begin         → pieter-levels, marco-arment, david-smith, dhh
Deciding what to build next          → steve-jobs, dhh, marco-arment
```

### Business Strategy & Model
```
Pricing & monetisation               → dhh, pieter-levels, marco-arment, david-smith, procreate-savage-interactive
One-time purchase vs. subscription   → procreate-savage-interactive, marco-arment, david-smith, dhh
Bootstrap vs. VC                     → dhh, pieter-levels, procreate-savage-interactive, reid-hoffman (for the VC case)
When to blitzscale                   → reid-hoffman (for), dhh (against) — read both
Network effects products             → reid-hoffman, kevin-rose, tim-ferriss
Launch strategy & marketing          → tim-ferriss, pieter-levels, reid-hoffman
Community-driven growth              → kevin-rose, reid-hoffman, pieter-levels
Staying indie / calm company         → dhh, marco-arment, pieter-levels, procreate-savage-interactive
```

### Product Decisions
```
Product vision & direction           → steve-jobs, dhh, jony-ive, marco-arment
Killing features / saying no         → steve-jobs, dhh, oliver-reichenstein-ia, jony-ive
Making something "insanely great"    → steve-jobs, andy-hertzfeld, jony-ive
Opinionated software decisions       → dhh, oliver-reichenstein-ia, marco-arment
App Store strategy (iOS/Mac)         → david-smith, marco-arment, steve-troughton-smith
Widget / home screen design          → david-smith, jony-ive, amber-case
Game design decisions                → zach-gage, lucas-pope, team-alto-snowman
Creative tool design                 → procreate-savage-interactive, algoriddim-djay, jony-ive
Writing tool design                  → oliver-reichenstein-ia, brent-simmons, amber-case
```

### Design & UX
```
Visual design review                 → jony-ive, andy-hertzfeld, oliver-reichenstein-ia
UX review (general)                  → jony-ive, amelia-wattenberger, amber-case, steve-jobs
Designing for focus / calm           → amber-case, oliver-reichenstein-ia, team-alto-snowman
Notification design                  → amber-case, david-smith, marco-arment
Onboarding flow                      → amber-case, amelia-wattenberger, marco-arment, tim-ferriss
Accessibility                        → paul-hudson, amber-case, david-smith
Typography & reading UX              → oliver-reichenstein-ia, brent-simmons
Emotional design / atmosphere        → team-alto-snowman, jony-ive, lucas-pope, zach-gage
Game feel & interaction design       → zach-gage, team-alto-snowman, lucas-pope
```

### Building with AI
```
Adding AI features to a product      → simon-willison, ethan-mollick, swyx-shawn-wang, amelia-wattenberger
Designing AI interfaces/UX           → amelia-wattenberger, amber-case, ethan-mollick
Prompt engineering & LLM tools       → simon-willison, ethan-mollick, swyx-shawn-wang
AI safety in products                → simon-willison (prompt injection), dario-amodei, demis-hassabis
What AI is actually good/bad at      → ethan-mollick, simon-willison
Building AI-powered creative tools   → algoriddim-djay, procreate-savage-interactive (cautionary), amelia-wattenberger
Ethical AI product decisions         → dario-amodei, demis-hassabis, procreate-savage-interactive, amber-case
AI infrastructure & platform bets    → jensen-huang, dario-amodei, swyx-shawn-wang
```

### Web & Distribution
```
Web presence & landing pages         → tim-ferriss, pieter-levels, oliver-reichenstein-ia
Web vs. native app decision          → marco-arment, brent-simmons, dhh (web-first via Hotwire)
SEO & content strategy               → tim-ferriss, paul-hudson, pieter-levels
Newsletter & content business        → tim-ferriss, paul-hudson, ethan-mollick, simon-willison
Open web advocacy                    → brent-simmons, linus-torvalds, sal-soghoian
```

### Platform & Technical Decisions
```
Apple platform direction & future    → steve-troughton-smith, brent-simmons, marco-arment
Mac-native development               → brent-simmons, steve-troughton-smith, mattt-thompson
Swift / iOS technical decisions      → mattt-thompson, chris-eidhof, paul-hudson
Adding Shortcuts/automation support  → sal-soghoian, steve-troughton-smith
API design                           → mattt-thompson, chris-eidhof, dhh
Open source strategy                 → linus-torvalds, brent-simmons, simon-willison, mattt-thompson
Documentation strategy               → mattt-thompson, paul-hudson, simon-willison
```

### People, Culture & Ethics
```
Hiring & people decisions            → bill-campbell, steve-jobs, reid-hoffman
Team culture & trust                 → bill-campbell, dhh, andy-hertzfeld
Executive coaching moments           → bill-campbell
Ethics in software                   → dario-amodei, demis-hassabis, amber-case, procreate-savage-interactive
Privacy decisions                    → dario-amodei, david-smith, marco-arment, simon-willison
Safety & responsible development     → dario-amodei, demis-hassabis, simon-willison, linus-torvalds
Long-term infrastructure bets        → jensen-huang, linus-torvalds, demis-hassabis
```

### Education & Community
```
Educational product design           → paul-hudson, ethan-mollick, mattt-thompson
Free-to-paid model for education     → paul-hudson, tim-ferriss, marco-arment
Teaching with / using AI             → ethan-mollick, simon-willison, paul-hudson
Developer community building         → mattt-thompson, simon-willison, swyx-shawn-wang
```

### Engineering & Code
```
Architecture decisions               → dhh, mattt-thompson, chris-eidhof, linus-torvalds, simon-willison
Frontend engineering                 → oliver-reichenstein-ia, amelia-wattenberger, dhh, brent-simmons, jordan-singer
Backend engineering                  → dhh, linus-torvalds, simon-willison, mattt-thompson, pieter-levels
Security & privacy (engineering)     → simon-willison, dario-amodei, linus-torvalds, david-smith, marco-arment
Mobile / iOS engineering             → marco-arment, david-smith, brent-simmons, steve-troughton-smith, sal-soghoian
Testing strategy                     → linus-torvalds, chris-eidhof, dhh, mattt-thompson, simon-willison
API design                           → mattt-thompson, chris-eidhof, dhh, simon-willison, linus-torvalds
Code review & quality standards      → linus-torvalds, andy-hertzfeld, mattt-thompson, chris-eidhof
Tech debt decisions                  → dhh, linus-torvalds, pieter-levels, simon-willison
Shipping vs. refactoring             → pieter-levels, dhh, steve-jobs, linus-torvalds, marco-arment
Monolith vs. microservices           → dhh (monolith), simon-willison (pragmatic), linus-torvalds (simple)
Automation & scripting in products   → sal-soghoian, simon-willison, linus-torvalds
AI engineering in products           → simon-willison, ethan-mollick, swyx-shawn-wang, amelia-wattenberger
Over-engineering check               → pieter-levels, dhh, oliver-reichenstein-ia
```

---

## How to Use in a Claude Session

### Read a single profile section
> "Read `profiles/bill-campbell/on-business.md` and tell me what Campbell would say about my pricing decision."

### Read a topic across multiple profiles
> "Read the `on-ux.md` files from `jony-ive`, `amber-case`, and `amelia-wattenberger`, then critique the onboarding flow I'm about to describe."

### Invoke the team as advisors
> "Read `when-to-use.md` from `dhh`, `pieter-levels`, and `marco-arment`. Then read their `on-business.md` files. I want three different takes on whether I should add a subscription tier to my app."

### Check who to consult
> "Read this `CLAUDE.md` Decision Matrix and tell me which profiles are most relevant for deciding whether to build native or web-first."

### Profile file reference
All profiles contain these 12 files:
- `overview.md` — Who they are and why they're on the team
- `philosophy.md` — Core worldview and beliefs
- `on-business.md` — Business, growth, monetisation
- `on-product.md` — Product thinking and decisions
- `on-design.md` — Visual design and aesthetics
- `on-ux.md` — User experience and interaction
- `on-customer-journey.md` — Acquisition, retention, trust
- `on-web.md` — Web strategy and presence
- `on-safety.md` — Ethics, privacy, responsibility
- `on-engineering.md` — Code quality, architecture, technical philosophy
- `quotes.md` — Verbatim sourced quotes
- `when-to-use.md` — Best use cases, blind spots, pairings

Select profiles also contain specialised engineering files (`on-architecture.md`, `on-backend.md`, `on-frontend.md`, `on-mobile.md`, `on-security.md`, `on-testing.md`) — see `BOARD.md` for the full availability matrix.

---

## Profile Directory Index

```
profiles/
├── algoriddim-djay/          # AI in creative tools, native Apple integration
├── amber-case/               # Calm technology, ADHD design, notification ethics
├── amelia-wattenberger/      # Human-AI interfaces, data viz, GitHub Copilot UX
├── andy-hertzfeld/           # Original Mac, software as art, humanist computing
├── bill-campbell/            # The Coach, people, trust, executive culture
├── brent-simmons/            # Mac-native dev, open source, open web (inessential.com)
├── chris-eidhof/             # Functional Swift, objc.io, types as documentation
├── dario-amodei/             # Anthropic CEO, responsible AI, Constitutional AI
├── david-smith/              # Widgetsmith, indie iOS economics, health apps
├── demis-hassabis/           # DeepMind, AlphaFold, scientific AI, Nobel 2024
├── dhh/                      # Rails, Basecamp, calm company, anti-VC
├── ethan-mollick/            # Jagged frontier, human-AI collaboration, Wharton
├── jensen-huang/             # NVIDIA, GPU computing, platform strategy, 30-year bets
├── jony-ive/                 # Apple CDO, industrial design, simplicity as mastery
├── jordan-singer/            # AI design tools, Diagram→Figma, Mainframe
├── kevin-rose/               # Digg, Oak, Zero, community products, habit apps
├── linus-torvalds/           # Linux, Git, open source governance, quality standards
├── lucas-pope/               # Papers Please, Obra Dinn, games as moral argument
├── marco-arment/             # Overcast, Instapaper, indie iOS, audio quality
├── mattt-thompson/           # AFNetworking, NSHipster, documentation as craft
├── oliver-reichenstein-ia/   # iA Writer, typography, focused software design
├── paul-hudson/              # Hacking with Swift, 100 Days, accessible education
├── pieter-levels/            # Nomad List, PhotoAI, build in public, solo $1M ARR
├── procreate-savage-interactive/ # Bootstrapped dominance, anti-generative-AI ethics
├── reid-hoffman/             # LinkedIn, blitzscaling, network effects, Masters of Scale
├── sal-soghoian/             # Apple automation PM, Shortcuts, user empowerment
├── simon-willison/           # Datasette, llm CLI, prompt injection, AI practitioner
├── steve-jobs/               # Apple co-founder, product vision, insanely great
├── steve-troughton-smith/    # Platform internals, Apple capabilities, iPad advocate
├── swyx-shawn-wang/          # AI Engineer discipline, Latent Space, learn in public
├── team-alto-snowman/        # Alto's Adventure, emotional minimalism, atmosphere
├── tim-ferriss/              # 4-Hour Workweek, 80/20, MED, launch strategy, podcast
└── zach-gage/                # SpellTower, Puzzmo, game design philosophy, ethical monetization
```
