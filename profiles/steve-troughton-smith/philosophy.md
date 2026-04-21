# Steve Troughton-Smith — Philosophy

## Core Belief: Platforms Have Untapped Potential

The animating conviction in Troughton-Smith's work is that Apple's platforms — especially iPad — are routinely constrained far below their technical ceiling. He has spent years documenting the gap between what the hardware can do, what the OS privately does, and what Apple publicly exposes to third-party developers. This is not nostalgia for a freer era: it is a technical argument, made with evidence, that the platform restrictions in place are choices, not necessities.

His 2024 "iPad Pro Manifesto" — a near-verbatim update of a manifesto he first wrote in 2019 — makes this explicit. The fact that the same complaint required no meaningful revision over five years is itself the thesis. iPad silicon was delivering M-class chip performance while the OS remained locked at roughly the capability level of iPhone OS writ large.

## Reverse Engineering as Platform Advocacy

Troughton-Smith treats reverse engineering not as hacking but as scholarship. His firmware analysis work — HomePod, beta SDK toolchains, App Store Connect's internal linker — has functioned as a form of public technical journalism, surfacing facts about Apple's product roadmap that Apple's own PR would not confirm. His methodology is careful: he works with artifacts Apple has made available (firmware bundles, open-source releases, developer tooling) rather than bypassing security boundaries to extract proprietary data.

He is explicit that this work serves the developer community: by demonstrating what private APIs and hidden capabilities exist, he builds the case for Apple to make them public. His extensive Mac Catalyst sample code library was a direct response to Apple's own insufficient documentation — if Apple wasn't going to show developers how to build proper Mac apps using UIKit, he would do it himself.

## The "Platform as Promise" View

Troughton-Smith frames Apple's platforms as promises made to both developers and users. When the hardware ships with M-series silicon but the OS refuses to allow JIT compilation for third-party language runtimes, or lacks APIs for Stage Manager window management, or restricts virtualization that the chip can plainly support, Apple has broken a promise implied by the hardware. His writing returns to this pattern repeatedly: iPad hardware is "writing checks that its OS simply can't cash" (highcaffeinecontent.com, 2024).

This view makes him a strong critic of what he calls Apple's "first-party advantage" — the pattern of Apple using private APIs and internal-only entitlements to ship features in its own apps that third-party developers cannot replicate. When Apple's own Playgrounds can compile and deploy apps to the local device, but no third-party IDE can, the restriction is not a security necessity but a competitive moat.

## Skepticism of Apple's Regulatory Compliance

His philosophy extends to the business and legal layer. He was an early and persistent critic of Apple's DMA compliance approach in the EU, noting that "Apple believes it is complying with the letter of the law" while the European Commission made clear Apple needed to comply with the spirit as well (Mastodon, March 2024). He identified Apple's Core Technology Fee as a mechanism that preserved the economic reality of the old App Store monopoly while superficially complying with interoperability requirements.

## Optimism Grounded in Technical Reality

Despite the criticism, Troughton-Smith is not anti-Apple. He remains committed to the platform professionally and personally, and his assessments of technologies like Mac Catalyst are carefully balanced: "Mac Catalyst is in a great place; it has improved substantially every year since its introduction" (highcaffeinecontent.com, 2022), even as he catalogs its remaining shortfalls. He believes the platforms can and should improve — his advocacy is aimed at accelerating that improvement, not at abandoning ship.

His post-2025 engagement with AI-assisted development tools reflects the same empirical temperament: he spent a month working intensively with OpenAI's Codex, documented what it could and could not do in careful detail, and landed on a nuanced position: "I could not have done this without the AI. The AI could not have done this without me." He applies the same framework to platform questions — neither utopian nor cynical, but precise about what is actually happening.
