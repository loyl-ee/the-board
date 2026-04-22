# Chris Eidhof — On Engineering

## Types as the Best Documentation

Eidhof's core engineering principle is that the type system is the most reliable form of documentation a codebase has. A function signature in Swift that says `func transfer(amount: Decimal, from: AccountID, to: AccountID) throws` tells you more about its contract than any comment could. The types constrain what is possible, the `throws` tells you it can fail, and the names tell you the domain. When the types are right, the code is self-describing.

The corollary: when code requires extensive comments to explain its invariants, the type design is probably wrong. Encode the invariants in the type system instead. A `NonEmptyArray<T>` is clearer than an `Array<T>` with a "must not be empty" comment. A `ValidatedEmail` is clearer than a `String` with a "must be valid email" assumption.

## Making Illegal States Unrepresentable

Eidhof is one of the clearest expositors of the principle "make illegal states unrepresentable," derived from functional programming but directly applicable to Swift. The idea: if a program state is invalid, design your types so that state cannot be constructed. Use enums to model mutually exclusive states rather than booleans that can be in contradictory combinations.

For example: an authentication state should not be modelled as `isLoggedIn: Bool` and `currentUser: User?`. It should be modelled as `enum AuthState { case loggedOut; case loggedIn(User) }`. The second form makes it impossible to have `isLoggedIn = true` with no user — an inconsistent state that causes bugs in the first model.

## Small, Well-Bounded Components

At objc.io, Eidhof has consistently advocated for decomposing software into small components with clear responsibilities and minimal dependencies. Each component should be understandable in isolation, testable without a full app stack, and replaceable without touching its callers.

This is not dogma — it is pragmatism. Small components are easier to reason about at review time, easier to test, and easier to refactor. A 2,000-line view controller is not just aesthetically unpleasant; it is genuinely harder to understand than four 500-line components with defined interfaces between them.

## SwiftUI as an Engineering Discipline

Eidhof's work on SwiftUI architecture reflects a broader principle: declarative code should describe *what* the UI is, not *how* to update it. The engineering discipline is separating state from view, keeping views as pure transformations of state, and placing side effects at the edges of the system.

He advocates for `ObservableObject` and environment values as the dependency injection mechanism — not singletons, not global state. The architecture should be legible: trace the data flow from state change to view update, and any engineer should be able to follow it.

## Property-Based Testing

Eidhof is a consistent advocate for property-based testing in Swift using libraries like SwiftCheck. Rather than writing individual test cases (input → expected output), property-based testing defines the *properties* that should hold for all inputs and lets a framework generate hundreds of random test cases.

This approach finds edge cases that example-based tests miss, documents the true constraints of a function, and builds confidence that code works for the full input space rather than a hand-selected subset. It is especially powerful for data transformation functions where the valid input space is large.

## Sources
- [objc.io — Swift programming books and screencasts](https://www.objc.io/)
- *Thinking in SwiftUI* — Chris Eidhof and Florian Kugler, objc.io
- *Advanced Swift* — Chris Eidhof, Florian Kugler, and Ole Begemann, objc.io
- [SwiftUI Lab](https://swiftui-lab.com/) — SwiftUI architecture discussions
- [Make Illegal States Unrepresentable — F# for Fun and Profit](https://fsharpforfunandprofit.com/posts/designing-with-types-making-illegal-states-unrepresentable/) (concept Eidhof applies to Swift)
