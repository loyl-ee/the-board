# Amelia Wattenberger — On Customer Journey

## Designing for Developers as Users

The majority of Wattenberger's product work has been targeted at developers — first at GitHub (Copilot, Code Brushes, Copilot for Docs), then at Augment Code (Intent). This gives her a detailed, grounded understanding of a specific and demanding user type: people who are both technically sophisticated and deeply opinionated about their tools.

Her key insight about developer users: they care about staying in flow. The worst thing an interface can do to a developer is force a context switch — make them leave their editor, type a question somewhere else, wait for an answer, and then return. The ghost text pattern is optimized entirely around this: it meets developers inside their existing work context, makes its suggestion visible without demanding attention, and disappears without friction if ignored.

## User Mental Models in AI Interfaces

Wattenberger understands that users approach AI interfaces with mental models developed from other software — search boxes, command lines, messaging apps. These models are often wrong for LLM interactions but impossible to discard. The blank chat box exploits the wrong mental model: users type as if they are searching, when effective prompting is more like briefing a colleague.

Her solution is not to fix the mental model through documentation or onboarding (which users skip) but to build interfaces that make the correct mental model visible. If you want users to understand that the AI is a specialist with a particular role, bake that role into the interface — show the AI's "persona," its scope, its limitations — rather than expecting the user to prompt their way to that understanding.

## The Unknown Unknowns Problem

In "Putting Knowledge in Its Place," she identifies a specific failure mode in AI interfaces: users cannot ask about what they do not know they should ask about. "Unknown unknowns are hard to stumble on when you're only given the information you explicitly ask for." A chatbot response to a question about Svelte transitions might answer perfectly without revealing that there are four other types of Svelte transitions the user has never heard of. The chatbot answers what was asked; it cannot surface what was not asked.

This has direct implications for customer journey design: if your product relies on AI to help users discover your value, a chatbot-only interface will systematically fail users who do not know what to ask for. The journey must be designed to surface what users do not know they need.

## Trust and Appropriate Skepticism

Wattenberger flags the trust problem directly in "Why Chatbots Are Not the Future": chatbots are "endlessly confident" even when wrong. Users cannot tell whether the AI understood their question or where its information came from. This creates a failure mode where users either over-trust (accept incorrect output) or under-trust (dismiss useful output) — neither of which is what good AI-assisted work looks like.

Her implicit prescription for customer journey design: show users enough about how the AI reached its answer that they can calibrate their trust appropriately. Do not let the AI's confident prose style become a false signal of reliability. This is particularly important in early stages of the customer relationship, before users have developed a working sense of the AI's actual capability and failure modes.
