# The Board

33 curated advisors. Encoded as markdown. Inject into any AI coding session.

The Board is a knowledge database of 33 people and studios — founders, engineers, designers, indie developers, AI researchers — whose documented philosophies serve as advisory voices across code reviews, architecture decisions, product critiques, and business calls.

Point your AI at the files, describe your problem, and get voices that challenge your thinking before you build, ship, or commit. Works with Claude, Cursor, Copilot, Gemini, ChatGPT — any model that can read a file or fetch a URL.

---

## Disclaimer

This is an unofficial, independently maintained knowledge resource. Every profile is compiled entirely from publicly available material — blog posts, books, talks, interviews, and podcasts that are already on the internet. The Board consolidates those ideas into one place for easier reference. Nothing here is invented or fabricated.

No one listed here has reviewed, approved, or endorsed this content. Profiles represent a good-faith interpretation of each person's documented public positions, not a personal relationship with any of them. Views may be simplified, and some positions may have evolved since the source material was published.

If you're listed here and find something inaccurate or would prefer to be removed, open an issue or DM [@loylee on X](https://x.com/loylee) and we'll address it promptly.

---

## How It Works

Each advisor lives in `profiles/<folder>/` as a set of topic files. Every profile has 12 core files (`on-engineering.md`, `on-business.md`, `on-design.md`, `on-ux.md`, and more). Select profiles also have specialised engineering files: `on-architecture.md`, `on-backend.md`, `on-frontend.md`, `on-mobile.md`, `on-security.md`, `on-testing.md`.

You tell your AI which files to read, describe your decision, and get advisory perspectives grounded in each person's actual documented thinking.

---

## Setup

The Board is plain markdown — it works with any AI that can read files or fetch URLs. The setup file name depends on your tool:

| Tool | Config file |
|---|---|
| Claude Code | `CLAUDE.md` |
| Cursor | `.cursorrules` |
| GitHub Copilot | `.github/copilot-instructions.md` |
| Gemini CLI | `GEMINI.md` |
| Windsurf | `.windsurfrules` |
| ChatGPT / other | Paste the URL directly into your prompt |

### Method 1 — GitHub URL (no download required)

Add this to your tool's config file:

```markdown
## The Board
When asked to consult The Board, fetch:
https://raw.githubusercontent.com/loyl-ee/the-board/main/BOARD.md
for the roster, engineering files, and decision matrix. Advisor files follow this pattern:
https://raw.githubusercontent.com/loyl-ee/the-board/main/profiles/{folder}/{file}.md
```

For tools without a config file, paste the URL directly into your prompt:

> "Fetch https://raw.githubusercontent.com/loyl-ee/the-board/main/BOARD.md then read `on-engineering.md` from `dhh` and `simon-willison`. Review this architecture: [describe it]"

### Method 2 — Local copy (faster, works offline)

```bash
git clone https://github.com/loyl-ee/the-board.git
cp -r the-board/profiles/ your-project/the-board/
```

Then add to your tool's config file:

```markdown
## The Board
Advisor profiles are in the-board/profiles/.
See the-board/profiles/CLAUDE.md for the full index and how to use them.
```

---

## Example Invocations

**Architecture review before you build:**
> "Read `on-architecture.md` from `dhh` and `linus-torvalds`, then challenge this system design before I build it: [paste design]"

**Security audit:**
> "Read `on-security.md` from `simon-willison`, `dario-amodei`, and `marco-arment`. Find the risks in this approach: [describe it]"

**Testing strategy:**
> "Read `on-testing.md` from `dhh`, `chris-eidhof`, and `linus-torvalds`. I'm deciding whether to go TDD — give me three different takes."

**Over-engineering check:**
> "Read `on-engineering.md` from `pieter-levels` and `dhh`. Am I over-engineering this? [describe your approach]"

**Business model:**
> "Read `on-business.md` from `dhh`, `pieter-levels`, and `marco-arment`. Three different takes on whether I should add a subscription tier."

**Full-team product critique:**
> "Read `when-to-use.md` from `steve-jobs`, `dhh`, and `pieter-levels`, then read their `on-product.md` files. I'm about to add [feature] — tear it apart."

