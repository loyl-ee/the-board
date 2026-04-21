# Chris Eidhof — On Safety

## Type Safety as a Form of Software Safety

Eidhof's most developed and consistent position on safety is about *type safety* — the use of Swift's type system to make invalid program states unrepresentable, and therefore to eliminate entire categories of runtime errors before the program runs.

His blog post "Types vs TDD" (chris.eidhof.nl) makes the foundational argument: "A type checker actually does testing for you." When a function declares a return type of `Int`, the compiler guarantees it will not return `nil`, a string, or a side-effecting action — without any test being written. Changing the return type to `Int?` then causes the compiler to surface every call site that now needs to handle the optionality, acting as an automated audit: "until you have reviewed every single call to `foo`, the program simply won't compile." He frames compiler errors during refactoring as "a todo-list, not as a speed bump."

This is safety as architecture, not safety as a post-hoc concern. The design question is not "how do we test for this bug?" but "how do we make this bug impossible?"

## Making Impossible States Impossible

The Swift Talk episode "Making Impossible States Impossible" (S01E153, May 2019, with Wouter Swierstra) develops this theme concretely. Foundation's `URLSession` completion handler takes three optional parameters (Data?, URLResponse?, Error?), creating eight theoretical combinations — but only a small subset of those combinations are semantically valid. The episode demonstrates how enums can collapse the valid space to precisely the states that can actually occur, eliminating the need to handle impossible combinations in application code.

The principle: "leverage the type system in such a way that our code precisely models the data of the domain we're working in." Safety here is achieved by making the type system's shape match the domain's shape.

This extends to API design. His UIKonf 2017 talk "Intermediate Types" with Florian Kugler shows how phantom types can enforce constraints at compile time — distinguishing horizontal from vertical Auto Layout anchors, for example, so that combining incompatible anchors is a type error rather than a runtime crash.

## Value Semantics as a Safety Guarantee

Eidhof's deep engagement with value semantics in Swift — structs, copy semantics, the `mutating` keyword — is also a safety argument. When data is represented by value types rather than reference types, mutation is local: "the mutation of the struct is a local side-effect, and only applies to the current struct variable." There is no implicit sharing, no action-at-a-distance, no race condition that stems from shared mutable state.

In "Struct Semantics in Swift," he quotes the safety benefit precisely: "if you read a line like `let point = ...`, and you know that `point` is a struct variable, then you also know that it will never, ever, change." This is a safety property with no runtime cost — it is enforced by the compiler at zero overhead.

## Honest Gaps on Broader Security

Eidhof has not written publicly about software security in the broader sense — network security, authentication, data privacy, threat modeling, or secure coding practices for consumer applications. His safety concerns are at the language and type system level, not the application security or cryptographic level. This is an honest and significant gap if the question involves security in the sense that end-users or security engineers understand it.

## The Ethics of Teaching Advanced Programming

Eidhof's teaching has an implicit ethical dimension: he consistently acknowledges the limits and trade-offs of the techniques he teaches. When he explores underscored SwiftUI APIs, he explicitly warns readers about the risks of App Store submission. When he discusses phantom types, he notes the trade-offs between type precision and API usability. When his functional view controllers experiment was incomplete, he said so.

This epistemic honesty in teaching is itself a form of safety — it prevents readers from over-applying techniques beyond their validated scope. Technical education that presents advanced patterns as universally applicable can cause real harm in production systems; Eidhof's habit of stating what a technique does and does not solve is a meaningful safeguard.
