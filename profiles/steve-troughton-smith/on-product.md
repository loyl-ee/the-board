# Steve Troughton-Smith — On Product

## Building for Developers as Users

The clearest thread through Troughton-Smith's product work is building for people who understand what they are using. His apps tend toward the technical end of the user spectrum — Scarlet targets indie developers managing their own projects, Broadcasts targets people who know what internet radio streams are and want control over them, Pastel targets designers who work with color at the code level. He does not build for the casual App Store browser; he builds for someone with a specific workflow problem and the sophistication to appreciate a precise solution.

This shapes his product decisions in concrete ways. Scarlet's data model — a plain text file that lives inside your project directory and gets version-controlled with your code — is a choice that most product managers would reject as too technical. It is also, for the right user, exactly right.

## Exposing Underlying Complexity Clearly

A consistent trait in his tools and sample code is the decision to surface complexity rather than hide it. His Mac Catalyst sample code library does not paper over AppKit's differences from UIKit; it shows developers how to bridge them explicitly. His UIFloat scaling utility for Catalyst does not abstract away the difference between iOS and macOS layout metrics; it makes the distinction legible and controllable.

This reflects a product philosophy closer to a Unix tool than to a consumer app: the right interface makes the underlying system understandable, not invisible. For users who are themselves engineers, this is more respectful than false simplicity.

## Iteration Driven by Platform Evolution

His products are explicitly tied to what Apple's platforms can do at a given moment, which means they evolve in response to platform changes rather than in response to user feature requests alone. When Mac Catalyst gained new capabilities, he updated his apps and published sample code showing how to use them. When Apple introduced Stage Manager, he immediately assessed what its absence of developer APIs meant for his and others' apps.

This platform-tracking approach has a downside: it means his products are sometimes behind when Apple moves slowly, and he is vocal about that frustration. But it also means his products reliably use the right primitives for each platform moment rather than accumulating layers of workarounds.

## The Grace App: Product That Matters Beyond the Platform

Worth noting as context for his broader product philosophy is Grace, the autism communication app he built in collaboration with Lisa Domican. Grace replicates the Picture Exchange Communication System using iPhone photos, enabling non-verbal people to build and exchange communication cards independently. It won the 2010 Irish Web Awards and the UN World Summit Award Mobile, and has been used in speech therapy and autism education contexts worldwide.

Grace represents a different register of his product work — not platform archaeology, but direct impact on how people communicate. It shows that his product instincts extend well beyond developer tooling and into human-centered utility at its most basic.

## On Documentation as Product

In his 2020 interview with iMore, Troughton-Smith named documentation as his primary ask of Apple: "Apple has been racing forward...and has left documentation by the wayside for years." He treats good documentation as a product in its own right, one that multiplies the value of every API and framework. His own sample code library is, in effect, the documentation he wished Apple had written — a product built to fill that gap.