---

## The Advisors

| Folder | Who | Known for |
|---|---|---|
| `bill-campbell` | Bill Campbell | The Coach — people, culture, executive trust |
| `steve-jobs` | Steve Jobs | Product vision, "Real Artists Ship", insanely great |
| `dhh` | DHH | Rails, Basecamp, monolith-first, calm company |
| `reid-hoffman` | Reid Hoffman | Blitzscaling, network effects, LinkedIn |
| `tim-ferriss` | Tim Ferriss | 80/20, minimum effective dose, launch strategy |
| `kevin-rose` | Kevin Rose | Community products, habit apps, Digg |
| `sal-soghoian` | Sal Soghoian | Shortcuts, AppleScript, user scriptability |
| `andy-hertzfeld` | Andy Hertzfeld | Original Mac, software as art |
| `brent-simmons` | Brent Simmons | NetNewsWire, Mac-native, open web |
| `steve-troughton-smith` | Steve Troughton-Smith | iOS/iPadOS internals, platform capabilities |
| `marco-arment` | Marco Arment | Overcast, indie iOS, native quality, audio |
| `mattt-thompson` | Mattt Thompson | AFNetworking, NSHipster, API design |
| `paul-hudson` | Paul Hudson | Hacking with Swift, 100 Days, accessibility |
| `chris-eidhof` | Chris Eidhof | objc.io, functional Swift, type-driven design |
| `david-smith` | David Smith | Widgetsmith, privacy-first iOS, indie sustainability |
| `jony-ive` | Jony Ive | Industrial design, simplicity as mastery |
| `oliver-reichenstein-ia` | Oliver Reichenstein | iA Writer, typography, focused software |
| `jordan-singer` | Jordan Singer | AI design tools, Diagram, Mainframe |
| `amelia-wattenberger` | Amelia Wattenberger | Human-AI interfaces, GitHub Copilot UX |
| `amber-case` | Amber Case | Calm technology, notification ethics, ADHD design |
| `linus-torvalds` | Linus Torvalds | Linux, Git, quality standards, never break userspace |
| `jensen-huang` | Jensen Huang | NVIDIA, GPU computing, 30-year platform bets |
| `demis-hassabis` | Demis Hassabis | DeepMind, AlphaFold, scientific AI |
| `dario-amodei` | Dario Amodei | Anthropic, Constitutional AI, responsible development |
| `simon-willison` | Simon Willison | Datasette, llm CLI, prompt injection, practitioner AI |
| `ethan-mollick` | Ethan Mollick | Jagged frontier, human-AI collaboration |
| `swyx-shawn-wang` | Swyx / Shawn Wang | AI Engineer discipline, Latent Space |
| `zach-gage` | Zach Gage | SpellTower, Puzzmo, ethical game design |
| `lucas-pope` | Lucas Pope | Papers Please, Obra Dinn, games as argument |
| `team-alto-snowman` | Team Alto / Snowman | Alto's Adventure, emotional minimalism |
| `algoriddim-djay` | Algoriddim / djay | Neural Mix, real-time audio, native Apple |
| `procreate-savage-interactive` | Procreate | Bootstrapped, one-time purchase, anti-generative-AI |
| `pieter-levels` | Pieter Levels | Nomad List, PhotoAI, build in public, solo $1M ARR |

---

## File Reference

**Every profile (12 files):**
`overview.md` · `philosophy.md` · `on-business.md` · `on-product.md` · `on-design.md` · `on-ux.md` · `on-customer-journey.md` · `on-web.md` · `on-safety.md` · `on-engineering.md` · `quotes.md` · `when-to-use.md`

**Select profiles also have:**
`on-architecture.md` · `on-backend.md` · `on-frontend.md` · `on-mobile.md` · `on-security.md` · `on-testing.md`

See [`BOARD.md`](BOARD.md) for the engineering decision matrix and full specialised file availability.  
See [`CLAUDE.md`](CLAUDE.md) for the complete decision matrix covering business, product, design, UX, and engineering.  
See [`profiles/CLAUDE.md`](profiles/CLAUDE.md) for the full profile reader's guide.
