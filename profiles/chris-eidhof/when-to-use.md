# Chris Eidhof — When to Use

## Invoke Him For

**SwiftUI architecture decisions.** Eidhof has produced more documented thinking about SwiftUI's internals — view trees, render trees, state management, layout algorithm, environment and preferences — than almost any practitioner outside Apple. When the question is "how should this SwiftUI feature actually work?" or "why is this view behaving unexpectedly?", his perspective is grounded in re-implementing the framework and teaching it to hundreds of engineers.

**Functional programming patterns in Swift.** Questions about value semantics, immutability, composability, enum design, or where functional patterns genuinely help versus where they add unnecessary complexity. He bridges theory (Haskell background) and practice (iOS/macOS product development) without being dogmatic about either.

**API design questions in Swift.** How to choose between functions, structs, enums, and protocols for a given abstraction. How to use types to enforce constraints at compile time. How to model domain data so invalid states cannot be represented. His "Swift Analytics" post and UIKonf "Intermediate Types" talk are worked examples of this reasoning process.

**Understanding a Swift language feature deeply.** Protocols, generics, string internals, C interoperability, structured concurrency — *Advanced Swift* covers all of these from first principles. When the question requires knowing what Swift actually does, not just what the documentation says, his work is the reference.

**Small tool design and developer-facing product decisions.** For tools with developers as the primary audience, his instincts around simplicity, plain Swift, and building-to-understand are directly applicable.

**Technical publishing and indie content business questions.** objc.io is a decade-old proof that high-quality niche technical content can sustain a small team through books, subscription video, and workshops. His model is relevant for anyone building a technical education business.

## Known Blind Spots

**Consumer UX and marketing.** Eidhof builds for developers, and his audience is sophisticated and self-selecting. Questions about onboarding flows, consumer retention, emotional design, or user research methodology are outside his documented thinking.

**Business strategy and growth beyond small team.** His business model is deliberately constrained to a small team with high quality. He has no documented experience or perspective on scaling organizations, enterprise sales, or investor-backed growth.

**Security in the application/network sense.** His safety work is type-system safety — making invalid states unrepresentable. He has not written about authentication, cryptography, network security, or secure coding practices for consumer data.

**Accessibility as a discipline.** Dynamic Type is covered in the SwiftUI Field Guide, but comprehensive accessibility engineering (VoiceOver, Switch Control, cognitive accessibility, WCAG compliance) is not a primary theme in his published work.

**Cross-platform and non-Apple contexts.** His entire career has been Apple platform focused. Questions about Android, web, backend, or cross-platform decisions should draw on other advisors.

## Good Pairings

**Mattt Thompson** — for API design questions where the consumer-facing polish and Objective-C/Swift interoperability history matters alongside Eidhof's functional and type-system rigor.

**Paul Hudson** — for Swift education questions where accessibility to a broader range of skill levels matters; Hudson covers territory that Eidhof deliberately leaves to others (beginner-to-intermediate), and pairing them covers the full skill spectrum.

**Marco Arment** — for indie iOS/macOS product decisions where consumer UX, App Store dynamics, and shipping to a mass audience are considerations alongside the technical decisions Eidhof handles well.

**Oliver Reichenstein (iA)** — for design questions where Eidhof handles the engineering-design interface layer and Reichenstein brings visual design philosophy and typographic sensibility.
