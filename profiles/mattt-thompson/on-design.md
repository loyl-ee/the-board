# On Design — Mattt Thompson

## Code as a Medium with Aesthetic Properties

Thompson's background in philosophy, linguistics, and art produces an unusual position: he treats code as an aesthetic medium, not merely an engineering substrate. This is not metaphor — he has consistently argued that the surface properties of an API (naming, parameter ordering, method signature length, return type conventions) carry aesthetic weight that affects how developers understand and use the software.

His NSHipster article on Objective-C's verbosity captures this elegantly: the language's long method names are not a defect but an aesthetic and semantic choice — the explicit naming of each parameter creates self-documenting code that reads closer to prose than to mathematical notation. He "learned to appreciate the beauty of the language and its frameworks" only after overcoming an initial aversion to Objective-C's distinctive syntax.

## The Beauty of a Well-Designed API Surface

Thompson's highest praise for a framework is consistently aesthetic: that it shows "thoughtfulness and a deep appreciation for understanding a problem in its entirety." His "Software Design and Eclecticism" talk (2014) used Apple's Foundation framework as a design gallery — surveying how `NSCalendar`, `NSFormatter`, `CFStringTransform`, and other types reflect genuine intellectual engagement with their problem domains. The design virtue being celebrated is not minimalism for its own sake but *fittedness*: the sense that the abstraction matches its domain at exactly the right level of generality.

His praise for `NSPredicate` as "one of the jewels of Cocoa" is aesthetic language. So is his condemnation of Key-Value Observing's API as the "worst in all of Cocoa." Both judgments are about whether the surface design honors or disrespects the developer's cognitive investment.

## NSHipster's Visual and Editorial Aesthetic

NSHipster as a publication embodies Thompson's design sensibility. The site is clean, typographically restrained, and content-forward — it does not use the visual complexity common in developer marketing. The editorial format is consistent: each article takes a single framework, type, or concept as its subject, explores it with genuine depth, and treats obscurity as a positive attribute rather than a warning sign. The Creative Commons BY-NC license is itself a design choice, signaling that knowledge sharing is built into the publication's identity rather than being an afterthought.

The weekly publication cadence (maintained from 2012 through 2015, then resumed in 2018) is a design constraint that forces concision and regularity — two aesthetic virtues Thompson applies to code as well.

## The Aesthetics of Alamofire's API

In his NSHipster article on Alamofire, Thompson directly discusses how Swift's language features enabled better API aesthetics. Swift's dot notation, trailing closures, and enum-with-associated-values changed what "beautiful" networking code looked like. The design conclusion: language features are not neutral — they create aesthetic affordances that good API designers take seriously. Alamofire's method chaining, for instance, was an aesthetic possibility that Objective-C's bracket syntax made awkward but Swift's dot syntax made natural.

## Gaps to Note

Thompson's design sensibility is almost entirely within code and technical writing. His public work has little to say about visual product design, brand identity, or the aesthetics of consumer interfaces. NSHipster's own visual design is serviceable but not a design showcase. His aesthetic contributions are most visible in the design of text: API surfaces, documentation, and written prose about technical subjects.
