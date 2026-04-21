# Oliver Reichenstein — On Product

## iA Writer as an Encoded Philosophy

iA Writer is not simply a text editor with fewer features. Every design decision in iA Writer encodes a specific philosophical position about writing, thinking, and tools. Understanding the product means understanding the reasoning behind each constraint.

## Markdown as a Feature, Not a Workaround

When iA Writer was designed, Markdown was a niche markup syntax used by developers and technical writers. Reichenstein saw it differently: Markdown separates the act of writing from the act of formatting. By writing in plain Markdown and not hiding the syntax, iA Writer makes the writer aware of structure without demanding they stop to format. The essay "Markdown and the Slow Fade of the Formatting Fetish" (ia.net, March 2025) articulates the position: "By not hiding [Markdown], we resisted turning it into a format." Proprietary formats hide complexity and create lock-in; Markdown exposes structure while keeping text portable.

Plain text files mean that your writing is always yours. iA Writer does not invent a proprietary file format. The files open in any text editor on any platform, now and in the future. This is not a technical detail — it is an ethical commitment to non-dependency.

## The Typography: Mono, Duo, Quattro

The original iA Writer used a monospace typeface (Nitti, by Bold Monday) as its sole composition font. The reasoning, explained by Reichenstein in a 2017 blog post: monospace fonts signal "this text is work in progress," while proportional fonts signal "this is almost done." By writing in monospace, the writer stays in drafting mode — less inclined to treat early text as finished.

In 2018, iA released three custom fonts — Mono, Duo, and Quattro — built on IBM Plex, with IBM's brand-specific features removed ("A Typographic Christmas," ia.net, December 2018). Square dots replaced round ones, curves were adjusted for neutrality, and large word spacing was preserved across all three. Duo is mostly monospaced with wider characters for M and W. Quattro is closer to a proportional typeface while retaining the word spacing and punctuation character width of monospace — optimized for small screens. The fonts are open-source, available on GitHub.

## Focus Mode and Typewriter Scrolling

Focus Mode — present since the original 2010 launch — fades all text except the current sentence or paragraph. Combined with Typewriter scrolling (which keeps the cursor at the vertical center of the screen, mimicking a physical typewriter), it creates a designed environment of attention. Reichenstein wanted "to develop a tool for writing that could only be used for writing. So we based it on the typewriter." He used a typewriter himself during the design process and found he wrote better on it — the physical act of translation informed the digital design.

One user described the effect: "The blue cursor blinking at the centre of my screen triggers a deep desire to put words down." This is the product working as designed.

## Syntax Highlight and Style Check

Syntax Highlight (introduced in iA Writer 4) colors parts of speech: adjectives in one color, adverbs in another, verbs in another. It does not tell the writer what to do. It makes visible what the writer is doing — overuse of adjectives, passive voice ("to be" constructions), repetitive nouns. The writer decides what to change.

Style Check (introduced 2020, "The Power of Style Check," ia.net, July 2020) flags fillers ("basically," "pretty much"), redundancies ("combine together"), and clichés ("against all odds"). The philosophy is identical: the tool prompts reflection, does not impose correction. All processing occurs locally on the device — no content is sent to external services. The feature quotes Strunk and Orwell as its intellectual forebears, positioning iA Writer in a tradition of writers' manuals about precision and economy of language.

## The Authorship Feature: AI Without Surrender

When every other writing app rushed to add AI generation in 2022-2023, iA did the opposite. In November 2023, iA Writer 7 launched with an "Authorship" feature that does not generate text — it tracks provenance. Text you type appears normally. Text pasted from an AI is visually dimmed. As you edit the AI-generated text, integrating it into your own voice, it gradually darkens toward your own text's color. When you are done, you can see clearly what is yours and what is borrowed.

The technical implementation stores authorship data separately from the document, in open "Markdown Annotations" format published to GitHub — so other apps can adopt the standard. Reichenstein's framing: "Honesty with others begins with honesty with ourselves, recognizing what is ours and what is borrowed." The feature works equally well for AI text and for text pasted from human co-authors, making it useful across all collaboration scenarios.

## Saying No as Product Strategy

iA Writer has no formatting toolbar. It has no font picker. For years it had no settings screen at all. Reichenstein was explicit about this: "Writer's deliberate absence of settings is a fundamental part of the app, and having no way to procrastinate with typography or other settings is one of the key reasons" for its effectiveness. "iA Writer is not successful because we choose the font size, it's because it helps people write."

The scalpel metaphor — "a scalpel in a world of Swiss army knives" — is the product strategy in one sentence. Every feature request that iA declines is an implicit decision to remain a scalpel.
