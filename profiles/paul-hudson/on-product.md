# Paul Hudson — On Product

## Educational Products as Structured Experiences

Paul Hudson's approach to educational product design is shaped by a single guiding question: what does a learner need at each point in their journey, and in what order? His products are not reference manuals or topic dumps — they are sequences, carefully staged to build confidence and competence simultaneously.

The best example is the 100 Days challenges. These are not simply 100 days of tutorials packaged together. They are a product with rules, accountability mechanisms, pacing, consolidation periods, and community architecture. The design decisions are deliberate:

- **One hour per day** — a commitment that is achievable without disrupting a life, but consistent enough to build a real habit
- **Daily public posts** — accountability through social visibility, which makes progress tangible and creates peer community without Hudson having to moderate it
- **Consolidation days** — spaced throughout the 100 days to let learned material settle and give learners who fell behind a way to catch up without abandoning the course
- **No lone-wolf rule** — Hudson explicitly discourages learners from treating the challenge as a solitary activity, directing them to ask questions, post publicly, and engage with the community

The 100 Days courses have been updated for new iOS versions (including a full iOS 17/SwiftData update announced in 2023) and remain free through every version. That maintenance commitment is itself a product decision: a course that decays becomes unusable and loses its ranking and reputation.

## Project-First Learning Architecture

Hudson's books and tutorials use a consistent structure: introduce a concept, then teach it by building a project that uses it. Every chapter in Hacking with iOS builds a complete, runnable app. SwiftUI by Example organizes over 600 pages of code by answering specific "how do I do X" questions with working code. Pro Swift advances techniques through demonstration in real Swift patterns.

This project-first architecture means learners end each session with something that works, not just knowledge they have absorbed. The psychological effect — seeing working code you wrote yourself — is a key part of the product experience.

## Progression Architecture: Beginner to Advanced

Hudson has constructed what amounts to a learning stack:

1. **100 Days of Swift / 100 Days of SwiftUI** — absolute beginners, zero to building apps
2. **Hacking with iOS / SwiftUI by Example** — intermediate, expanding the toolkit
3. **Pro Swift / Pro SwiftUI** — advanced language features and patterns
4. **Swift Design Patterns / Testing Swift / Swift Concurrency by Example** — professional-grade depth on specific domains
5. **Swift Career Accelerator** (Hacking with Swift+) — organized across five career stages, from entry-level to lead developer

Each product has a clear audience and entry point. There is no content that leaves learners wondering which resource they should be using at which stage. The catalogue functions as a curriculum even though it was built incrementally over a decade.

## The Unwrap App

Unwrap (free, no in-app purchases) is a mobile-first companion to the text and video tutorials — an app for learning Swift on your iPhone. It contains nearly 100 short video lessons, interactive reviews, code-writing activities, error-spotting exercises, and daily challenges. It was released as open source on GitHub, which is consistent with Hudson's philosophy that the tools for learning should not be gated.

The design of Unwrap reflects his understanding that not all learners sit at a desk — some learn during commutes or in short bursts. The app accommodates that context.

## Hacktivate: Teaching Security Through Play

In 2025 Hudson released Hacktivate, a capture-the-flag app with 240 missions where players hack servers, crack ciphers, and uncover hidden flags. This represents an extension of his pedagogical model into security education — learning real computer science skills through structured play rather than lectures or documentation.

## What Hudson Does Not Build

Hudson does not build products for non-Apple platforms, does not build enterprise training tools, and does not build tooling for teams. His product surface is deliberately personal and individual — one learner, one device, one journey. This is a constraint he has maintained consistently across his entire catalogue.

## Sources

- hackingwithswift.com/100/swiftui
- x.com/twostraws/status/1667194153489539072 (iOS 17 update, free, 2023)
- github.com/twostraws/Unwrap
- hackingwithswift.com/plus/swift-career-accelerator
- x.com/twostraws/status/1980329586463502561 (Hacktivate launch, 2025)
