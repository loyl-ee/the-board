# On Product — Mattt Thompson

## APIs as Products

The most important insight Thompson brings to product thinking is the equivalence between API design and product design. AFNetworking was used by developers, not end users, but it was nonetheless a *product* — one with onboarding friction, learning curves, delight moments, and churn risk. Thompson's decade of work on AFNetworking and NSHipster is largely a sustained exploration of what it means to ship a good developer product.

His AFNetworking 2.0 redesign (September 2013) illustrates this product thinking in action. The core architectural decision — to separate previously bundled concerns (security, reachability, serialization) into distinct modules — was driven by a product insight: developers only needed parts of what the library offered, and forcing them to adopt everything created unnecessary overhead. The introduction of CocoaPods subspecs meant developers could take only what they needed, reducing bundle size and cognitive load. This is classic product minimalism applied to infrastructure.

## Developer Experience as a Product Concern

Thompson treats developer experience (DX) with the same rigor that consumer product designers apply to user experience. His NSHipster article on AFNetworking 2.0 emphasizes that the redesign was motivated by "ease-of-use and extensibility" simultaneously — the recognition that these goals are not opposed but that good product design finds the design space where they coexist.

His NSHipster article "Stewardship" argues that every user question is a product signal: "Each question is a data point for what could be clarified or improved." This positions documentation not as a support cost but as a product feedback loop — bad documentation surfaces as support burden, which signals where the API's design or naming failed to communicate its intent.

## Good Defaults as a Feature

Thompson's Principle of Least Surprise — "clear intent, reasonable defaults, and control" (NSHipster book) — is a product philosophy as much as a technical one. He argues consistently that an API should work correctly in the common case with zero configuration, while still exposing the full surface area for advanced use. This is the same principle behind good defaults in consumer product design: the product should do the right thing for a new user, and the expert user should be able to find the controls.

AFNetworking practiced this by making JSON request serialization the default behavior (the common case) while exposing serializer protocols for any other format. The developer who just needs HTTP JSON gets immediate value; the developer building a custom binary protocol can still use the same framework.

## Testing and Reliability as Features

Thompson's public writing treats testing as product quality, not process bureaucracy. His NSHipster article on `XCTestCase` and `XCTestExpectation` (July 2014) approaches testing tooling with the same depth and enthusiasm as any other framework — the implicit argument being that a developer who understands their testing tools deeply will write tests, and a developer who writes tests ships reliable products.

His emphasis on semantic versioning in "Stewardship" carries the same logic to dependency management: a library that breaks its API contract without a major version bump is a product that damages its users' reliability. Trustworthy versioning is itself a product feature.

## The Flight School Model: Dense Knowledge, Accessible Delivery

The Flight School book series represents Thompson's most explicit product design experiment. Each book is short enough to read over a weekend — a deliberate constraint. This is a product decision: the format signals that the content is worth the reader's time, that the author has done the work of distillation rather than padding. The series targets developers from non-CS backgrounds, addressing the gap between theoretical computer science concepts (floating-point arithmetic, Unicode encoding, serialization) and practical daily work. The product insight is that this gap creates real-world bugs and that accessible, honest treatment of the underlying concepts is more useful than both overly academic treatments and overly simplified blog posts.
