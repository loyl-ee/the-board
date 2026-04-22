# Mattt Thompson — On Engineering

## Documentation Is Part of the Implementation

Thompson's foundational engineering principle is that documentation is not downstream of code — it is concurrent with it. NSHipster, his long-running reference site for iOS and macOS development, is built on the premise that understanding an API deeply enough to explain it clearly is itself a form of mastery. Writing documentation forces you to confront the gaps in your own understanding that working code can conceal.

His "perfect commit" philosophy (independently parallel to Simon Willison's formulation) holds that a commit is not complete until it includes the implementation, the tests, updated documentation, and a link to the relevant issue thread. Shipping code without documentation is not finishing — it is deferring a cost that grows as the team grows.

## API Design as the Primary Concern

Thompson approaches software engineering with the view that the API is the most important design decision, and the implementation is secondary. A well-designed API is self-documenting: the names of types, methods, and parameters should tell the caller exactly what to expect. A poor API is one where callers need to read the implementation to understand the contract.

He has written about Objective-C and Swift API design principles extensively: methods should read as sentences, parameter labels should clarify the role not the type, return values should be predictable. He was an early and vocal advocate for the Swift API Design Guidelines, which codified many of these principles into language conventions.

## Understand Before Using

Thompson argues consistently against cargo-culting libraries and frameworks without understanding what they do. NSHipster's entire editorial stance is: before you use `NSDateFormatter`, understand `NSDateFormatter`. The articles typically explain the internals, the edge cases, the historical context, and the common mistakes — because shallow understanding leads to subtle bugs.

This principle applies to his own libraries. AFNetworking was designed to be readable, not just usable. The assumption was that engineers would read the source, and the source should teach them something about the URL loading system, threading, and HTTP semantics.

## Protocol-Oriented Design

Thompson was an early adopter of Swift and an advocate for protocol-oriented programming before Apple made it a formal part of the language. His position: define behaviour through protocols, not class hierarchies. Protocols compose; inheritance trees lock you in. A type that conforms to a protocol makes an explicit, auditable contract with its callers.

This approach produces smaller, better-bounded components. Each protocol defines a single capability. A type can conform to many protocols without inheriting state or implementation it doesn't need. Testing becomes straightforward: create a mock conformance to the protocol.

## The Cost of Abstraction

Thompson is careful about abstractions that obscure the platform. Apple's frameworks are themselves a careful set of abstractions over system calls and hardware, and adding another layer on top of those abstractions compounds the cognitive overhead. His rule: add an abstraction only when it genuinely reduces complexity for callers — not when it reduces lines of code for the author.

He has been sceptical of frameworks that wrap Foundation or UIKit completely, arguing that engineers who rely on them lose the ability to debug at the layer beneath. When the abstraction breaks — and it will break — you need to understand what is underneath.

## Sources
- [NSHipster](https://nshipster.com/)
- [Swift API Design Guidelines](https://swift.org/documentation/api-design-guidelines/)
- [AFNetworking — GitHub](https://github.com/AFNetworking/AFNetworking)
- [Protocol-Oriented Programming in Swift — WWDC 2015](https://developer.apple.com/videos/play/wwdc2015/408/)
