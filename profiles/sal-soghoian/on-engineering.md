# Sal Soghoian — On Engineering

## Scriptability as a First-Class Engineering Requirement

Soghoian spent 18 years at Apple as the Product Manager for Automation Technologies — the person responsible for AppleScript, Automator, and the subsequent Shortcuts framework. His engineering position, developed across that career, is that user scriptability is not an optional add-on for power users — it is a fundamental measure of a software product's quality.

A scriptable application exposes its actions and data through a defined interface. This forces the engineering team to think about the application's model as a public API. The act of making something scriptable reveals whether the internal model is coherent: if it is hard to script, it is hard to understand. Scriptability is a design quality signal.

## The Shortcuts Architecture: Actions as Building Blocks

The Shortcuts framework on iOS, iPadOS, and macOS is built on the concept of actions — discrete units of capability that can be composed into workflows. Soghoian's engineering philosophy behind this architecture: each action should do exactly one thing, have clear inputs and outputs, and be composable with other actions without requiring the user to understand the implementation.

The engineering discipline for app developers: when adding Shortcuts support, do not expose the full complexity of your app's internal model. Expose the *verbs* — the actions that users want to perform. "Add item to list", "Get today's tasks", "Mark as complete" — not "modify database record at index". The abstraction level should match the user's mental model, not the implementation.

## User Empowerment as Engineering Ethics

Soghoian's career-long position is that software should empower users to do things the developers did not anticipate. A locked-down app that can only do what its developers envisioned is a product failure — it treats users as consumers rather than creators. AppleScript was designed on the principle that a user who can write a simple script should be able to automate any action they can perform manually.

The engineering corollary: expose your app's capabilities through documented automation APIs. Users who automate your app are your most engaged users. They will find bugs you never anticipated, build workflows you never imagined, and become advocates for your product to other power users.

## Documentation of Automation APIs

Soghoian is emphatic that automation support is only as valuable as its documentation. An AppleScript dictionary that is not documented is a private API with an awkward syntax. Every automatable action should have a description, examples, and error handling guidance.

He has argued that automation documentation is often better user research than formal usability studies: the questions users ask about automating your app reveal exactly what they are trying to do and what your app's model obscures from them.

## The Open Automation Ecosystem

Soghoian has consistently advocated for open automation standards — URL schemes, x-callback-url, Apple Events, Shortcuts actions — over proprietary integration points. Open standards allow apps to interoperate without bilateral engineering agreements. A URL scheme that one app exposes can be called by any other app on the platform.

The engineering argument: proprietary integrations create N×M maintenance problems (every pair of integrated apps requires a specific integration). Open standards create N+M possibilities (every app that supports the standard works with every other app that supports it).

## Sources
- [macosxautomation.com — Soghoian's automation resources](https://www.macosxautomation.com/)
- [Automators podcast](https://www.relay.fm/automators) — frequent guest
- [Apple Shortcuts developer documentation](https://developer.apple.com/documentation/sirikit/adding_user_interactivity_with_siri_shortcuts_and_the_shortcuts_app)
- WWDC sessions on Shortcuts app integration (multiple years)
