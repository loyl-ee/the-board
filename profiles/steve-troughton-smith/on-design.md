# Steve Troughton-Smith — On Design

## The Mac-iPad Continuum

Troughton-Smith has long argued for a tighter design continuum between macOS and iPadOS — not convergence for its own sake, but the recognition that the same underlying frameworks and interaction primitives should be surfaced consistently across both platforms. His investment in Mac Catalyst is grounded in this belief: that UIKit's evolution toward "Optimize for Mac" was a meaningful step toward a unified platform design language, even if imperfectly executed.

He tracks this at the code level: when Apple ships a new Catalyst capability, or when it quietly stops using it in first-party apps, he notices and reports. His June 2025 reaction to the macOS 26 "Liquid Glass" redesign was pointed: "The macOS 26 redesign is unhinged. I guess I'm not the only one questioning the continued value of tailoring my Mac Catalyst UIs to the Mac — Apple has thrown out its own NSToolbars too." (Mastodon, June 2025). Apple redesigning away the conventions he had carefully built toward was a design trust problem, not just a technical one.

## Multi-Window and Stage Manager

Troughton-Smith was a vocal proponent of proper multi-window support on iPad long before Apple shipped it, and equally vocal about Stage Manager's failure to deliver what he had hoped for. His criticism was not that multi-window was a bad idea — he had argued for it for years — but that Stage Manager was shipped without developer APIs for the core functionality it introduced.

As he described it: "Stage Manager wasn't provided as an opportunity to make our apps better, it was inflicted on developers in a way that harmed the developer, and user, experience." (highcaffeinecontent.com, March 2026). Developers could not set window sizes, position windows, provide resize limits, or offer "Open in New Window" context menu items — the hooks that would make Stage Manager feel native were simply absent.

His further critique was conceptual: Stage Manager's windows and sets lacked names or a legible model. "The lack of names suggests to me that Stage Manager is not conceptually complete," he observed. A design feature that cannot be named is one that has not been thought through.

## Pointer Support and Keyboard-First Design

He discovered early references to pointer (trackpad/mouse) support in iPad firmware before Apple announced it, and was a consistent advocate for its introduction. When Apple did ship pointer support in iPadOS 13.4, he welcomed it but noted immediately that it was not enough — without APIs for apps to define pointer interaction regions, hover states, and context menus consistently, the feature remained an Apple-managed system feature rather than a developer-accessible design primitive.

## Views on Apple's Design Direction Post-Liquid Glass

The macOS 26 / iOS 26 Liquid Glass redesign prompted sharp commentary. Troughton-Smith observed that "Podcasts and Music on macOS 26 are a pretty extreme example of the new design" and raised concerns that the redesign had been "developed in a vacuum away from third parties, accessibility experts and engineers." His concern was less about the aesthetic and more about the implications for third-party app design coherence — when Apple abandons its own design conventions without APIs for third parties to follow, the platform design becomes fragmented.
