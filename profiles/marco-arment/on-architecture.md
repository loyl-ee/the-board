# Marco Arment — On Architecture

## The iOS App as a Monolith

Arment's iOS application architecture is explicitly monolithic in the sense that DHH uses the term: a single process, a single codebase, no external services beyond what is necessary. Overcast is an app and a sync server. The app contains all the logic; the server contains only what the app genuinely cannot do locally (push notification delivery, podcast search, subscription validation).

The architectural principle for mobile apps: keep as much logic as possible in the app process, where you control it completely, rather than distributing it to backend services that become dependencies. A feature that works without a network connection is more reliable than a feature that requires one.

## Audio Architecture: The Processing Graph

Overcast's audio engine is a graph of AVAudioNodes managed by AVAudioEngine. Each node in the graph performs a specific transformation: input from file or network, playback speed adjustment, Smart Speed silence detection, Voice Boost equalisation, output to hardware. The graph architecture makes the audio pipeline composable and testable: individual nodes can be replaced, reordered, or bypassed.

The architectural lesson for processing pipelines: model the pipeline as a directed graph where each node performs a single transformation. The graph architecture separates the definition of what transformations to apply from the implementation of each transformation.

## Privacy-Constrained Architecture

Overcast's server architecture is constrained by the privacy decisions Arment has made. Because the server does not collect listening data, the server does not know which episodes users have listened to, what their listening history looks like, or what podcasts they subscribe to. This constraint shapes the sync architecture: the server stores what it needs to support features (episode positions, subscription lists) and nothing more.

The architectural discipline: start with the privacy requirements, then design the architecture to satisfy them. Adding privacy constraints to an existing architecture is far more expensive than designing privacy into the architecture from the start.

## Third-Party Dependency Architecture

Arment is conservative about third-party dependencies in his architecture. Overcast uses system frameworks — AVFoundation, URLSession, Core Data — rather than third-party alternatives. The reasoning: system frameworks are maintained by Apple, updated with the OS, and do not require his review when they change. Third-party frameworks require him to evaluate each version update, understand what changed, and decide whether the update is safe to ship.

The architectural standard: for any component of the system, prefer the system framework if one exists and is adequate. Third-party alternatives are appropriate when the system framework is genuinely insufficient, not when a third-party alternative is more convenient.

## Indie App Economics and Architecture

The economics of an indie iOS app — a single developer, no venture capital, no large engineering team — constrain the architecture in specific ways. The architecture must be maintainable by one person. The backend infrastructure must be operable by one person. The deployment process must be something one person can manage.

These constraints produce architectural discipline: no microservices, no Kubernetes, minimal moving parts. Arment has discussed his server architecture in terms of what he can diagnose and fix at 2am when something breaks. That is the correct test for an indie application's architecture.

## Sources
- [Marco.org — Arment's blog](https://marco.org/)
- [Accidental Tech Podcast — architecture discussions](https://atp.fm/)
- ["Overcast's audio engine" — Marco.org](https://marco.org/2014/07/17/overcast-audio-features)
- [Build Phase podcast — various episodes on iOS architecture]
