# Brent Simmons — On Architecture

## Mac-Native Architecture Patterns

Simmons' architectural approach is built on the Cocoa application model: a document-based or single-window app with a model-view-controller separation, using AppKit for the view layer, Core Data or a custom persistence layer for the model, and a clear separation between the UI code and the data code.

This is not an architectural choice made fresh — it is an architectural inheritance from decades of Mac application development that has proven correct over time. The Cocoa patterns for undo (NSUndoManager), document management (NSDocument), and user preferences (NSUserDefaults) are well-understood, well-tested, and well-integrated with the operating system. Using them correctly is more important than inventing something new.

## Open Source Architecture: Readable by Strangers

NetNewsWire's architectural decisions are made with the understanding that strangers will read the code. The module boundaries are clear: the networking layer, the database layer, the article parser, the sync engine for each supported sync service, and the UI layer are all distinct. A contributor who wants to add support for a new sync service can read the existing sync engine implementations and understand what is required without reading the rest of the codebase.

The architectural principle: design module boundaries as if they are public APIs. A new contributor's ability to contribute to one module without touching others is the test of whether the boundaries are correct.

## Long-Term Architecture: No Dead Ends

Simmons has maintained NetNewsWire for over two decades through multiple technology transitions. The architectural lesson: avoid choices that create dead ends. A dependency on a specific framework version, a proprietary data format, or a third-party service that might disappear creates future migration debt.

His architectural heuristics for longevity: prefer open standards (RSS, Atom, SQLite) over proprietary alternatives, prefer system frameworks over third-party libraries, and prefer data formats that can be read by any tool over formats that require your specific application.

## The Sync Architecture Problem

NetNewsWire supports multiple sync services (Feedbin, Feedly, NewsBlur, iCloud, etc.). Each service has a different API, a different data model, and different reliability characteristics. The architectural solution is an abstract sync engine with service-specific implementations: a common interface that the application talks to, and service-specific implementations that translate between the service's API and the common interface.

This is the architectural pattern for handling heterogeneous external services: define an abstraction at the boundary of your system and implement service-specific adapters behind it. The application code changes when your requirements change; the adapter code changes when the service's API changes.

## The Open Web as an Architectural Commitment

Simmons' advocacy for the open web is not just a philosophical position — it has architectural consequences. NetNewsWire does not depend on any closed platform. RSS and Atom are open standards that any server can implement. The sync services NetNewsWire supports are chosen partly for their API openness and stability.

The architectural discipline: for any external dependency, evaluate whether it could disappear without notice (a closed platform can shut down their API; an open standard cannot). Prefer dependencies that can be replaced.

## Sources
- [inessential.com — Simmons' blog](https://inessential.com/)
- [NetNewsWire — GitHub (open source)](https://github.com/Ranchero-Software/NetNewsWire)
- [NetNewsWire architecture discussions — GitHub issues and inessential.com](https://inessential.com/)
