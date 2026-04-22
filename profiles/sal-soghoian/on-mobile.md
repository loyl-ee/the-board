# Sal Soghoian — On Mobile Engineering

## Shortcuts as the Mobile Automation Layer

Soghoian's work on iOS Shortcuts (as successor to Workflow, itself successor to Automator) is mobile engineering for user empowerment. Shortcuts is not a scripting tool — it is a visual programming environment for users who do not think of themselves as programmers. The engineering challenge it solves: exposing app functionality to automation without requiring users to write code.

The mobile engineering discipline: every app action that users might want to automate should be exposed as a Shortcuts action. The Shortcuts engine is the scriptability layer of iOS in the same way AppleScript was the scriptability layer of the Mac. An app without Shortcuts actions is an app that power users cannot fully own.

## Donate Your App's Intent Vocabulary

Soghoian's framework for Shortcuts integration: apps should donate their intent vocabulary to the system. When a user performs an action in the app, donate that action as an INIntent. Siri and Shortcuts can then surface it as a suggested automation, reducing the gap between what the user can do and what they know the app can do.

The mobile engineering implementation: use SiriKit Intents and App Intents (iOS 16+) to expose app actions. The App Intents framework is significantly cleaner than the older SiriKit API and should be the default for new automation work. Actions that are exposed as App Intents also appear in Spotlight, Focus Filters, and the Shortcuts editor.

## Automation as Product Differentiation

Soghoian's core argument: apps that support automation attract power users who then become advocates. A user who has built a personal Shortcut around your app is a user who cannot easily switch to a competitor — not because of lock-in, but because they have invested time in building their workflow around your app's actions.

The mobile engineering argument: Shortcuts support is not a feature for the majority of users. It is infrastructure for the minority who build workflows, and that minority drives disproportionate word-of-mouth and App Store reviews.

## Focus Filters and Contextual Automation

iOS 16+ Focus Filters allow apps to respond to the user's active Focus mode — showing work content in Work Focus, personal content in Personal Focus. Soghoian's philosophy extended: the app's state should adapt to the user's context, not the other way around.

The mobile engineering pattern: implement FocusFilterIntent to let users configure what your app shows in each Focus mode. This is especially important for apps with multiple contexts (accounts, projects, modes) where switching manually requires effort.

## Scriptability as Respect for User Intelligence

Soghoian's deeper principle, carried from AppleScript to Shortcuts: scripting an app is an act of respect for the user's intelligence. It says: "We know you have needs we didn't anticipate. Here are the building blocks. Build what you need." The alternative — apps that can only do what their developers designed — treats users as passive consumers.

The mobile engineering standard: before shipping any significant workflow feature, ask: could a user want to automate this? If yes, expose it as an App Intent.

## Sources
- ["Sal Soghoian: The Man Behind Mac Automation" — various interviews](https://www.macstories.net/)
- [Apple WWDC sessions — SiriKit Intents, App Intents, Shortcuts engineering]
- [Sal Soghoian on Macintosh Automation — macosxautomation.com]
- [Under the Radar episodes — Shortcuts integration for indie developers]
