# David Smith — On Engineering

## Widget Engineering: Constraints as Creativity

Smith is the author of Widgetsmith, the most-downloaded widget app in App Store history. Widgets in iOS operate under severe engineering constraints: no continuous process, a snapshot-based rendering model, limited memory, no user interaction beyond a single tap. These are not bugs in the platform — they are engineering constraints that force clear thinking about what a widget actually needs to do.

His approach to the widget runtime is to treat it as a display surface only: data is fetched and processed by the main app, serialised into a timeline of snapshots, and handed to the widget extension. The widget code itself is stateless and fast. This separation of concerns — processing in the app, display in the widget — maps directly to the platform's intent and produces widgets that are reliable and battery-efficient.

## Solo Maintainability as an Architectural Requirement

Smith maintains a portfolio of apps — Widgetsmith, Pedometer++, Sleep++, Heart Analyzer — as a solo developer. This constraint is not incidental; it is the primary architectural requirement. Every design decision is filtered through: can I understand this in six months? Can I fix a bug in this at 11pm when a critical issue is reported?

The practical implications: minimal third-party dependencies (each is a maintenance liability), thin abstraction layers (deep stacks are debugging nightmares for one person), and aggressive use of platform frameworks (Apple maintains them, not him). He has written about deleting abstractions that seemed helpful at write time but added cognitive overhead at maintenance time.

## Privacy-First Engineering

Smith's apps collect no third-party analytics. There is no Mixpanel, no Firebase, no advertising SDK. The engineering decision is principled and practical: third-party SDKs are security and privacy risks, they increase binary size, they introduce review complications, and they create dependencies on services outside his control.

Where he needs usage data for product decisions, he uses Apple's App Store Connect analytics — privacy-preserving, aggregated, and requiring no SDK. His argument: if you cannot make product decisions with App Store Connect analytics, you need more data than any individual user should be asked to provide.

## HealthKit and Sensor Engineering

Several of Smith's apps integrate with HealthKit — Apple's health data platform. The engineering discipline HealthKit requires is specific: health data is sensitive, the permissions model is granular, and users can revoke access at any time. Code that assumes HealthKit data is always available fails in ways that are embarrassing and trust-destroying.

His approach: always handle missing or incomplete health data gracefully, never assume permissions, and explain clearly what data is used and why before requesting access. These are not just compliance requirements — they are engineering requirements for building software people trust with their health data.

## App Store Economics as an Engineering Constraint

Smith has been publicly transparent about App Store revenue across his portfolio. The economics shape engineering decisions: a free app with in-app purchases requires engineering a paywall and managing subscription state. A paid app requires engineering a trial experience. A subscription app requires engineering renewal logic and grace periods.

His observation: over-engineered monetisation systems create more bugs and support burden than they generate in revenue. The simplest monetisation model that works for your product is almost always the right engineering choice. Widgetsmith's initial free/premium split was a simple paywall, not a complex metered system.

## Sources
- [david-smith.org — Smith's blog](https://david-smith.org/)
- [Developing Perspective podcast (archived)](https://developingperspective.com/)
- [Widgetsmith — App Store](https://apps.apple.com/app/widgetsmith/id1523682319)
- [App Store revenue transparency posts — david-smith.org](https://david-smith.org/)
