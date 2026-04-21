# Chris Eidhof — On Design

## Engineering and Design as Overlapping Territories

Eidhof does not position himself as a designer, and he does not write at length about visual or interaction design as a discipline separate from engineering. His relationship to design is practical: he is someone who builds tools, and building good tools requires thinking about the design of the interface — both the user interface and the programmer interface.

His most sustained engagement with design-as-design is in SwiftUI, where the framework's declarative model deliberately collapses the distance between visual specification and code implementation. In this territory, Eidhof has done serious thinking.

## SwiftUI as a Design System

Eidhof's work on *Thinking in SwiftUI* (with Florian Kugler) treats SwiftUI not just as a technology but as a design system with a specific philosophy: views are functions of state, layout is proposal-and-response, and the composition of modifiers forms a deterministic description of visual output. Understanding this system deeply means understanding how visual decisions map to code structures.

His "A Day in the Life of a SwiftUI View" presentation (chris.eidhof.nl) traces how written SwiftUI code becomes two tree structures — a view tree (ephemeral) and a render tree (persistent) — and how state is stored in the latter. This is not UX design, but it is the structural understanding that allows engineers to implement designs faithfully and debug visual regressions accurately.

## The Layout System as Design Language

Eidhof has invested more intellectual effort in SwiftUI's layout system than almost any other topic. The system works through a parent-child proposal mechanism: parents propose sizes to children, children report what they actually take. Modifiers like `aspectRatio` implement sophisticated two-step proposal strategies — proposing nil first to discover natural dimensions, then proposing constrained dimensions based on the result.

His Swift Talk has produced more than 219 episodes on SwiftUI (as of 2025), many of them exploring layout behavior in detail. The SwiftUI Field Guide (2024) translates this understanding into interactive visual documentation — sliders and animated diagrams that demonstrate the layout algorithm directly. Eidhof's stated motivation was that he wished SwiftUI's official documentation "would be like: way more visual and interactive."

This is an aesthetic position as much as a pedagogical one: he believes complex layout behavior should be *seeable*, not just described. That belief drove a significant engineering investment (re-implementing SwiftUI layout in TypeScript) in service of a visual and educational product.

## Custom Rendering and Exploration

Eidhof's GitHub includes experiments in building custom rendering systems — his diagrams library in *Functional Swift* builds a compositional API over Core Graphics. His `LiterateSwiftGUI` project explores GUI building in Swift. His UIKonf 2020 talk built a programming language interpreter in Swift. These are not products aimed at mainstream design workflows; they are explorations in what it means to design computation at the level of the language and rendering pipeline.

## Honesty About Scope

Eidhof does not hold strong opinions about visual aesthetics, branding, information architecture, or product design in the consumer sense. His engagement with design is engineering-forward: how does the system model design decisions in code? How does the layout algorithm translate visual intent into geometric output? These are important questions, but they are a subset of what "design" encompasses.

He works at the intersection where engineering and design overlap — in the semantics of layout, the composition of views, the structure of rendering pipelines. He does not write about typography, color theory, or brand identity. That gap should be acknowledged when pairing his perspective with decisions about visual identity or consumer-facing design direction.
