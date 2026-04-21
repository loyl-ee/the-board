# Procreate & Savage Interactive — On Product

## The Valkyrie Engine: The Hidden Foundation

Procreate's defining competitive advantage is not its interface or its price — it is the custom graphics engine underneath. Savage Interactive built Valkyrie as a proprietary rendering layer on top of Apple's Metal framework, enabling real-time brush rendering at up to 120 frames per second on supported iPad Pro hardware. This matters because responsiveness in a drawing application is not a luxury feature; it is the experience. Latency between stylus movement and the mark appearing on screen breaks the physical illusion of drawing. Valkyrie was engineered to close that gap.

When Procreate 5 shipped the rebuilt Valkyrie engine (2019), the capability expansion was significant: the engine enabled Dual Brushes (combining two brushes into a single stroke), a full-screen Brush Studio with over 150 adjustable parameters per brush, a graphically accelerated texture generator, and simultaneous pressure and tilt sensitivity mapped to hundreds of individual brush variables. Notably, imported Adobe Photoshop brushes render faster in Procreate 5 than they do in Photoshop itself — a performance demonstration that is also a market positioning statement.

## The Brush Engine as Moat

Procreate's brush library and brush creation system represent the deepest layer of its competitive moat. The application ships with 190 brushes organized across 18 categories. Each brush can be customized across 10 categories of characteristics in the Brush Studio. Users can create entirely new brushes, combine two brushes into a Dual Brush, and import brushes designed for Adobe Photoshop. An independent ecosystem of third-party brush sets — sold by artists on platforms like Creative Market — has grown up around the format, effectively extending Procreate's capabilities through community creation.

The brush engine is also the most directly tactile expression of Procreate's product philosophy. The goal is not to provide a digital approximation of a physical medium — it is to create tools that respond so naturally to Apple Pencil pressure, tilt, and velocity that the physical/digital distinction loses relevance. Brushes can be configured so that pressing harder increases stroke width, tilting reduces opacity, or speed changes texture — behaviors that mirror the physics of real media while enabling things no physical brush can do.

## Progressive Capability Without Progressive Complexity

Procreate's product design solves a genuinely difficult problem: how to make a professional-grade tool that does not intimidate a beginner. The application gives 95% of screen space to the canvas. Advanced tools are hidden behind gestures, not cluttering the interface. The Brush Studio is accessible but not imposed. Layers can be ignored by casual users and used with full professional depth by others.

James Cuda has described the tension directly: "Making something simple is really complex. The beauty of the product is its accessibility." And: "We always want to add more functionality, but we don't want the app to become overburdened." Chief Product Officer Claire d'Este frames the underlying design question as: "How do we keep that simplicity and those low barriers — but still give everyone the power they need?"

The Quick Shape feature is the canonical internal example of this philosophy in practice. Users had been requesting physical drawing aids — rulers, protractors, guides — as additional UI elements. Savage's solution was a gesture: draw any shape, hold at the end, and the app recognizes the shape and snaps it to a perfect form. No UI added. The feature is more powerful than what users asked for, and it is discoverable through behavior rather than through a menu. As Cuda put it: "It's very intuitive, but it's not conventional." The feature took nearly three years of iteration to ship.

## Procreate Dreams: Expanding the Vision

Procreate Dreams (November 2023) is the most ambitious product Savage has shipped. The app was five years in development and represents a genuine rethinking of what 2D animation software can feel like on a touch device. Key innovations include:

- **Performing**: A real-time recording mode where gestures applied to the Stage (the canvas area) are automatically translated into keyframes. Users do not set easing curves; they perform movements and the system generates the animation data.
- **Multi-touch Timeline**: The timeline is navigated through touch gestures rather than mouse-driven scrubbing.
- **Real-time playback rendering**: No waiting for RAM previews. The Stage plays back in real time regardless of project complexity.
- **4K video compositing**: Dreams supports drawing over and rotoscoping 4K footage directly.

Procreate Dreams 2 (December 2025, free update) substantially deepened the professional offering: unlimited flipbook tracks with blend mode support, Selection and Transform tools in drawing mode, 180 new animation-specific brushes, advanced export including ProRes 4444 with alpha, and a redesigned timeline. The update addressed many of the feature gaps cited in early reviews.

## Product Discipline: What Savage Does Not Ship

A meaningful part of Procreate's product story is restraint. Savage does not ship subscription models. It does not ship cloud sync of artwork (privacy by design). It does not ship a desktop version. It does not ship generative AI tools. It does not ship features simply because users request them. The product team reads every suggestion thread, tags each one with a status (planned, in development, released), and openly acknowledges when requests are declined or deferred. The product roadmap is internally driven and shaped by a decade of accumulated judgment about what belongs in the tool — not by what is trending.

## Sources

- [MacStories: Procreate 5 Review](https://www.macstories.net/reviews/procreate-5-review-a-rebuilt-graphics-engine-drives-fantastic-animation-color-and-brush-tools-in-an-art-app-perfectly-tailored-to-the-ipad/)
- [Apple Developer: Behind the Design — Procreate](https://developer.apple.com/news/?id=e409h6ja)
- [Procreate: Dreams Reveal](https://procreate.com/insight/2023/procreate-dreams-reveal)
- [Creative Bloq: Procreate Dreams — bringing animation to everyone](https://www.creativebloq.com/features/procreate-dreams-interview)
- [Procreate About Ideas & Suggestions](https://procreate.com/about-ideas-suggestions)
- [Wikipedia: Procreate (software)](https://en.wikipedia.org/wiki/Procreate_(software))
