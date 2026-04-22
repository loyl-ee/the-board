# Procreate / Savage Interactive — On Engineering

## GPU-Accelerated Canvas Engineering

Procreate's core engineering achievement is its drawing engine — a Metal-based GPU-accelerated canvas that renders brush strokes at 120fps on ProMotion displays with sub-millisecond latency. This is not an incremental improvement on existing drawing engines; it required building a custom rendering pipeline that uses the GPU for every step of stroke rasterisation, compositing, and display output.

The engineering discipline behind Procreate's performance: profile first, optimise second. The team measured exactly where time was being spent in the drawing pipeline and invested engineering effort proportionally. The result is a rendering architecture that saturates the GPU efficiently while keeping the CPU available for UI and file operations.

## Metal as the Right Abstraction Level

Procreate uses Metal directly — not through intermediate rendering frameworks — because the highest performance and lowest latency require direct control over the GPU pipeline. This is a deliberate trade-off: Metal is harder to program than higher-level frameworks, requires more platform-specific knowledge, and produces code that does not port to non-Apple platforms.

The engineering principle: choose the abstraction level appropriate to your performance requirements. For most applications, high-level frameworks are the right choice because they reduce engineering complexity. For an application where rendering performance is the product, the lower abstraction level is the right choice.

## Privacy-First Architecture: No Data Leaves the Device

Procreate collects no telemetry, sends no usage data, and has no analytics SDK. The canvas rendering, brush engine, and file operations are entirely local. The engineering architecture reflects this: there is no network layer in the drawing pipeline, no background sync process, and no tracking infrastructure.

The engineering argument is both ethical and practical. Ethically: an artist's work should not be transmitted to a remote server without explicit consent. Practically: a local-only architecture is simpler, more reliable (no network dependency), and eliminates an entire class of security vulnerabilities.

## One-Time Purchase as a Technical Architecture

Procreate's one-time purchase model has direct engineering implications. Without subscription revenue, the team cannot invest in recurring server infrastructure, cloud features, or online services that require ongoing operational costs. The architecture must be sustainable as a local application.

This constraint has produced engineering discipline: every feature must justify its engineering cost through the value it adds to a paid-once product. Features that require ongoing server costs are incompatible with the model. The engineering team has learned to build powerful capabilities within local computation rather than offloading to the cloud.

## Solo Engineering Ownership

Procreate is built by a small team in Hobart, Tasmania — small by the standards of a market-leading creative application. The engineering culture reflects this: each component is owned by an individual engineer who understands it deeply, rather than being distributed across a large team with diffuse responsibility.

The engineering benefit of small team ownership: fewer coordination costs, clearer accountability, faster debugging (the person who wrote the code is the person who fixes the bug), and a shared understanding of the full system that large teams lose.

## Sources
- [Procreate — procreate.com](https://procreate.com/)
- [Procreate statement on generative AI — August 2023](https://procreate.com/ai)
- [Procreate engineering blog — various](https://procreate.com/news)
- Savage Interactive WWDC design award acceptance (multiple years)
