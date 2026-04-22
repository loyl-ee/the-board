# David Smith — On Mobile Engineering

## Widget Engineering as a Discipline

Smith's work on Widgetsmith — an app whose entire purpose is widget creation — required mastering WidgetKit's constraints at a level most developers never encounter. Widgets are not views: they are snapshots generated on a schedule, rendered outside the app process, with no user interaction beyond a single tap. The engineering discipline is designing for a read-only, time-limited rendering context.

The mobile engineering insight: widgets that try to behave like interactive apps fail. The correct model is designing for the "glanceable moment" — the user unlocks their phone, sees the widget, and returns to their task. Everything in the widget's design and engineering should serve that two-second interaction.

## Health App Privacy Architecture

Smith's health apps (Pedometer++, Workouts++) are built with a privacy-first architecture: health data is processed on-device, not transmitted to a server, not logged, and not used for analytics. This is not a marketing claim — it is an engineering constraint that shapes every technical decision.

The mobile engineering discipline: when building health or personal data apps, design the architecture so that sensitive data never leaves the device. On-device processing with HealthKit, Core Motion, and CoreML means there is no server-side attack surface and no privacy policy to violate. Privacy through architecture is stronger than privacy through policy.

## Sustainable Release Cadence Engineering

Smith has shipped weekly podcast episodes (Developing Perspective, Under the Radar) alongside weekly app updates for years. This requires treating software development as a production system with a defined output rate, not as a creative process that ships when ready.

The mobile engineering discipline for sustainability: establish a release cadence and treat it as a production constraint. A weekly release forces scope discipline — you cannot add a feature that cannot be finished in a week. It trains the instinct to ship the minimum valuable increment rather than the complete ideal version.

## App Store Engineering: Ratings and Reviews

Smith has written about the engineering of App Store ratings prompts — specifically, the SKStoreReviewRequest API and the timing of when to request a review. The engineering decision: request a review at a moment of demonstrated success (the user completed a workout, created a widget they liked), not at a moment of friction.

The mobile engineering discipline: treat every user-facing system interaction (review prompts, notification permissions, purchase flows) as a UI/UX engineering problem, not a defaults problem. The default implementation is rarely the correct one.

## Complications and Always-On Display

Smith's experience with watchOS complications and the always-on display extends the widget engineering discipline to an even more constrained context: a 40×40 point area, updated at most every 15 minutes, rendered on a dim always-on display. The engineering problem is communicating one piece of information so clearly that it is readable at a glance on a dimmed screen at arm's length.

The mobile engineering principle: design for the most constrained context first. An interface that works on an Apple Watch complication works everywhere. An interface designed only for full-screen will fail in every smaller context.

## Sources
- [david-smith.org — David Smith's blog](https://david-smith.org/)
- [Under the Radar — Relay FM podcast with Marco Arment](https://www.relay.fm/radar)
- [Widgetsmith — App Store](https://apps.apple.com/app/widgetsmith/id1523682319)
- [WWDC sessions — WidgetKit, HealthKit, watchOS engineering]
