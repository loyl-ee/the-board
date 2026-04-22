# Jordan Singer — On Frontend Engineering

## Design Systems as Frontend Architecture

Singer's frontend engineering is inseparable from design systems. A design system is not a style guide — it is a shared vocabulary of components with defined behaviours, states, and variants that developers and designers both use to build consistent interfaces. The engineering discipline of a design system is maintaining that vocabulary: every component is documented, every variant is specified, and every consumer of the system is notified when the component changes.

The frontend engineering discipline: design system components should encapsulate their own state management, accessibility, and responsive behaviour. A button component that requires callers to implement its focus state, hover state, and disabled state is not a design system component — it is a set of styles with aspirations.

## AI-Native Frontend Patterns

Singer's work on Mainframe explores what frontends look like when AI is a first-class architectural component. The engineering patterns are different from traditional frontends: components must handle streaming text, must have affordances for editing AI-generated content, must show uncertainty (when the AI is not confident), and must handle latency gracefully (AI responses take longer than database queries).

The frontend engineering requirements for AI-native interfaces: streaming text must be rendered progressively, not all-at-once on completion. Skeletons or loading states must be proportional to expected response length. Edit affordances must be visible on AI-generated content by default.

## Figma Plugin Frontend Engineering

Singer's Figma plugin work demonstrates the engineering of a constrained frontend environment: Figma plugins run in a sandboxed iframe, have limited access to the host application, and communicate via message passing. The frontend engineering discipline for plugin development is understanding the API surface provided by the host and working within it effectively.

The broader lesson: constrained environments (iframe sandboxes, WebExtensions, Electron renderers) require understanding the specific capabilities and limitations before designing the frontend. Features that depend on capabilities the environment does not provide cannot be shipped.

## Rapid Prototyping Frontend Engineering

Singer is known for shipping prototypes rapidly. His frontend engineering approach: use existing design system components where they exist, write inline styles rather than separate style files for prototypes (reduces the number of files to context-switch between), and deploy immediately to get feedback before investing in production architecture.

The frontend engineering discipline: prototypes and production code are different artefacts with different standards. A prototype demonstrates a concept; production code implements it reliably. The mistake is applying production engineering standards to prototypes (too slow) or shipping prototype code as production (too fragile).

## Component Composability as the Primary Frontend Metric

Singer evaluates frontend components by their composability: can the component be used in contexts its author did not anticipate? A composable component receives its content and behaviour through props, not through hardcoded assumptions. A non-composable component assumes a specific context and breaks when used elsewhere.

The frontend engineering standard: write components that are agnostic about where they are used. Data should come from props, not from global state or direct API calls inside the component. Side effects should be explicit, not hidden.

## Sources
- [prol.page — Jordan Singer's website](https://prol.page/)
- [Mainframe — mainframe.so](https://mainframe.so/)
- [Diagram — diagram.com](https://diagram.com/)
- [@jsngr on Twitter/X — design system and frontend discussions](https://twitter.com/jsngr)
