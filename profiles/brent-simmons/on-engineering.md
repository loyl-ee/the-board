# Brent Simmons — On Engineering

## Mac-Native as an Engineering Commitment

Simmons built NetNewsWire — one of the longest-lived Mac applications still in active development — using AppKit, not web views, not Electron, not cross-platform toolkits. His engineering position is that Mac-native development means using the platform's actual frameworks: AppKit for views, Core Data for persistence, URLSession for networking, and the frameworks Apple ships and maintains. This is not nostalgia; it is leverage.

The engineering argument for native: AppKit evolves with macOS. Accessibility is built in. Performance is platform-native. The app integrates with system services — Spotlight, Services menu, AppleScript, Shortcuts — without adaptation layers. A cross-platform framework gives you code that runs everywhere and behaves like it comes from nowhere.

## Open Source as an Engineering Practice

NetNewsWire has been open source since its revival in 2018, and Simmons maintains it with a community of contributors under the MIT licence. He has written about open source stewardship as an engineering discipline: the codebase must be readable by people who didn't write it, the architecture must be documented at least informally, and contributions must be reviewable without requiring deep context to evaluate.

The practical engineering implication: code that will be read by strangers is written more carefully than code written for yourself. The review process that open source requires produces better code than private development, because shame is a useful quality control mechanism.

## The Open Web as an Engineering Philosophy

Simmons is one of the most consistent engineering advocates for the open web — RSS, Atom, ActivityPub, and open protocols. NetNewsWire is an RSS reader. Feedbin and similar services that it supports are built on open standards. His position: software that depends on proprietary APIs is software that can be killed by a platform decision. Software built on open standards can be maintained, forked, and rebuilt independently of any single company.

The engineering principle: prefer open standards over proprietary APIs. Accept the constraints that come with open standards — they are the constraints that make the software durable.

## Long-Term Code as Engineering Discipline

NetNewsWire dates to 2002. Simmons has been writing Mac software for over two decades, maintaining codebases across Objective-C and Swift transitions, processor architecture changes (PowerPC to Intel to Apple Silicon), and four major AppKit revisions. The engineering discipline required to maintain software across that span is specific: avoid architectural dependencies that tie you to a single OS version, write migrations for every data model change, and test on old OS versions before deprecating support.

Long-term maintenance shapes API design: once a public API is released, it must be supported. Simmons is careful about what he publishes because he knows he will be responsible for it.

## Resist the New for Its Own Sake

Simmons has written about the tendency in software engineering to reach for new frameworks, languages, and abstractions before mastering existing ones. His caution: new technology introduces risk, breaks muscle memory, and requires learning time. The engineer who is fluent in AppKit and reaches for SwiftUI before understanding what SwiftUI gains and loses has introduced a maintenance risk in exchange for novelty.

His approach: adopt new platforms and frameworks deliberately, not compulsively. SwiftUI is now part of NetNewsWire — but it was adopted where it offers clear advantages over AppKit, not as a wholesale replacement.

## Sources
- [inessential.com — Simmons' blog](https://inessential.com/)
- [NetNewsWire — GitHub (open source)](https://github.com/Ranchero-Software/NetNewsWire)
- [NetNewsWire blog](https://netnewswire.blog/)
- [On the open web — various inessential.com posts](https://inessential.com/)
