# Jordan Singer — On Engineering

## Design Systems as Engineering Infrastructure

Singer's engineering philosophy treats design systems not as style guides but as engineering infrastructure — the same category as a component library or a build tool. A design system done well encodes design decisions in code, making them reproducible, consistent, and reviewable. A design system done poorly is a PDF that developers ignore.

His work on Diagram and its AI-native design tools reflects this: the design system is not a separate artefact from the product — it is the product's implementation contract. When a component is changed in the design system, every instance in the product updates. The engineering discipline is maintaining that bidirectional relationship.

## AI-Native Interface Engineering

Singer's Mainframe project explores what applications look like when AI is a first-class architectural component, not a feature bolted onto an existing UI. The engineering implication of AI-native design: the data model, the interaction model, and the rendering model all need to account for AI outputs that are non-deterministic, latency-sensitive, and context-dependent.

Traditional UI engineering assumes that user actions produce deterministic state changes. AI-native engineering requires engineering for probabilistic outputs: streaming responses, confidence indicators, revision affordances, and graceful handling of AI failures.

## Fast Iteration as an Engineering Discipline

Singer is known for shipping prototypes rapidly — days, not weeks. His engineering approach to this speed: use the highest-leverage tools available (Figma for design, Swift for iOS, existing APIs for AI capabilities), build the minimum version that demonstrates the core idea, and learn from it before adding complexity.

The engineering philosophy behind fast iteration: most architectural decisions that seem fundamental at the start can be changed later. The cost of learning from a working prototype is almost always less than the cost of extended up-front design. Ship something, observe how it is used, then invest in the architecture.

## Figma Plugin Architecture as Engineering Reference

Singer's Figma plugin work demonstrates the engineering of extensibility systems: APIs that allow third-party developers to extend a host application's capabilities without access to the host's source code. The engineering requirements for a good plugin API are specific: it must be sandboxed, documented, stable across versions, and designed for the operations that plugin developers actually need.

The engineering lesson from Figma's plugin architecture: the best extensibility APIs are not the ones that expose the most surface area — they are the ones that enable the most valuable use cases with the smallest, most stable interface.

## Prototyping as Engineering Research

Singer treats rapid prototyping as engineering research: building something that works well enough to test a hypothesis, not building something meant to ship. The engineering discipline is knowing when a prototype has served its purpose and when to stop extending it versus starting fresh with a production architecture.

His public prototypes — posted to Twitter/X and his website — are explicitly framed as experiments. They demonstrate capabilities and design directions, not production-quality implementations. This framing allows him to share work early without creating expectations that the code is maintainable or extensible.

## Sources
- [Jordan Singer — prol.page](https://prol.page/)
- [Mainframe — mainframe.so](https://mainframe.so/)
- [Diagram — diagram.com](https://diagram.com/)
- [@jsngr on Twitter/X](https://twitter.com/jsngr)
- [Figma Plugin API documentation — figma.com](https://www.figma.com/plugin-docs/)
