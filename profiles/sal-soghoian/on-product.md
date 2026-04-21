# Sal Soghoian — On Product

## Automator as a Product Philosophy

Automator is Soghoian's most complete expression of his product thinking. The core insight behind it was architectural: instead of building a fixed scripting language that users had to learn, build a library of discrete, reusable actions that could be combined visually into workflows. Each action does one thing. Actions pass their output to the next action in sequence. The user builds a workflow by selecting actions from a library and dragging them into an ordered list — no syntax, no compilation, no debugging environment required.

This design philosophy contains several overlapping product decisions. First: lower the floor without raising the ceiling. Automator was explicitly designed so that a user who had never written code could build a workflow that previously required scripting knowledge. But it also integrated directly with AppleScript and shell scripts as native action types, meaning expert users could drop arbitrary code into the same visual pipeline. The tool served beginners and experts in the same interface.

Second: make the library the product. Automator shipped with hundreds of actions covering Apple's own applications, and third-party developers could write actions for their apps using a published API. The quality and breadth of the action library determined the tool's power. Soghoian understood that Automator would only be as useful as the developers who built actions for it — which meant that developer adoption was itself a product problem, requiring outreach, documentation, and evangelism.

## Scriptability as a First-Class Feature

Soghoian's product philosophy holds that automation support is not a feature that gets added after the core application is built. It is a design consideration that shapes the application's architecture from the beginning. An application that is scriptable has to have a coherent internal model — objects with properties, events with parameters, data that flows across application boundaries. That internal model is also what makes the application understandable and predictable to users.

When developers treat scripting as an afterthought, the resulting AppleScript dictionary typically reflects the application's implementation rather than its user-facing model — exposing arbitrary internal identifiers instead of meaningful object relationships. Soghoian advocated for scripting dictionaries as product artifacts in their own right, designed to express what an application does at the same level of clarity as its user interface.

He has been explicit about the success condition for an automation tool: "The success of any automation tool requires the addition of granularity gained through integration with scripting languages, as well as widespread developer adoption of the tool's APIs in their applications." (Rebooting interview, 2023.) This is a product manager's statement: tool adoption and ecosystem participation are the metrics that matter, not the technical quality of the underlying implementation.

## Actions as Components

A distinctive feature of Automator's design is that actions are not scripts — they are components. They are compiled bundles with defined input types, output types, user-configurable parameters, and error handling. This architecture gives Automator workflows a composability that raw scripting lacks: any action that outputs images can connect to any action that accepts images, regardless of which applications the actions belong to. The system enforces type compatibility and presents the user with only valid connections.

This component model anticipated the approach that would later define iOS Shortcuts: discrete actions with typed data flowing between them, assembled visually into workflows. Soghoian has acknowledged Shortcuts as a genuine successor to Automator's design principles, noting that "Shortcuts has the potential to become a universal automation tool, especially as it integrates with scripting languages." (Rebooting interview, 2023.)

## The Role of Scripting Languages Within Visual Tools

One of Soghoian's most nuanced product insights is that visual workflow builders and scripting languages are not alternatives — they are complements. Automator's "Run AppleScript" and "Run Shell Script" action types exist because visual building blocks can never cover every case, and forcing users out of the tool entirely when they need to do something custom breaks the workflow experience. The right product design includes an escape hatch to full scripting that integrates naturally into the visual layer.

This same principle applies to Shortcuts: its ability to run scripts and integrate with external tools is what separates it from a simple macro recorder. The visual metaphor handles the common cases; the scripting integration handles everything else.

## Omni Automation as Post-Apple Product Work

After leaving Apple, Soghoian worked with The Omni Group to design Omni Automation — a JavaScript-based scripting framework embedded directly in OmniFocus, OmniGraffle, OmniOutliner, and OmniPlan. The framework runs the same scripts across iOS and macOS, with shared syntax and compatible APIs. This cross-platform consistency was a product goal Soghoian had not been able to fully achieve at Apple, where AppleScript remained Mac-only and iOS automation was fragmentary. Omni Automation represents his mature product thinking: scriptable from a console inside the application, cross-platform by design, shareable via standard URLs, and integrated with Shortcuts on both platforms.
