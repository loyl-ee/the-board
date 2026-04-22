# Chris Eidhof — On Testing

## Property-Based Testing: Test the Law, Not the Example

Eidhof advocates property-based testing (using Swift's SwiftCheck or equivalent) for code that has invariants: functions where a property should hold for all inputs, not just the ones you thought to write tests for. For a `sort` function, the property is that the output is sorted and contains the same elements as the input. Testing on three hand-crafted arrays does not tell you the function is correct — testing on 10,000 randomly generated arrays does.

The testing discipline: when writing a pure function, identify its invariants. If you can express an invariant that should hold for all inputs (commutativity, associativity, idempotency, round-trip encoding), write a property test. The random input generator will find edge cases your examples will not.

## Types as the First Test

Eidhof's foundational position: the type system is the first and most important test suite. A type that makes invalid states unrepresentable eliminates an entire class of tests — the tests that verify the code handles invalid states correctly. When invalid states cannot be constructed, you do not need to test what happens when they are.

The testing discipline: before writing a unit test for a failure case, ask whether the type system can make that failure case impossible. A `NonEmptyArray<T>` type does not need tests for the empty case. An enum with only valid cases does not need validation tests.

## Test Logic, Not Views

Eidhof's SwiftUI testing discipline: views should not be tested directly. SwiftUI's rendering is tested by Apple; the logic that drives your views is your responsibility. The correct testing target is the view model — the pure state machine that transforms user actions into new state.

The testing pattern: write view models as structs with `mutating func` methods. Each method is a state transition: `mutating func userTappedFavorite(_ id: Item.ID)`. Test the struct directly without constructing any views. The test is fast (no UI), deterministic (no rendering), and complete (covers all state transitions).

## Small Components Are Testable by Definition

Eidhof's architectural preference for small, well-bounded components directly enables testing. A function that does one thing has one observable behaviour. A component that takes its dependencies as parameters (not from global state) can be tested by constructing the dependencies. A type with a clear interface can be tested through that interface.

The testing discipline: if a unit is hard to test, the architecture needs simplification. Hard-to-test code is a signal that the code has too many responsibilities, hidden dependencies, or implicit global state. Fixing the architecture fixes the testability.

## Snapshot Testing for Complex UI

For SwiftUI views that have genuinely complex rendering (charts, custom drawing, complex layouts), Eidhof has used snapshot testing: render the view, capture the output as an image, and fail the test if the image changes. Snapshot tests detect unexpected visual regressions without requiring manual review of every UI change.

The testing discipline for snapshot tests: treat failing snapshots as changes to review, not as failures to fix immediately. A snapshot failure means the rendering changed — sometimes intentionally (update the snapshot), sometimes accidentally (fix the bug). The discipline is reviewing every snapshot failure before updating.

## Sources
- [objc.io — Swift programming books and videos](https://www.objc.io/)
- *Advanced Swift* — Chris Eidhof, Florian Kugler, Ole Begemann, objc.io
- [Swift Talk — property-based testing episodes](https://talk.objc.io/)
- [SwiftCheck — property-based testing for Swift](https://github.com/typelift/SwiftCheck)
