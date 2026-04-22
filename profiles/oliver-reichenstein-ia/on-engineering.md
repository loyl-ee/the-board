# Oliver Reichenstein — On Engineering

## Removing Complexity Is the Engineering Achievement

Reichenstein's most important engineering principle is that simplicity is the product of engineering effort, not its absence. iA Writer is not simple because it was easy to build — it is simple because enormous engineering effort was invested in removing everything that was not essential. The writing environment, the custom fonts, the Authorship tracking system, the Markdown handling — each represents significant engineering work applied to the goal of making writing feel effortless.

His "scalpel in a world of Swiss army knives" metaphor applies directly to engineering decisions: a system that does one thing excellently is an engineering achievement. A system that does many things adequately is an engineering failure of ambition. The discipline is choosing what the one thing is and having the restraint to build only that.

## Typography as a Technical System

Reichenstein's work on iA Writer's custom fonts (Mono, Duo, Quattro — released in 2018, built on IBM Plex) demonstrates that typography is an engineering discipline, not just a design preference. Each font required specific technical decisions: character width algorithms, punctuation character metrics, OpenType feature support, hinting for low-resolution displays, and cross-platform rendering differences between macOS, iOS, and Windows.

The engineering work of typography: consistent rendering across operating systems and rendering engines is a solved problem only in theory. In practice, it requires testing, fallback strategies, and sometimes font-level adjustments for specific platforms.

## The Authorship System: Engineering for Provenance

iA Writer 7's Authorship feature — which tracks which text is human-written versus AI-generated, and updates as the human edits AI text — required engineering novel metadata storage alongside Markdown files. The implementation uses "Markdown Annotations" format published to GitHub as an open standard, so other applications can implement it.

The engineering decisions: provenance metadata is stored separately from the document content (so the document remains a clean Markdown file), the format is human-readable, and the visual representation (gradual darkening as AI text is edited) requires a custom text rendering layer. This is non-trivial engineering in service of a clear design intention.

## Plain Text as an Engineering Commitment

iA Writer stores documents as plain Markdown files — no proprietary format, no database, no metadata lock-in. The engineering commitment behind this: the user's documents must remain accessible regardless of whether iA Inc. continues to exist. Plain text is the most durable storage format in computing history.

For software engineers: proprietary data formats are a liability, both for users (who cannot easily switch tools) and for engineers (who must maintain parsers, exporters, and migration tools). When a standard format exists that meets your requirements, use it.

## Local Processing as a Privacy Architecture

iA Writer's Style Check and Syntax Highlight features process text entirely on-device. No content is sent to iA's servers. The engineering discipline: local processing is more complex to implement (it requires bundling processing logic into the app binary) but eliminates the privacy, latency, and availability risks of server-side processing.

The engineering question for any feature that processes user content: does this require server processing, or can it be done locally? Local processing that is fast enough is always preferable.

## Sources
- [ia.net — iA's blog and essays](https://ia.net/topics)
- [iA Writer custom fonts — ia.net](https://ia.net/topics/a-typographic-christmas)
- ["No Feature" — ia.net, November 2023](https://ia.net/topics/no-feature)
- [iA Writer Authorship — ia.net](https://ia.net/topics/authorship)
- [iA Writer fonts on GitHub — open source](https://github.com/iaolo/iA-Fonts)
