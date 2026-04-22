# Marco Arment — On Security

## Privacy as a Technical Architecture, Not a Policy Document

Arment's privacy position is engineering, not marketing. Overcast does not collect listening data. The server knows device tokens (for push notifications), episode positions (for sync), and subscription status. Nothing else. This is not a policy claim — it is the consequence of a server architecture that was designed from the start not to collect what it does not need.

The security engineering argument: data that is not collected cannot be breached, subpoenaed, or sold. Every field in your database is a liability. The question before adding any data collection is not "what could we do with this?" but "what do we need to do with this, and does the value outweigh the risk?"

## No Tracking, No Advertising SDKs

Arment has been consistently hostile to third-party advertising and tracking in his apps. The security argument beyond privacy: advertising SDKs are significant attack surface. They are third-party code with broad permissions, often with their own networking stack, that execute in the context of your app. Their security practices are outside your control. Their updates can introduce vulnerabilities without your review.

The engineering discipline: every third-party SDK you include in your app is code you are responsible for but did not write. Audit it. Minimise it. Prefer system frameworks over third-party alternatives.

## HTTPS and Certificate Pinning

Arment has discussed Overcast's API architecture in terms of transport security: all communication uses HTTPS, and the app validates certificates strictly. The engineering standard for any app communicating with a backend: HTTPS everywhere, no HTTP fallbacks, and consider certificate pinning for sensitive API endpoints.

The security engineering principle: network communication that is not encrypted is communication that can be observed and modified by any network intermediary — your ISP, a coffee shop router, or a government surveillance system.

## App Store Sandboxing as a Security Model

Arment has written about iOS sandboxing as a genuine security benefit: apps on iOS cannot access other apps' data, cannot modify system files, and cannot install code that Apple has not reviewed. This is not a constraint he chafes against — it is a security model that benefits his users.

The engineering standard: work within platform security models rather than around them. iOS sandboxing, macOS notarisation, and App Store review exist because they provide security guarantees that benefit users. An app that circumvents these mechanisms is an app that users cannot trust.

## User Data Minimisation in Sync Architecture

Overcast's sync architecture is designed to sync what users need across devices — episode positions, played status, playlist contents — while collecting nothing that reveals what users listen to in aggregate. The server-side schema does not include a "listening history" table because that data was deliberately excluded from the design.

The security engineering discipline: design the schema and API around the minimum data required to provide the feature. Expand data collection only when a specific feature requires it, not speculatively.

## Sources
- [Marco.org — Arment's blog](https://marco.org/)
- [Overcast privacy policy — overcast.fm](https://overcast.fm/privacy)
- [Accidental Tech Podcast — privacy and security episodes](https://atp.fm/)
- [Marco on tracking — various blog posts and ATP episodes]
