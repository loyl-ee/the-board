# Philosophy — Mattt Thompson

## Documentation as a First-Class Citizen

Thompson's most distinctive belief is that documentation is not supplementary — it is constitutive of the software itself. He has written that "code structure and organization is a matter of pride for developers. Clear and consistent code signifies clear and consistent thought." This treats documentation as an ethical signal: messy or absent documentation is not an efficiency problem, it is a character problem.

In his NSHipster article on Objective-C documentation, he argued that even "a small amount of effort can yield significant benefit to others" and that following established documentation conventions allows any developer to produce material rivaling Apple's official guides. He recommended studying existing documentation before writing your own — "in order to get a sense of the correct tone and style" — positioning documentation as a learnable craft requiring attentiveness to existing conventions. His practical advice: adopt good habits early, before tooling is perfect, because documentation is an ongoing discipline rather than a release-gate task.

## The Craft of Naming

Thompson has an obsessive relationship with naming — not as a stylistic preference, but as a claim about clarity of thought. He is fond of quoting the programmer's adage that "there are only 2 hard things in programming: naming, cache invalidation, and off-by-one errors" (itself a joke about precision). His NSHipster essays routinely interrogate why a framework was named as it was, what the name reveals about how Apple's engineers understood the problem, and where naming choices created conceptual confusion for users downstream. His essay on `TimeInterval`, `Date`, and `DateInterval` captures this precisely: "Our limited understanding of time is reflected in — or perhaps exacerbated by — the naming of the Foundation date and time APIs."

## Understanding Tools Before Using Them

The entire NSHipster project is an operationalization of this belief. Rather than teaching developers the minimum interface for a framework, Thompson consistently documents the full semantics, history, edge cases, and design tradeoffs. His conviction is that shallow familiarity creates fragile code — that understanding *why* `NSPredicate` works the way it does (he called it "one of the jewels of Cocoa") is what separates developers who use APIs correctly under pressure from those who don't. His talk "Software Design and Eclecticism" (2014) made this explicit: deep problem-domain understanding — in beer color formulas, calendaring standards, shoe-sizing conventions — is what produces excellent software models. Eclecticism, in his framing, is not a hobby but a prerequisite.

## The Humanist in Programming

Thompson dropped his CS major to pursue Philosophy, Linguistics, and Art. This was not a detour — it is the source of his most distinctive contributions. He has written about empathy as a professional skill: "Everything you need to succeed as a software developer extends from a conscious practice of empathy." His NSHipster article "Empathy" (March 2014) argued that online developer communities strip out the non-verbal cues that humanize communication, and that this deficit requires conscious compensation. Before engaging with someone online, he recommended pausing to visualize the encounter in person and asking whether you would be proud of your conduct.

This humanist orientation shapes his API criticism. When he noted that "Key-Value Observing has the worst API in all of Cocoa," the complaint was not merely technical — it was about what a bad API communicates to a developer about their relationship to the framework's creators: that the developer's time and confusion are not worthy of care.

## Obscurity as Professional Maturity

NSHipster's premise — that deep familiarity with *obscure* corners of an API is a mark of professional maturity, not pedantry — is central to Thompson's philosophy. He built the site on the conviction that the developers who will serve their users best are those who have read past the first Google result, who know what `CFStringTransform` can do, who understand the behavior of `NSNull` in collection operations. Curiosity about the weird corners of a platform is, for Thompson, a sign that a developer has internalized craft rather than just shipping product.

## Sanity Over Cleverness

His NSHipster book articulates the Principle of Least Surprise as "a general approach to software that celebrates sanity over cleverness: clear intent, reasonable defaults, and control." This is a conservative philosophy in the original sense: it prefers legibility, predictability, and explicit communication over elegant tricks. It explains why his APIs tend toward expressive naming over compact syntax, why his documentation spends time on error conditions, and why he has consistently praised frameworks that respect the developer's need to understand what is happening.
