# Chris Eidhof — Philosophy

## Functional Programming as a Practical Tool, Not an Ideology

Eidhof's most distinctive philosophical position is that functional programming is a *toolkit*, not a religion. Having learned Haskell at Utrecht University and worked extensively in it before switching to iOS development, he arrived at Swift with deeper functional knowledge than most Apple platform developers — but he has consistently resisted using that knowledge to evangelize pure FP ideology.

His book *Functional Swift* (co-authored with Florian Kugler and Wouter Swierstra) frames the argument directly: the goal is to use functional concepts "in a pragmatic way, in order to write clearer and more expressive code." The book does not advocate for pure functional style. It advocates for understanding functions-as-values, careful type selection, and composability — and then applying those ideas where they genuinely help, not everywhere.

In a 2014 blog post, Eidhof summarized the core insight: "Functional programming can be like that: making certain programs smaller by a huge factor." The emphasis is on *certain programs* — he is precise about the scope of the claim.

## Types as Documentation and Compiler Assistance

Eidhof has a deep and consistent belief that well-chosen types communicate intent better than comments and enforce constraints better than tests. This thread runs through everything he has published.

In "Types vs TDD" (chris.eidhof.nl), he argues that type systems perform a form of automated testing: "A type checker actually does testing for you." He describes compiler errors during refactoring not as obstacles but as useful direction: "a todo-list, not as a speed bump." Change a return type, and the compiler surfaces every call site that now needs attention — a mechanical checklist no test suite provides automatically.

This extends to API design. His post on Swift analytics walks through multiple ways to model an analytics API — from thin function wrappers to enum-based deep embeddings — treating each design choice as a statement about what the type system should enforce and what it should leave to runtime. The principle: "choose the simplest possible solution for your problem and team," and let the types say as much as they can.

His UIKonf 2017 talk with Florian Kugler, "Intermediate Types," explored how phantom types and precise type modeling can eliminate entire classes of bugs by making invalid states unrepresentable. The Swift Talk episode "Making Impossible States Impossible" (S01E153) develops this theme directly: the goal is to "leverage the type system in such a way that our code precisely models the data of the domain we're working in."

## Making the Compiler Your Ally

Eidhof treats the Swift compiler as a collaborator rather than a gatekeeper. In his blog post on protocols, he identifies that conforming to `Collection` requires much less than it appears — the compiler's requirements reduce to four items once default implementations are accounted for. His response to this complexity is not frustration but a call for better tooling: automated protocol introspection so developers can work *with* the compiler more fluently.

In "Struct Semantics in Swift," he argues for value types precisely because the compiler enforces their immutability guarantees: "if you read a line like `let point = ...`, and you know that `point` is a struct variable, then you also know that it will never, ever, change." The compiler becomes a proof assistant — a lightweight form of formal verification available to every developer.

## Understanding Fundamentals Before Reaching for Frameworks

A recurring theme in Eidhof's work is the value of building things from scratch to understand them deeply. Swift Talk builds parsers, layout systems, routing libraries, and form frameworks from first principles — not because external libraries don't exist, but because understanding the implementation gives developers better instincts for using anything that builds on the same ideas.

*Functional Swift* includes examples like a type-safe Core Image wrapper, a diagrams library built on Core Graphics, and a small spreadsheet from scratch. The choice is intentional: these examples force readers to confront the underlying mechanics, not just the API surface.

His 2024 SwiftUI Field Guide took this further: to build interactive explanations of SwiftUI's layout algorithm, he re-implemented key portions of SwiftUI in TypeScript. The exercise deepened his own mental model and produced better teaching material. In his 2024 review, he noted that the learning from teaching workshops was mutual: "The learning has been tremendous from all sides."

## Simplicity Through Constraints

Eidhof is drawn to small, well-understood systems. He believes constraints produce clarity. The objc.io monthly issues format was strict — one topic, multiple expert perspectives, one month. The Swift Talk format is strict — one problem, live code, under 30 minutes. His workshops follow a fixed structure with pair exercises and group discussion.

This preference for constraints extends to software design. In his analytics post, he argues for matching solution complexity to actual requirements rather than defaulting to elaborate abstractions. The principle he articulates — start simple, add complexity only as forced — is itself a kind of constraint: a policy against premature sophistication.

## Honest About Limits

Eidhof is notable for acknowledging the edges of his claims. His post on phantom types cautions that there are trade-offs between type preciseness and usability. In his functional view controllers work, he called the implementation "still very much work in progress" and acknowledged open challenges. On variadic views in SwiftUI, he explicitly warned against shipping with underscored APIs: "I don't know whether this API is going to change in the future, whether it's App-Store-proof, and so on."

This intellectual honesty — stating what a technique does and does not solve — is part of what makes his work authoritative rather than promotional.
