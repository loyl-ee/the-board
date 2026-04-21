# Swyx — On Product

## The Smol Philosophy: Build Small to Learn Fast

Swyx's "smol" projects are his most direct expression of product philosophy. Smol-developer, launched May 2023 and announced on Twitter/X, was an early open-source coding agent: a ~200-line Python script that could scaffold an entire codebase from a product spec — not snippets, but a complete starting structure. He described it as "human-centric, coherent whole program synthesis" — your own "junior developer."

The design principles are revealing: intentionally small (under 200 lines), intentionally readable, intentionally customizable. The goal was not to build the definitive coding agent but to build the *minimum viable coding agent* — something simple enough for anyone to understand and fork, with enough capability to be genuinely useful. This is the smol aesthetic: prototype rapidly, ship immediately, learn from usage, and let the community fork it into directions you didn't anticipate.

In retrospect (in his Cognition essay), he describes smol-developer as "what smol developer should have become with more skills and conviction." This is the honest accounting of a builder who understands that rapid prototyping and going all-in on a conviction are different choices — and that he made the former when the latter might have been right.

## AI Wrappers vs. Genuine AI Products

Swyx holds a nuanced position on the "AI wrapper" debate. He resists the dismissive framing that any product built on top of a foundation model is merely a wrapper — because "every successful software company wraps something." At the same time, he recognizes that some products labeled as AI products are, in practice, thin interfaces that will be absorbed by platform incumbents.

His framework for what makes an AI product defensible (versus a wrapper that will fail):

1. **Proprietary data flywheels** — products that accumulate usage data that trains better models or makes better decisions over time. The data moat is real.
2. **Deep workflow integration** — products that live "where work is done" become structurally embedded and survive even when underlying model costs drop.
3. **Domain specificity** — products that apply AI to a specific domain with verifiable outputs (code execution, medical records, legal documents) have correctness constraints that general models can't easily replicate.
4. **UX that unlocks capability** — great AI UX can be a moat; it makes the model's full potential accessible rather than leaving users to discover it themselves.

## Building in Public as Product Strategy

Swyx's own products and platforms are built with the same "learn in public" ethos he advocates for individuals. Latent Space is a media product built in public — the editorial direction, the decision-making about guests and topics, the reasoning behind conference programming, the mistakes in conference execution — all documented and shared. This transparency is not accidental; it is a product strategy.

Publishing how you build a thing attracts an audience that trusts you precisely because you showed your work. That trust translates to subscriber loyalty, conference ticket demand, and the ability to launch new shows or tracks without starting from zero.

## The "Fire, Ready, Aim" Workflow

Swyx describes the AI product development workflow as "fire, ready, aim" — prototype with LLMs first, gather domain data from usage, validate the hypothesis cheaply before committing to infrastructure. This inverts the traditional "ready, aim, fire" product sequence and is enabled specifically by foundation models: you can get a working demo with API calls and prompts before writing any training code. The result is 1,000-10,000x cheaper hypothesis validation.

This is not recklessness. It is a recognition that the uncertainty at the beginning of an AI product is so high that extensive planning is less valuable than rapid empirical feedback. The risk management frame from his finance background applies: minimize the cost of being wrong before making large commitments.

## What Swyx Looks for in AI Products

Based on his writing and conference curation, the AI products that swyx finds genuinely interesting share common traits:
- They operate where verification is possible (code that runs, output that can be evaluated against ground truth)
- They build on usage, not just capability — the product gets better as more people use it
- They are built by people with domain expertise, not just AI expertise
- They treat the model as a component, not as the product itself

He is skeptical of demos that showcase impressive capabilities in isolation from any product context. His emphasis is always on: does this ship, does it work reliably for real users, and does it improve over time?

## Cognition as Vision for AI Products

His decision to join Cognition (the company behind Devin and Windsurf) reflects his product thesis concretely: software development is the highest-value domain for AI products because code is verifiable. When an AI writes code, you can run it. That verifiability creates a feedback loop that other domains lack. He argues that "Code AGI will be achieved in 20% of the time of full AGI, and capture 80% of the value" — a characteristically quantified bet on where to place product focus.
