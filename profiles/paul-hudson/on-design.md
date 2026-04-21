# Paul Hudson — On Design

## Apple's Human Interface Guidelines as the Default Framework

Paul Hudson teaches iOS design from the perspective that Apple's Human Interface Guidelines (HIG) are not suggestions — they are the contract between a developer and the platform. His tutorials consistently direct learners to use native controls (UIButton, UITableView, the standard SwiftUI components) rather than custom implementations wherever possible, because native controls carry HIG compliance, accessibility support, and platform consistency as built-in properties.

His reasoning is practical: native controls receive updates from Apple automatically. A custom implementation requires the developer to maintain every behavior the native control would have provided for free, including all accessibility behaviors, dark mode support, Dynamic Type scaling, and platform conventions. For most app use cases, the cost of that maintenance is not justified.

## Accessibility as a Design Requirement

Hudson treats accessibility not as a visual design problem but as a product completeness requirement. An app that does not work with VoiceOver is, in his view, an incomplete app — not because of legalistic compliance obligations, but because real people depend on it to use their devices.

This is reflected in how he structures his teaching. Accessibility is not a chapter at the end of a course as an optional extension. It appears throughout his tutorials as part of the normal workflow of building an interface. When he teaches a list view, he teaches how to label it for VoiceOver. When he teaches an image, he teaches when to mark it as decorative.

## Design Philosophy on His Own Site

Hackingwithswift.com is itself a design artifact. The site presents thousands of tutorials, multiple books, code examples, and news without visual complexity. The design is functional and deliberately minimal — text-heavy, clearly organized by topic, with navigation that surfaces specific answers to specific questions quickly.

The design also reflects his content-first philosophy: the format serves the tutorial, not the other way around. Articles are long when the topic requires it, short when it does not. Code is presented in clear blocks with the ability to copy. Video accompanies articles when video adds value (demonstrating a technique in motion), but text remains available for those who prefer it or need to copy code.

## Tutorial Design: Clarity Over Style

Hudson designs his tutorials with a consistent internal structure: set up the problem, write the code, explain what happened, explain why it matters. This structure is a design decision — it creates a predictable reading experience that lets learners move faster because they know what format they are navigating.

He has also built systems to keep design quality high at scale. The SwiftUI by Example reference book is organized so that any learner can search a specific technique and find a working answer without needing to read everything that precedes it. This is an information architecture decision that privileges the returning user and the searcher over the sequential reader.

## What He Does Not Engage With

Hudson does not write extensively about graphic design, brand identity, motion design, or visual design systems beyond what Apple's own HIG covers. His design focus is almost entirely on interface design at the code level — how to implement layouts, controls, and interactions correctly — rather than the upstream visual design decisions that precede implementation.

## Sources

- hackingwithswift.com/books/ios-swiftui/accessibility-introduction
- hackingwithswift.com (site design)
- hackingwithswift.com/quick-start/swiftui/introduction-to-accessibility-with-swiftui
- github.com/twostraws/Ignite (accessibility built into HTML output by default)
