# Algoriddim — On Product

## The Product Arc: From Utility to Instrument

djay launched in 2006 as freeware for Mac — a relatively straightforward digital simulation of a DJ setup at a time when most DJ software ran on Windows and required dedicated hardware. Algoriddim's first important product decision was making it good enough for real DJs to use, not just a novelty for enthusiasts. The commercial launch in November 2007 established the Mac version as a credible professional tool.

When the iPad arrived in 2010, Algoriddim did not simply resize the Mac interface. They rebuilt djay for touch interaction, with virtual turntables designed for fingers rather than mice, and album artwork as the central visual element. The iPad version won an Apple Design Award in 2011 — the first of three. The iPhone followed in 2011, again as a thoughtful redesign rather than a port.

## Key Product Milestones

**2014 — Spotify integration.** djay became the first DJ app to integrate a streaming service, giving users access to tens of millions of tracks without buying or downloading music. This was a meaningful democratization of the DJ library — previously, serious DJs needed large purchased collections. The integration was built first, trusted second, and eventually lost when Spotify terminated third-party DJ API access in 2020.

**2016 — Touch Bar support.** Algoriddim shipped Touch Bar integration at the MacBook Pro launch, with Karim Morsy demonstrating live at Apple's keynote. The Touch Bar provided tactile controls for crossfading, effects, and sample triggers — a natural fit for DJ performance workflow.

**2019 — djay Pro AI and Neural Mix.** This was the most significant product inflection point in the company's history. Neural Mix introduced real-time AI-powered stem separation, allowing DJs to isolate vocals, drums, and instruments from any track — locally, in real time, during live performance. The feature leveraged Apple's Bionic chip and Neural Engine, available to developers since the iPhone Xs. Neural Mix was patented with multiple U.S. and international patents.

**2021 — djay Pro AI for M1 Mac.** The M1 chip's 15x machine learning performance improvement enabled higher-quality Neural Mix processing. Morsy called M1 "a fundamental breakthrough" for the application, as it extended desktop-class AI performance to a device optimized for the mobile software architecture Algoriddim had refined over a decade.

**2023 — djay Pro 5 with next-generation Neural Mix.** Algoriddim partnered with AudioShake, an AI audio company, after more than a year of R&D collaboration. The updated Neural Mix delivered AudioShake's source separation algorithms optimized for real-time device performance — described by AudioShake CEO Jessica Powell as a "big technical challenge" given the requirement to run large AI models on-device without latency. djay Pro 5 also introduced Crossfader Fusion (automated transition blending) and Fluid Beatgrid (dynamic tempo analysis that adjusts beat grids automatically for tracks with variable tempo).

**2024 — djay for Apple Vision Pro.** The visionOS version required a complete rethinking of the djay interface — the team went back to "the drawing board," questioning every convention built over a decade of DJ interface design. The result offers three interaction paradigms: Windowed (traditional 2D interface), Volumetric (3D turntables brought into the user's space), and Immersive Scenes (full spatial environments including a nighttime desert and a space lounge with dancing robots). djay won the 2024 Apple Design Award for Spatial Computing.

**2024 — djay for Meta Quest.** DJ Eskei83 performed the first professional DJ set powered entirely by a VR headset at Riverside Studios in Berlin.

## Neural Mix: The Product's Technical Centerpiece

Neural Mix is described by Algoriddim as "inspired by the auditory system of the human brain." What this means in practice: the app displays separate waveforms for vocal, instrumental, and drum components per track, updating in real time as stem isolation sliders are adjusted. DJs can crossfade not between whole tracks but between the stems of different tracks — removing a vocal from one song while bringing in the instruments from another, blending the drums of two records independently.

Neural Mix runs on-device without server calls, which is essential for live performance (no network dependency) and enables use in environments where streaming would be impractical. The technology is disabled for tracks from Apple Music and Spotify due to licensing restrictions — a significant limitation that illustrates how platform partnerships constrain product capability.

## Hardware Controller Integration

djay supports 100+ MIDI controllers with plug-and-play native integration, including deep partnerships with Pioneer DJ (CDJ-3000X, CDJ-3000, CDJ-2000NXS2), Reloop (including the Reloop Buddy, designed exclusively for djay), and Numark. The Reloop Mixon 8 Pro is a four-channel professional controller with dedicated Neural Mix controls. DVS (Digital Vinyl System) support allows djay to be controlled with real turntables and vinyl control records — a feature that professional DJs require. For unsupported hardware, a MIDI Learn system allows custom mapping.

## Streaming Service Ecosystem

djay supports Apple Music, Spotify (restored late 2025, currently desktop-only), TIDAL, SoundCloud, Beatport, and Beatsource, providing access to over 100 million tracks across services. The multi-service approach — learned from the Spotify disruption — reduces catalog dependency on any single platform.

## Product Tiers

djay (free) serves beginners with core mixing features. djay Pro (subscription) adds Neural Mix, advanced Automix, hardware controller integration, and professional audio routing. Neural Mix Pro is a standalone stem separation and audio editing application for Mac, positioned as a studio production tool rather than a performance app.
