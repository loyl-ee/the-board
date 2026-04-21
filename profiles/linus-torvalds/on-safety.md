# Linus Torvalds — On Safety

## The Original Security Philosophy

For much of Linux's early history, Torvalds held a position on security disclosure that was controversial and, in some ways, remains so. His stated personal preference was for immediate public disclosure — fixing security bugs in the open, committing to the public git repository without embargo. He acknowledged this explicitly: if he knew about a security bug, he would fix it and commit it publicly right away.

This stance was grounded in his general distrust of embargoes. He has said he personally does not like embargoes and does not think they work. His reasoning: the fix, once committed publicly, is the notification. Giving advance notice to vendors and coordinating a release window creates a period where the vulnerability is known to some parties but not patched for users. Torvalds found this window worse than the immediate exposure of a public fix.

## The Tension with Security Researchers

This position put him in conflict with the security research community, which generally advocates for coordinated disclosure — notifying affected parties privately, giving them time to prepare patches, and announcing simultaneously with the patch release. The security community's argument is that immediate public disclosure gives attackers a window between disclosure and patch deployment where real harm can occur.

Torvalds' response, documented in various mailing list and blog exchanges, was that the Linux kernel's rapid update cycle made this window small, and that embargoes create their own information security problems — a wider circle of people who know about the vulnerability before users are protected.

## Evolution: The Ethics of Critical Infrastructure

As Linux became genuinely critical infrastructure — powering hospitals, financial systems, communication networks, and national security applications — the stakes of Torvalds' disclosure philosophy changed. A kernel vulnerability that is announced before all major distribution vendors have prepared updates creates a window of exposure for systems that cannot be rapidly patched.

The Linux kernel's actual security practice has evolved over time to accommodate coordinated disclosure for significant vulnerabilities, even while the formal kernel development process remains highly public. This reflects a pragmatic adaptation: the original philosophy assumed a relatively small, technically sophisticated user base that could update quickly. The current user base is neither small nor uniformly sophisticated.

Torvalds' 2024 interview with The New Stack addressed modern security concerns, including the xz-utils backdoor incident. He acknowledged that trust remains fragile and that "how to figure out when [trust is] being violated is an open problem." His encouragement was drawn from the community's rapid detection: "In both cases, they were actually really caught fairly quickly" — suggesting that open source's many-eyeballs property functions as a security feature over time.

## Security Through Obscurity vs. Open Development

Torvalds has maintained a consistent position against security through obscurity — the idea that keeping code private improves security. His view is that open code can be audited, fixed, and improved by anyone who finds a flaw, while proprietary code has no such correction mechanism. The Linux kernel's public development model is, in his view, a security asset, not a liability.

He has also been critical of organizations that treat security as a domain where normal engineering principles do not apply. His comment about the OpenBSD project (known for aggressive security-first development) — that their approach represents a kind of absolutism that ignores the tradeoffs inherent in all engineering decisions — reflects his position that security must be weighed against performance, flexibility, and usability, not treated as an absolute that overrides all other considerations.

## The 2018 Code of Conduct: Safety of Contributors

The most significant change in Torvalds' public behavior came in September 2018, when the Linux kernel adopted a Contributor Covenant-based Code of Conduct, replacing the brief "Code of Conflict" that had been in place since 2015.

In his release notes for Linux 4.19-rc4 (LKML, September 16, 2018), Torvalds posted a substantive apology: "My flippant attacks in emails have been both unprofessional and uncalled for. Especially at times when I made it personal." He acknowledged: "This is not an emotional 'I am just not an emotionally empathetic kind of person and that probably doesn't come as a big surprise to anybody.'" He announced he was taking a break from kernel development to "get some assistance on how to understand people's emotions and respond appropriately."

The background was an *Ars Technica* article and *New Yorker* inquiry about his conduct, plus confrontations from community members about his communication patterns over decades. Torvalds returned to kernel development after Linux 4.19's October 2018 release.

The apology and Code of Conduct addressed a real safety problem in the kernel community: that Torvalds' pattern of personal attacks in code reviews had driven contributors away from the project. The harm was documented and the change was genuine, though critics questioned whether a single individual's communication style should require a project-wide governance document to address.

His post-2018 conduct has been notably different in tone, though he has acknowledged in subsequent interviews — including a 2018 BBC interview — that the change requires ongoing effort: "I'll never be cuddly but I can be more polite."
