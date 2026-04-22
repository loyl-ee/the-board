# Brent Simmons — On Mobile Engineering

## iOS as a Second Citizen, Mac as the First

Simmons built NetNewsWire as a Mac app first, and its iOS port is explicitly a Mac-derived product. His engineering hierarchy: the Mac is the primary platform where the interface can breathe, where keyboard shortcuts matter, where power users live. iOS is a reading surface — important, but not the place where the full product vision is expressed.

The mobile engineering implication: when building apps that exist on both platforms, do not let iOS constraints drive the Mac design. Build the Mac app to Mac standards, then build the iOS app to iOS standards. Platform-parity is a business constraint, not a design goal.

## RSS and Open Protocol Implementation

NetNewsWire's core is an RSS/Atom parser and a sync engine. The mobile engineering challenge: RSS is a loosely-specified format where real-world feeds violate the spec regularly. The correct engineering response is generous parsing — accept everything that is plausible, not just what is technically correct.

The mobile engineering principle from RSS engineering: the specification describes what producers should send, not what consumers will receive. Production data is always messier than the spec. Parse defensively, fail gracefully, and log what you cannot parse rather than crashing.

## Performance in Feed Readers

A feed reader that processes hundreds of feeds, with thousands of articles per feed, must handle large data sets without blocking the main thread. Simmons' engineering for NetNewsWire: all network requests, parsing, and database writes happen on background queues. The main thread touches only what is visible on screen.

The mobile engineering discipline: on iOS, the main thread is for UI only. Any operation that touches the network, the disk, or a large in-memory data structure belongs on a background queue. An app that blocks the main thread fails its users visibly — the interface freezes.

## Core Data and SQLite for Local Persistence

NetNewsWire moved from Core Data to a custom SQLite layer. The engineering reason: Core Data's abstraction adds complexity that is only justified when the data model changes frequently. For a feed reader with a stable schema, direct SQLite via FMDB gives predictable performance and debuggable SQL queries.

The mobile engineering lesson: Core Data is not the default correct choice for iOS persistence. It is the correct choice when the data model is complex and changing. For stable schemas with large data sets, SQLite with a thin wrapper gives better visibility and control.

## SwiftUI vs. AppKit/UIKit for Existing Apps

Simmons has been explicit about the cost of rewriting existing apps in SwiftUI: the framework is not mature enough to replace AppKit for complex Mac apps, and UIKit for complex iOS apps. SwiftUI is appropriate for new views in existing apps, for watchOS/tvOS interfaces, and for simple iOS apps. It is not yet a replacement for the full UIKit/AppKit surface.

The mobile engineering discipline: evaluate SwiftUI feature by feature, not as an all-or-nothing migration. Use it where it is better than UIKit/AppKit — simple declarative views, previews, prototyping. Keep UIKit/AppKit where control is required.

## Sources
- [inessential.com — Brent Simmons' blog](https://inessential.com/)
- [NetNewsWire — GitHub](https://github.com/Ranchero-Software/NetNewsWire)
- [Under the Radar — various episodes on Mac-first development]
- [WWDC sessions — referenced in inessential.com posts]
