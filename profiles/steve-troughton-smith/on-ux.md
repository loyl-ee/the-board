# Steve Troughton-Smith — On UX

## Power Users as First-Class Citizens

Troughton-Smith's UX instincts are shaped by his own use patterns: he is a keyboard-driven, multi-window, professionally productive user of Apple devices, and he advocates for that mode of use as something Apple's platforms should support with the same rigor they apply to touch-first interactions. His iPad Pro manifestos consistently name keyboard shortcuts as a gap: the command-key shortcut panel has poor discoverability, there is no persistent menu bar, and the system help infrastructure present on Mac is absent from iPadOS.

He discovered the iOS 9 keyboard's new Tab and Caps Lock keys and top-row symbol additions before Apple announced them, consistent with his broader pattern of tracking where platform UX is heading before it ships publicly.

## The Gap Between What iPadOS Could Do and What Apple Allows

This is the central UX argument in his body of work. The gap has several layers:

**Capability gap**: Apple's own apps ship features using private APIs that third-party apps cannot access. Safari can use JIT compilation; third-party browsers cannot. Apple's Playgrounds can compile and install apps to the local device; no third-party IDE can. This is not a UX design choice — it is a policy choice that manifests as a UX limitation.

**API gap**: Stage Manager shipped with no developer APIs for window management. Third-party apps could not respond to Stage Manager's affordances in a first-class way. The UX of Stage Manager in third-party apps was therefore always worse than it needed to be, not because developers were negligent, but because the tools were withheld.

**Background task gap**: iOS/iPadOS does not support long-running background processes in the way macOS does. A scripting app cannot run a script as a sub-process that outlives the host app's foreground state. A video export cannot continue reliably when the user switches apps. These are UX limitations for power users who expect their professional tools to behave like professional tools.

## Menu Bar as Power User Anchor

He has noted consistently that the absence of a persistent menu bar on iPadOS is a UX regression for keyboard users coming from Mac. The command-key shortcut panel — the iPadOS substitute — is discoverable only if you know to hold the command key, and it provides no persistent surface for infrequently used commands. He cited menu bar support as "a top user request and developer topic over the past two years" with no action from Apple.

## On Review Prompts

A characteristically precise UX observation from 2026: "Review prompts are the difference between a great app experience and a good one" — raising the question of how and when to ask for ratings without breaking the user's flow. This reflects his broader attention to the small design decisions that separate professional-quality apps from adequate ones.

## SwiftUI as a UX Regression for Developers

He has been critical of SwiftUI's execution, arguing that it has not delivered on its cross-platform promise: "Boy do I wish Apple had built a real Apple-quality next-gen UIKit/AppKit-like first-party cross-platform UI framework instead of SwiftUI. The closest thing Apple makes is still Catalyst, but they completely squandered their opportunity to make something better than what came before." (Mastodon, 2025). For him, a framework's UX includes the developer experience of building with it — and SwiftUI's gaps in reliability, API coverage, and debugging tooling are UX failures, not just technical ones.
