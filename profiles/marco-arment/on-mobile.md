# Marco Arment — On Mobile Engineering

## Native First, Always

Arment's mobile engineering philosophy starts with a categorical position: native APIs are not optional for quality iOS apps. The UIKit and SwiftUI frameworks are not abstractions over the platform — they are the platform. Apps built with cross-platform frameworks (React Native, Flutter, Capacitor) trade platform integration for development convenience, and the cost is visible to users who use native apps daily.

The mobile engineering standard: if you are building a paid iOS app, it should be built with native APIs. Users who pay for apps notice the difference between apps that feel like iOS and apps that feel like a website.

## Audio Engineering as Core Competency

Overcast's audio engineering is its competitive moat. The Voice Boost feature required Arment to write custom DSP code using AVAudioEngine's audio unit graph — not a plug-in from a library, but original signal processing code. Smart Speed required analysing audio in real time to detect and remove silence.

The mobile engineering lesson: the features that are hardest to build are the features that competitors cannot copy quickly. If a feature can be implemented with an off-the-shelf library, it provides no durable differentiation. If it requires original engineering in a domain that most developers avoid, it does.

## Performance as User Respect

Arment has written about performance as a form of respect for the user's time and battery. Every unnecessary computation is a tax on the user. Every background task that prevents the CPU from sleeping is a drain on the battery. The engineering discipline: understand what the hardware is doing, and do not waste it.

The mobile engineering discipline for iOS: use Instruments to profile CPU usage, memory allocations, and battery impact before shipping. Background audio apps like Overcast have particular responsibility — they run while the screen is off and battery usage is directly visible to users.

## App Size and Launch Time

Arment has written about app binary size and launch time as engineering quality metrics. A large app binary takes longer to download and update. A slow launch time is the first impression. Both are engineering failures that ship silently.

The mobile engineering discipline: measure app launch time from cold start. Use App Thinning and on-demand resources to keep binary size minimal. Every MB added to the binary should be justified.

## iOS Version Support Policy

Arment's approach to iOS version support: support the current and previous major iOS version, no further. Supporting older iOS versions requires conditional code paths, prevents using new APIs, and increases testing surface. The engineering overhead of maintaining backwards compatibility beyond two versions is not justified by the marginal increase in addressable users.

The mobile engineering argument: users who keep devices on very old iOS versions are also less likely to purchase apps or follow software updates. The commercial and engineering cost of supporting them outweighs the benefit.

## Sources
- [marco.org — Marco Arment's blog](https://marco.org/)
- [ATP — Accidental Tech Podcast](https://atp.fm/)
- ["Overcast" — App Store, engineering notes](https://overcast.fm/)
- [WWDC sessions — AVAudioEngine and audio engineering references]
