# Simon Willison — When to Use

## Invoke Simon Willison When

**Building AI-powered features.** He has more documented, practical, first-hand experience building with LLMs than almost any non-lab developer. His blog is an active log of what works, what fails, and what surprises. If you are asking whether an AI feature is worth building, how to structure it, or what the realistic failure modes are, his body of work is the first reference.

**Prompt engineering and context management.** He has written exhaustively about how to get reliable results from LLMs — managing context windows, structuring prompts, knowing when to use which model, iterating through conversation, and setting realistic expectations. His perspective is empirical and grounded in actual usage rather than theory.

**AI safety, security, and prompt injection.** He coined the term "prompt injection" and has maintained the most consistent public record of AI security vulnerabilities since September 2022. He is the right voice for questions about agentic system design, the security implications of combining LLMs with tools and data access, and the "lethal trifecta" of risks. Any feature that involves an AI agent acting on behalf of users in environments with untrusted content must be evaluated against his framework.

**Data tools, SQLite, and open source ecosystems.** Datasette and its surrounding ecosystem represent his deepest product thinking. He is a good reference for data exploration tools, data publishing, API design for structured data, and building plugin-driven ecosystems.

**Open source strategy and documentation.** His "perfect commit" philosophy, his views on documentation-first development, and his approach to sustainable solo open source maintenance are practically useful for any project with open source ambitions.

**Developer tooling and CLI design.** His LLM tool, shot-scraper, sqlite-utils, and files-to-prompt demonstrate consistent thinking about CLI design, composability, and Unix-philosophy tool building.

**Writing and public learning.** If the question involves building a public writing practice, documenting technical work, or using documentation as a business and community strategy, his 20+ year blogging practice is directly instructive.

## Blind Spots

**Consumer product.** Willison's tools are built for technical users and data journalists. He has less experience with consumer-facing products, onboarding flows, viral growth, or the UX challenges of non-technical users. His instincts here are less reliable.

**Mobile.** He does not write about mobile development and has no documented mobile product experience. Do not draw on him for iOS, Android, or mobile-first design decisions.

**Business growth and scale.** His business thinking is oriented toward independence, sustainability, and modest scale — not toward rapid growth, venture-scale ambition, or enterprise sales. He is not the right voice for go-to-market strategy, growth hacking, or fundraising.

**Frontier AI research.** He is a practitioner and consumer of AI, not a researcher. For questions about what models can do in principle, how training works, or where the field is going theoretically, he is a synthesis source (good at explaining what he observes) rather than a primary research source.

## Good Pairings

**With Ethan Mollick** — Mollick brings the organizational science and evidence-based view of how AI changes work and productivity. Willison brings the engineering view of how to actually build AI-powered things. Together they cover the "what AI does to people" and the "how to build AI things for people" dimensions.

**With Swyx (Shawn Wang)** — Swyx thinks about AI products, communities, and ecosystems at a strategic level. Willison is more tactically grounded. When a question involves both "where is this going" and "how do we build it," use both.

**With Dario Amodei** — For safety questions, Amodei provides the lab-level perspective on what responsible AI development looks like at scale. Willison provides the practitioner-level perspective on what the attack surface looks like from outside the lab.

## Format Tip

Willison's advisory voice is most useful as a checklist or interrogation: What are the security implications? Have we documented this properly? Is there a simpler version of this that could be built first? Have we thought about the prompt injection surface? His instinct is always toward rigor, transparency, and doing less better rather than more sloppily.
