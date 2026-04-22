# Chris Eidhof — On Mobile Engineering

## SwiftUI Architecture: The View as Function

Eidhof's SwiftUI engineering philosophy centres on the view as a pure function of its state. A view that is a function of its state is a view that can be tested by constructing the state, is predictable because there are no hidden side effects, and is composable because it takes data and returns UI.

The mobile engineering discipline: when a SwiftUI view is hard to test or reason about, the cause is almost always state that lives in the view instead of being passed in. Extract state into a model type. Pass the model to the view. The view becomes a pure transformation of data into UI.

## The Environment as a Dependency Injection System

SwiftUI's Environment is a typed key-value store that flows through the view hierarchy. Eidhof has documented its correct use: push dependencies (database, network client, authentication state) into the environment at the root, and access them from leaf views without passing them through every intermediate view.

The mobile engineering discipline: do not pass dependencies through multiple layers of views via property chains. Use the environment for system-wide dependencies and ObservableObjects for view-local state. The distinction: environment is for infrastructure; @StateObject is for view-owned data.

## Types as Documentation: Making Invalid States Unrepresentable

Eidhof's functional programming influence in iOS: model your data with types that make invalid states impossible to construct. An Optional<User> where nil means "logged out" is a typed state machine. An enum with associated values is a sum type that is exactly as expressive as its cases require.

The mobile engineering discipline: before writing conditional logic (`if user != nil`, `if isLoading && !hasError`), ask whether a type could express this state. A `LoadingState<T>` enum with `.loading`, `.loaded(T)`, `.failed(Error)` cases eliminates the combinations that unit tests must cover.

## SwiftUI Performance: Identity and Lifetime

Eidhof has documented SwiftUI's view identity and lifetime model — the rules by which SwiftUI decides whether a view is new (reconstructed) or existing (updated). The engineering insight: SwiftUI performance problems are almost always identity problems. Views that reconstruct when they should update trigger expensive animations and lose transient state.

The mobile engineering discipline: use stable identifiers in ForEach. Prefer `.id()` modifiers deliberately, not cargo-culted. Understand that structural identity (position in the view tree) is separate from explicit identity (the `.id()` modifier). When a list scrolls slowly, the problem is identity, not rendering.

## Testing SwiftUI: Separate Logic from View

Eidhof's testing approach for SwiftUI: do not test views directly (SwiftUI's testing story is weak). Test the state transformations that drive views. A view model with pure functions (`mutating func selectItem(_ id: Item.ID)`) is testable without a simulator. The view is a thin layer over tested logic.

The mobile engineering discipline: design view models as pure state machines. Every user interaction is an input; the resulting state is the output. Test the state machine. Trust the view to render the state correctly — that is what SwiftUI is designed to do.

## Sources
- [objc.io — Swift programming books and videos](https://www.objc.io/)
- *Thinking in SwiftUI* — Chris Eidhof and Florian Kugler, objc.io
- *Swift UI in Practice* — objc.io video series
- [Swift Talk — objc.io video series on functional Swift](https://talk.objc.io/)
