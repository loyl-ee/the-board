# Chris Eidhof — On Product

## Small, Well-Understood Components

Eidhof's product philosophy centers on building systems from small, well-understood pieces rather than reaching for large frameworks. His Swift Talk series demonstrates this repeatedly: parsers, routing systems, form libraries, and layout engines are built from scratch, not because external solutions don't exist, but because understanding the implementation gives developers better judgment about every decision that follows.

This is not anti-framework dogmatism. It is a pedagogical and engineering conviction: before you trust an abstraction, you should be able to explain what it does. Building from first principles develops the instincts to recognize when a framework is the right tool and when it is adding complexity you don't need.

## Plain Swift Over Heavy Frameworks

A thread running through objc.io's content since 2013 is a preference for idiomatic Swift over framework-heavy solutions. The *Functional Swift* book builds a type-safe Core Image wrapper, a diagrams library over Core Graphics, and a spreadsheet — all using the language itself rather than third-party dependencies. The choice is deliberate: "it's about doing functional programming" with reasoning that while frameworks evolve rapidly, programming principles have been stable for decades.

Eidhof's analytics post ("Swift Analytics," chris.eidhof.nl) is a model of this thinking applied to product decisions: he works through five different approaches to the same problem, from the simplest inline solution to the most flexible protocol-based design, and recommends choosing "the simplest possible solution for your problem and team." The hierarchy matters — start at the bottom, only climb toward complexity when forced.

In his Swift Talk episodes on architecture, the same pattern appears. He has explored The Elm Architecture, MVVM, and MVC — not to declare a winner but to show the trade-offs embedded in each choice. His *App Architecture* book (co-authored with Matt Gallagher and Florian Kugler) surveys common and experimental patterns with similar neutrality, equipping developers to make their own informed decisions.

## Building Things to Understand Them

Eidhof built the SwiftUI Field Guide (2024) by re-implementing significant portions of SwiftUI's layout algorithm in TypeScript to make interactive visual examples possible. The effort was substantial — not a thin wrapper over documented behavior, but a genuine re-implementation. The result was both a better teaching tool and a substantially deeper personal understanding of the system being taught.

This is a consistent pattern: his `tea-in-swift` GitHub repository implements The Elm Architecture in Swift, not because he was shipping a product that needed it, but to understand what the pattern actually means in Swift's type system. His "OLD-functional-view-controllers" repository is an exploration of whether view controllers can be composed functionally — an experiment in understanding, not a production library.

## Small Tools and Shipping

Eidhof is drawn to small, shippable tools that solve real problems for himself or a narrow audience. In early 2026, he and collaborator Nathan built Pancake — a Mac app for static site generation featuring a native text editor, bundled dependencies, and an integrated publish server. The project was scoped to one month. It did not receive a public launch. They shared it with close friends and acknowledged the scope was too ambitious for the timeline. This is characteristic: he ships incomplete things intentionally, learns from the constraint, and moves on.

His `TerminalUI` library (323 GitHub stars) builds command-line user interfaces in Swift. His `github-issues` app is a Swift-native GitHub issue viewer. His `pomotv` is a simple Pomodoro timer. These are tools he made because he wanted them — not products designed for a mass market.

The "Dynamic Type Package" he highlighted in his 2024 review is the clearest articulation of his product sensibility: "the simplest and most useful" code he wrote that year. It enables iOS-style dynamic type scaling across presentations and internal tools. Small surface area. Solves one thing completely. Ships.

## Product Philosophy in Teaching

objc.io and the SwiftUI Field Guide are themselves products, and Eidhof has thought carefully about their design. The Field Guide is free and interactive — his explicit wish was that SwiftUI documentation would be "way more visual and interactive." The workshop curriculum is custom-tailored to each company's codebase and product challenges. The Swift Talk series includes transcripts and downloadable source code alongside the video — multiple formats for the same content, because different people learn differently.

The product instinct here is: know exactly who you are building for (experienced Apple platform developers who want to go deep), don't dilute the product trying to serve everyone, and keep improving based on direct feedback.

## Known Limits

Eidhof's product thinking is strongest in the technical layer. He does not write extensively about distribution, marketing, or scaling products to mass-market audiences. His tools are typically built for developers, not consumers. His product intuitions are valuable for developer tools, technical content platforms, and anything requiring strong API design — less applicable to products where the primary challenge is acquisition, conversion, or retention at consumer scale.
