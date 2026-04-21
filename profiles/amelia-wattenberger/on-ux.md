# Amelia Wattenberger — On UX

## The Defining Problem of AI UX

Wattenberger's central UX argument is that the AI industry has defaulted to the wrong interaction paradigm. The blank chat box — familiar from messaging apps, inherited from command-line interfaces — is being used as the universal interface for AI because it is easy to build, not because it is good for users. She has made this argument most explicitly in "Why Chatbots Are Not the Future of Interfaces" (wattenberger.com, 2023), and it has shaped everything she has built since.

## The Four Chatbot Failures

She identifies four structural UX failures in chat interfaces:

**Affordances.** A text input provides no signal about how to use it well. "The interface looks the same as a Google search box, a login form, and a credit card field." Users must discover effective prompting through costly trial and error.

**Context must be typed, not embedded.** Every useful chatbot prompt contains layers of context — the AI's role, the task's structure, the desired output format, the user's background. These could be embedded as interface controls (dropdowns, sliders, pre-filled templates). Instead, users must type them from scratch every time, or lose them entirely between sessions.

**Responses are isolated.** There is no persistent working buffer. Comparing two outputs requires scrolling. Iterating requires re-reading. Creative work — which requires holding multiple possibilities simultaneously and choosing between them — becomes nearly impossible.

**The implementation-evaluation loop is severed.** Good tools let the user control when to shift between doing and assessing. Chat forces constant switching: type a prompt, read the response, type another prompt, read again. This breaks the concentration states — flow, deep focus — where the best work happens.

## The Ghost Text Solution

The Copilot ghost text pattern is her implicit answer to these failures. It preserves the developer's primary modality (writing code), makes AI suggestions visible without interrupting, allows immediate evaluation with zero additional input (accept or keep typing), and maintains the working buffer (the file). It embeds the interface affordance in the context where work is happening, rather than relocating the user to a chat window.

Her Code Brushes extension extends this philosophy into code editing: named, pre-scoped actions (debug, clean, document, add types) that the developer selects and applies directly to selected code. The AI action is anchored to the specific artifact being worked on. There is no prompt anxiety, no context-typing burden, no isolation of the result.

## New Patterns That Do Not Exist Yet

Wattenberger is explicit that AI UX requires genuinely new interaction patterns — not existing patterns extended with an AI backend. In her framework, the key design questions are:

- What level of abstraction does this user need right now, and can they move up or down easily?
- What context is the user forced to type that could be embedded in the interface instead?
- Is there a working buffer that persists and can be refined iteratively?
- Does the user remain in their primary work modality, or are they forced to switch to a chat paradigm?
- Is the AI augmenting human decision-making or replacing it in a way that leaves the human nominally responsible without being genuinely in control?

## The Human-AI Collaboration Interface

Her Intent product (Augment Code, 2026) represents her most complete answer to what AI-native UX looks like at scale. The design centers on the specification — a living document that captures intent — as the primary artifact of human contribution. Humans write specs; agents implement them. The interface is organized around managing multiple parallel agents, reviewing their work, and iterating on the spec — not around writing code line by line.

This is a UX paradigm shift: the developer's primary interaction is with their own articulated intent, not with code. The code is a byproduct. The agent is a collaborator executing that intent. The UX question becomes: how do you help a person articulate, refine, and communicate intent clearly? That is a completely different UX problem than "how do you help a person write good code?"

## Showing Context, Not Just Answers

In "Putting Knowledge in Its Place" (wattenberger.com), she extends her UX thinking to information retrieval: AI interfaces should provide the answer AND show where the answer fits. Wikipedia does this better than a chatbot — it shows you a fact in the context of related facts, related categories, related people. She calls for "couching AI-generated responses in larger frameworks and related context" because this produces "much richer, stronger understanding."

The UX principle: users should always know where they are in the landscape of knowledge, not just what the AI found at one specific coordinate.

## Sensory Richness as UX Principle

"Our Interfaces Have Lost Their Senses" (wattenberger.com, 2025) frames UX as a sensory design problem. Modern AI interfaces — particularly chatbots — strip away the texture of interaction: there is no spatial organization, no sound, no haptics, no visual richness. The result is an interaction that feels like "pointing a flashlight at a dark room for a second at a time." She advocates for interfaces that support multiple simultaneous input and output modalities, that respond to ambient context, and that let people collaborate on tangible artifacts rather than exchanging text strings.

## What She Would Tell You About Your AI UX

Invoke Wattenberger when you need to pressure-test any AI interface decision. Her questions: Does this interface tell users how to use it and how NOT to use it? Is there context the user is typing that could be embedded? Is there a working buffer? Is the user remaining in their primary work context or being relocated? Is the human in genuine control or nominal control? Is the AI output shown in its context or isolated? These are the questions that distinguish thoughtful AI UX from the default chatbox.
