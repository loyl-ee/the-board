# Amelia Wattenberger — On Product

## The Ghost Text Pattern and What It Got Right

The inline "ghost text" suggestion pattern — where Copilot's proposed code appears as faded gray text that developers accept with Tab or ignore by continuing to type — is the defining UI innovation of the AI coding era. Wattenberger was part of the GitHub Next team that developed and shipped this pattern. Its genius is in what it avoids: it does not interrupt the developer, does not require switching to a chat window, does not demand that the user formulate a question. The developer stays in flow. The AI's contribution is visible but unobtrusive. The evaluation of the suggestion requires no additional cognitive mode — you either accept it or you don't.

This is a product decision with deep implications. It answers Wattenberger's critique of chatbots before she articulated it publicly: there is no forced implementation-evaluation loop break, no isolated response, no blank-prompt anxiety. The context is already in the code; the response appears inline; the working buffer is the file itself.

## Code Brushes: Tactile Metaphor as Product Feature

Her Code Brushes project asked: "how could we make editing your code feel as tactile and easy as painting with a brush in Photoshop?" The framing is instructive. Instead of asking "how should the AI modify code," she asked "what physical metaphor makes this feel natural?" Brushes — debug, clean, document, add types — are pre-scoped, named, and reversible. They give the developer control (you choose which brush) while the AI handles execution.

This product instinct — reach for the right metaphor before specifying the mechanism — is core to her approach. A good metaphor creates affordances; it tells the user what the tool can and cannot do without documentation.

## Intent: Designing for the Multi-Agent Era

At Augment Code, she designed Intent — a workspace for orchestrating multiple AI coding agents simultaneously. The design insight is: as AI agents get better at writing code, the developer's job shifts from writing to directing. The bottleneck is no longer "can I type this code?" but "can I coordinate these agents without losing track of what they're doing?"

Intent's design response: isolated workspaces (each backed by a git worktree), a living specification that evolves as the work evolves, coordinated agents with shared context (Coordinator, Implementer, Verifier roles), and full git integration from prompt to merged PR. The product treats the specification as the primary artifact — not the code. This is a meaningful product philosophy: in an agentic world, the human's contribution is intent and judgment, not implementation.

## AI Should Show Its Work

A consistent thread in Wattenberger's product thinking is that AI outputs should not be presented as atomic facts. In "Putting Knowledge in Its Place" (wattenberger.com), she argues that couching AI-generated responses in larger frameworks and related context leads to much richer, stronger understanding. The chatbot answer to "what is condensation?" is technically correct but contextually impoverished — you learn the fact but not where it sits in the landscape of knowledge.

For product, this means: show the context. Show the distribution. Show where this answer falls relative to other answers. Show the uncertainty. The Financial Times model of embedding charts in reporting — grounding factual claims in visual data — is her exemplar. AI products that present outputs as authoritative, isolated statements are missing an opportunity to help users think better.

## The Role Shift: From Implementation to Orchestration

In her Refactoring podcast appearance (2026), she articulated what may be her sharpest product observation: "Every single pixel in the IDE is devoted to reading and understanding code. And it feels like as agents get better at the nitty-gritty, our role as developers has changed, where we're working more at higher levels of abstraction, where we have more leverage." This is a product thesis: the IDE as currently designed is optimized for the wrong task. The next generation of developer tools must be designed for intent, planning, and coordination — not code reading and comprehension.
