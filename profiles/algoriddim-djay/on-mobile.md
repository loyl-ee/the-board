# Algoriddim / djay — On Mobile Engineering

## AVAudioEngine as Creative Platform

djay's audio engineering is built on AVAudioEngine's audio unit graph — a real-time audio processing pipeline capable of sub-millisecond latency. Two simultaneous audio streams, each with independent pitch/tempo processing, EQ, reverb, and effects — all mixed in real time. This is not consumer audio playback; it is a professional audio workstation running on an iPhone.

The mobile engineering lesson: AVAudioEngine is underused because it requires understanding audio graph architecture, buffer management, and real-time thread constraints. Apps that need serious audio quality — not just playback — should invest in the AVAudioEngine graph model rather than the higher-level AVPlayer abstractions.

## Neural Mix: On-Device ML for Real-Time Audio

Neural Mix, djay's AI stem separation feature (isolating vocals, instruments, and drums from any track in real time), runs entirely on-device using Apple's Neural Engine. The engineering challenge: stem separation models are large and computationally expensive. Making them run in real time on a mobile device required model optimisation, quantisation, and careful use of the Neural Engine without blocking the audio thread.

The mobile engineering discipline: on-device ML for real-time audio requires the inference to run on a separate thread from the audio processing graph. The Neural Engine has its own scheduling, and blocking the audio callback is audible as glitches. Architecture: inference produces a buffer of stems; the audio graph consumes from that buffer.

## Native Apple API Integration as Competitive Advantage

djay is not a cross-platform app. It is written for each Apple platform natively — iOS, macOS, and tvOS — using the platform's native frameworks. The result is that djay integrates with Apple's ecosystem at a level that cross-platform frameworks cannot: AirDrop for track sharing, Handoff for session continuity, Apple Music for library access, AirPlay for external audio output.

The mobile engineering argument: native Apple API integration is only possible if you are writing native code. Every platform feature Apple adds becomes a potential feature for native apps and an impossible gap for cross-platform apps.

## Real-Time Audio and Background Execution

djay requires background audio execution — the music must keep playing when the user locks the screen or switches apps. iOS background audio is a specific entitlement with specific constraints: the audio session must be configured correctly, the app must declare the `audio` background mode, and the audio must be continuous.

The mobile engineering discipline for audio apps: test background audio execution explicitly. Common failure modes — the audio session being interrupted by a phone call, the audio route changing when headphones are disconnected, the session deactivating when another app starts audio — must all be handled gracefully.

## Apple Silicon and the Unified Memory Model

Algoriddim's engineering work benefits from Apple Silicon's unified memory model: the CPU, GPU, and Neural Engine share memory, eliminating copy operations between processing stages. Audio processed by the CPU can be handed to the Neural Engine for ML inference without a memory copy — a significant performance advantage for a real-time audio pipeline.

The mobile engineering lesson: on Apple Silicon, design pipelines that keep data in the unified memory pool rather than moving it between discrete memories. Metal Performance Shaders, Core ML, and AVAudioEngine are all designed to work within this model.

## Sources
- [algoriddim.com — djay product and engineering blog](https://www.algoriddim.com/)
- [djay Pro — App Store](https://apps.apple.com/app/djay-pro/id947578651)
- [WWDC sessions — AVAudioEngine, Core ML, Neural Engine engineering]
- ["Neural Mix" — Algoriddim feature documentation and engineering blog posts]
