# Amelia Wattenberger — On Engineering

## Interface Engineering for Human-AI Collaboration

Wattenberger's engineering work sits at the boundary between data visualisation, interaction design, and AI. Her essays and projects demonstrate a specific engineering discipline: building interfaces that make complex information learnable and that integrate AI as a collaborative partner rather than a black box. GitHub Copilot's ghost text — the inline code suggestion that appears as you type — is the most widely deployed expression of this interface engineering approach.

The engineering principle behind ghost text: AI assistance should appear at the moment of need, require zero UI overhead to dismiss, and provide immediate value without interrupting the user's flow. The implementation requires precise engineering of the suggestion trigger, latency management (the suggestion must appear fast enough to feel responsive), and careful attention to when *not* to suggest.

## Climbing the Ladder of Abstraction

Wattenberger's essay "Climbing the Ladder of Abstraction" documents the engineering pattern of building interfaces at multiple levels of detail — from individual data points to high-level summaries — and allowing users to move fluidly between levels. The engineering challenge is building the connections between levels such that zooming in and out feels natural rather than disorienting.

For AI systems, the ladder of abstraction is explicit: the model operates on tokens, the interface shows sentences, the user thinks in concepts. Good AI interface engineering spans all three levels without requiring the user to think about the lower ones.

## Canvas and Interactive Essay Engineering

Wattenberger's work at The Pudding and on her personal site demonstrates the engineering of interactive explanations — pieces where the user's interaction with data is the explanation, not an add-on to it. These require engineering at the intersection of data pipeline, SVG/Canvas rendering, and interaction design.

The engineering discipline: interactive explanations require the data to be clean, fast to compute, and responsive to user input. A visualisation that takes 500ms to update on hover has failed. The engineering standard is that interaction should feel immediate.

## Context Window Engineering

Wattenberger has written about the engineering challenges of AI context management — specifically, how to present a large context window to users in a way that makes it transparent and controllable. Her argument: users need to understand what the AI "knows" in order to collaborate with it effectively. An AI that has access to your entire codebase but shows no signal about what it is attending to is a black box.

The engineering implication: build context transparency into your AI interface from the start. Show users what documents, files, or history the model is drawing on. Allow them to add and remove context explicitly. This is not just a UX concern — it is an engineering requirement for trustworthy AI systems.

## Accessibility-First Data Engineering

Wattenberger's interactive pieces consistently handle screen reader access, keyboard navigation, and colour contrast — not as post-hoc additions but as architectural requirements. For data visualisation specifically, this means engineering text alternatives to visual encodings and ensuring that the interactive affordances work without a mouse.

The engineering discipline: accessibility requirements must be specified before implementation, because retrofitting them onto existing interactions is costly and often incomplete.

## Sources
- [Amelia Wattenberger — amelia.developer](https://wattenberger.com/)
- ["Climbing the Ladder of Abstraction" — wattenberger.com](https://wattenberger.com/blog/climbing-the-ladder-of-abstraction)
- ["Pushing ChatGPT's Limits" — wattenberger.com](https://wattenberger.com/blog/pushing-chatgpt)
- [The Pudding — pudding.cool](https://pudding.cool/)
- [GitHub Copilot research — GitHub Blog](https://github.blog/2023-07-25-github-copilot-research-quantifying-the-impact-on-developer-productivity-and-happiness/)
