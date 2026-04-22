# Amelia Wattenberger — On Frontend Engineering

## Interactive Visualisation Engineering

Wattenberger's frontend engineering is specialised in interactive data visualisation: transforming data into visual representations that users can explore, manipulate, and understand. The engineering stack she works in is SVG and Canvas with D3.js for data binding and React for component structure. The engineering discipline is performance: a visualisation that drops frames on interaction has failed its primary purpose.

The frontend engineering requirements for interactive visualisation: compute expensive operations (scales, projections, path generation) outside the render cycle and cache them. Use `requestAnimationFrame` for smooth animation. Prefer Canvas over SVG for large datasets (thousands of elements). Use WebGL for datasets that exceed Canvas performance.

## Ghost Text and Inline AI Engineering

Wattenberger has written about the engineering of inline AI suggestions — the "ghost text" pattern that GitHub Copilot made standard. The engineering requirements are stringent: the suggestion must appear within 150ms of the trigger (beyond which it feels laggy), must not disrupt the user's cursor position or selection, must be dismissible without the user lifting their hands from the keyboard, and must update or cancel when the user continues typing.

The frontend engineering challenge: streaming completions from an LLM must be rendered incrementally, cancellation must abort the network request, and the UI state machine must handle the cases where a suggestion arrives after the user has already continued typing.

## The Ladder of Abstraction in Frontend Architecture

Wattenberger's "climbing the ladder of abstraction" principle has frontend implications: a well-designed frontend allows users to see their data at multiple levels of detail and move between them fluidly. The engineering of this requires that each level of abstraction is pre-computed or fast to compute on demand, and that the transitions between levels are animated to preserve spatial context.

The frontend engineering pattern: use `zoom` and `pan` interactions with smooth transitions, not page navigation, to move between abstraction levels. Navigation breaks the spatial memory that allows users to orient themselves.

## Sensory Richness as a Frontend Engineering Goal

Wattenberger has written about designing for "sensory richness" in AI interfaces — the observation that pure text responses from AI systems feel impoverished compared to richly formatted, structured, and visualised information. The frontend engineering investment is in rendering a wider range of output types: tables, charts, code with syntax highlighting, mathematical notation, timelines.

The frontend engineering discipline: define the output types your AI system can produce, and engineer the rendering for each type to a high standard. A table that renders as a plain text grid is worse than no table; a table that renders with sorting, filtering, and correct column alignment is a genuine improvement over prose.

## Accessibility in Interactive Frontends

Wattenberger's interactive essays are built with keyboard navigation and screen reader support. For visualisations — which are inherently visual — this requires engineering text alternatives to visual encodings, keyboard navigation through data points, and ARIA labels that describe the visual information.

The frontend engineering standard: every interactive element must be reachable and operable via keyboard. Every visual encoding of data must have a text alternative. Test with VoiceOver and keyboard-only navigation before shipping.

## Sources
- [wattenberger.com — Amelia Wattenberger's writing and projects](https://wattenberger.com/)
- ["Climbing the Ladder of Abstraction" — wattenberger.com](https://wattenberger.com/blog/climbing-the-ladder-of-abstraction)
- ["Pushing ChatGPT's Limits" — wattenberger.com](https://wattenberger.com/blog/pushing-chatgpt)
- [The Pudding — interactive essays](https://pudding.cool/)
