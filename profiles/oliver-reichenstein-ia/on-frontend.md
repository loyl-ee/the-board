# Oliver Reichenstein — On Frontend Engineering

## Typography Is Frontend Engineering

Reichenstein's foundational claim — "web design is 95% typography" — is a frontend engineering claim as much as a design claim. The engineering decisions of the frontend directly determine the typographic quality: font loading strategy (FOIT vs. FOUT), fallback fonts, OpenType feature support, text rendering settings (`text-rendering: optimizeLegibility`), line height inheritance, and rem vs. em units for responsive scaling.

A frontend that renders beautiful typography in optimal conditions but flickers on load, uses system fonts that don't match the design, or breaks at non-standard viewport sizes has failed typographically. Typography is not set once in a Figma file — it is engineered into the CSS and maintained across browser updates.

## HTML First, CSS Second, JavaScript Last

Reichenstein's product philosophy maps to a specific frontend architecture: HTML provides the semantic structure, CSS provides the visual expression, and JavaScript provides only the interactivity that HTML and CSS cannot express. This is progressive enhancement: the page works without JavaScript, works better with CSS, and works best with JavaScript.

The engineering discipline: before reaching for JavaScript, ask whether the interaction can be expressed in CSS (`:hover`, `:focus`, `details`/`summary`, CSS animations). Before reaching for CSS, ask whether the semantic HTML structure alone conveys the information correctly. The engineering quality of a frontend is measured in part by how much it achieves without JavaScript.

## Readable Line Lengths as a Constraint

iA Writer's line length is fixed: 68 characters per line on desktop. This is not an aesthetic preference — it is an engineering constraint derived from typographic research showing that optimal reading speed and comprehension occur at line lengths of 50-75 characters. The engineering implication for web frontends: max-width constraints on text containers are engineering requirements, not design constraints.

Frontend engineers who allow text lines to extend the full width of a widescreen monitor have not optimised for reading — they have optimised for filling space.

## Markdown Rendering as Engineering Craft

iA Writer's rendering of Markdown to HTML — and the precision of that rendering — is frontend engineering with editorial standards. Code fences must render correctly. Smart quotes must replace dumb quotes. Em dashes must be distinct from hyphens. The engineering of a Markdown renderer is the engineering of a reading environment: every character matters.

The frontend engineering standard for reading-focused products: test your typography at the character level, not just the layout level. Render your content and read it.

## Local Processing in the Frontend

iA Writer's Style Check and Syntax Highlight run entirely in the app — no content is sent to a server. For web frontends that need to process user content, the same principle applies: if the processing can be done in the browser (with WebAssembly, with the Web Speech API, with local ML models), doing so eliminates network latency, privacy risk, and offline unavailability.

The frontend engineering question: can this feature be computed locally? For processing text, often yes. Investing in client-side processing produces a faster, more private, and more reliable frontend.

## Sources
- ["Web Design is 95% Typography" — ia.net, 2006](https://ia.net/topics/the-web-is-all-about-typography-period)
- [iA Writer — ia.net](https://ia.net/writer)
- [iA Fonts — open source on GitHub](https://github.com/iaolo/iA-Fonts)
- ["Responsive Typography: The Basics" — ia.net, 2012](https://ia.net/topics/responsive-typography-the-basics)
