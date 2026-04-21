# Jordan Singer — On Product

## The Core Product Philosophy: Solve Your Own Problems

Singer has consistently built products that solve problems he personally experiences. He has stated directly: "building to solve my own problems proved far more relatable than building for someone else." This is not an unusual founding principle, but Singer applies it with unusual consistency — every major product in his history (lil software, Figma plugins, Diagram, Mainframe) emerged from his own friction as a designer-developer.

The implication for product decisions is that Singer tends to build tools where he understands the workflow deeply from the inside, rather than abstracting from user research. His detailed knowledge of Figma's plugin API, SwiftUI constraints, and design system mechanics directly shaped what Diagram's tools could and could not do.

## Diagram's Product Line

Diagram built focused tools, each addressing a distinct workflow problem:

**Magician** was the entry product — a Figma plugin that used deep generative models to generate icons from text descriptions, write copy, and insert imagery. It solved a specific, immediate pain point: the blank-canvas problem for common design assets. This focus contributed to its rapid adoption.

**Genius** was the more ambitious product — an AI design companion that understood the active design context and made autocomplete suggestions using the project's own design system components. As Singer described it, Genius "understands what you're designing and makes suggestions that autocomplete your design using components from your design system" and "ideates and iterates alongside you as you design." This was a significantly harder technical and UX problem: the system had to understand design intent, not just respond to text prompts.

**Automator** addressed the workflow automation gap — it allowed designers to build custom Figma automations visually, without code. Singer modeled it consciously on Apple's Shortcuts app, and prioritized familiarity with Figma's own design language to reduce learning curve.

**Fig** (under the Tricycle AI brand, pre-Diagram) was an earlier AI design assistant prototype inside Figma, using natural language input to create design elements. It established the foundational interaction model that Genius later refined.

## Product Decisions in the lil software Line

The lil software iOS apps represent a different kind of product philosophy: radical scope reduction as a feature. Each app does one thing. lil weather shows the weather in your preferred unit. lil calculator calculates. lil draw draws. The product decision that made these apps notable was not the feature set — it was the refusal to add features and the quality of execution on the single feature chosen.

Several apps (lil notes, lil todo, lil browser) were rejected by Apple's App Store review for guideline violations. Singer appealed, accepted the rejections, and continued distributing them via TestFlight. This experience shaped his thinking about App Store policies and alternative distribution — he subsequently built Airport, a TestFlight discovery platform, partly as a practical solution to his own distribution problem.

## Mainframe: Proactive Over Reactive

At Mainframe, Singer's product thesis is a direct critique of current productivity software: "The core ways we interact with computers haven't kept pace with technological advancements. While software has grown more powerful, it's still reactive — requiring manual input at every step." Cobot is designed to be agent-native: it anticipates needs rather than waiting for commands. The three design principles Singer articulates for AI agents in this context are accessibility, collaboration (human-AI teamwork in shared environments), and familiarity (patterns users already know from consumer software).

## On AI as a "Jumping Off Point"

In describing Make Designs at Figma's Config 2024, Singer framed AI-generated designs as "a jumping off point" for designers, not finished output. This framing — AI produces a first draft, humans craft the meaning — has been consistent across his work from Diagram to Mainframe. It reflects both a product philosophy (AI outputs require human judgment to become good products) and a positioning choice (avoids the "AI replaces designers" framing that generates resistance).
