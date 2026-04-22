# Mattt Thompson — On Architecture

## Protocol-Oriented Architecture

Thompson's architectural approach in Swift is protocol-oriented: define behaviour through protocols, not class hierarchies. The architecture of a well-designed Swift system is a set of protocols that define what each component must be able to do, and a set of types that conform to those protocols. The protocols are the architecture; the implementations are the details.

The architectural advantage of protocols: they define a minimal interface between components. A component that depends on a protocol rather than a concrete type depends only on the defined behaviour, not the implementation. Replacing one implementation with another — for testing, for performance, for different platforms — requires only a new conformance.

## Documentation as the Architectural Specification

Thompson's engineering practice treats documentation as the canonical expression of architectural intent. Before an API is built, it should be documentable: if you cannot write a clear explanation of what the API does, why it exists, and how to use it, the API is not yet well-designed. The documentation is not downstream of the design — it is part of the design process.

The architectural discipline: write the documentation for a module before writing the implementation. If the documentation is confusing, the architecture is confusing. Simplify the architecture until the documentation is clear.

## The Cost of Abstraction in iOS Architecture

Thompson is careful about abstraction layers in iOS development. Every layer of abstraction between application code and the framework layer adds cognitive overhead for the engineer reading the code. The question before adding an abstraction is: does this abstraction genuinely reduce complexity for callers, or does it reduce lines of code for the author while adding layers that obscure what is actually happening?

His architectural rule: add abstraction only when the abstraction has a clearer mental model than the thing it abstracts. A networking abstraction that maps directly to URLSession's mental model of requests, responses, and sessions is useful. An abstraction that hides URLSession's mental model behind a different one is not.

## Small, Composable Components

Thompson's work consistently favours small, self-contained components that do one thing well. AFNetworking was not a large framework that covered all networking needs — it was a focused addition to NSURLConnection that addressed specific weaknesses. NSHipster's tutorials consistently present focused, understandable examples rather than comprehensive frameworks.

The architectural principle: prefer a collection of small, well-understood components over a large, comprehensive framework. Small components can be understood in isolation, replaced when they become inadequate, and composed in ways their authors did not anticipate.

## Understanding Before Abstracting

Thompson's consistent editorial position at NSHipster is: understand the framework before you abstract over it. AFNetworking was written by someone who deeply understood the URL loading system. The abstractions it provides are meaningful because they are grounded in genuine understanding of what is being abstracted.

The architectural warning: engineers who abstract before understanding produce abstractions that are wrong in subtle ways — ways that become apparent only when the abstraction is used in edge cases or when the underlying framework changes.

## Sources
- [NSHipster — nshipster.com](https://nshipster.com/)
- [AFNetworking — GitHub](https://github.com/AFNetworking/AFNetworking)
- [Swift API Design Guidelines](https://swift.org/documentation/api-design-guidelines/)
- [Protocol-Oriented Programming in Swift — WWDC 2015](https://developer.apple.com/videos/play/wwdc2015/408/)
