# Chris Eidhof — On Architecture

## Functional Architecture: State at the Edges

Eidhof's architectural approach is functional: push side effects and mutable state to the edges of the system, and make the core logic pure functions. A pure function takes input, produces output, and has no side effects. Pure functions are easy to test, easy to reason about, and easy to compose. Side effects — network requests, database writes, UI updates — are isolated to specific layers.

The architectural pattern: a SwiftUI view is a function of state; the state is managed by an observable object that separates business logic from UI logic; the business logic is implemented as pure functions that can be tested without a UI or a simulator.

## Making Illegal States Unrepresentable in Architecture

At the architectural level, Eidhof's "make illegal states unrepresentable" principle means designing the data flow so that invalid system states cannot exist. If a user can be in only one authentication state at a time, the authentication state should be an enum, not a combination of booleans. If a network request can be in only one loading state at a time, the loading state should be an enum, not a combination of optionals.

The architectural discipline: when you find yourself writing code that checks whether a combination of state variables is valid, the architecture has not encoded the constraint properly. Redesign the data model to make the invalid combination impossible.

## Small, Replaceable Components

Eidhof advocates for architectures where each component is small enough to be understood completely by the engineer responsible for it, and bounded enough that it can be replaced without affecting adjacent components. The boundary is defined by the interface: a component that exposes a clean interface can be replaced with any implementation that satisfies the interface.

The architectural red flag: a component that is too large to be understood by a single engineer, or that has dependencies that bleed through its interface, is a component that needs to be split. The split is not always obvious, but it is almost always possible.

## SwiftUI Architecture: Unidirectional Data Flow

Eidhof's SwiftUI architectural guidance follows the unidirectional data flow pattern: state flows down from parent to child views, and actions flow up (through bindings, callbacks, or environment). This is architecturally simpler than two-way data binding because state changes are traceable — you always know where state is managed and how it changes.

The architectural discipline for SwiftUI: resist placing complex state management inside views. Views should be as stateless as possible, computing their display from the state passed to them. State that is shared between views should be managed by an observable object, not duplicated in multiple views.

## Property-Based Testing as an Architectural Validation Tool

Property-based testing is not just a testing technique for Eidhof — it is an architectural validation tool. If a function's properties cannot be expressed precisely enough to write a property-based test, the function's contract is not clear enough to be in the architecture. The act of writing property-based tests forces precision about what a function guarantees.

The architectural discipline: for every core algorithm or data transformation in the system, identify the properties it must satisfy and validate them with property-based testing. If a property cannot be identified, the function's role in the architecture is unclear.

## Sources
- [objc.io — functional Swift books and screencasts](https://www.objc.io/)
- *Thinking in SwiftUI* — Chris Eidhof and Florian Kugler, objc.io
- *Advanced Swift* — Eidhof, Kugler, Begemann, objc.io
- [WWDC sessions on SwiftUI architecture — various](https://developer.apple.com/videos/)
