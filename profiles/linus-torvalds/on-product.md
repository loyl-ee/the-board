# Linus Torvalds — On Product

## Backwards Compatibility as Sacred Commitment

The closest thing Torvalds has to a product religion is the rule that the Linux kernel must not break userspace. This has been stated publicly many times, most famously in a 2012 kernel mailing list message that became known by its subject line: "WE DO NOT BREAK USERSPACE!"

The principle is: if a change to the Linux kernel breaks a program that was working before, the change is a kernel bug. Not the application's bug. Not a documentation problem. A kernel bug. This is true even if the application was relying on undocumented behavior, even if the application was technically incorrect in what it was doing, even if fixing the regression would be elegant. If users in the real world relied on a behavior, that behavior is now part of the contract.

This stance has real engineering costs. It means supporting ancient interfaces long after they should have been retired. It means carrying code that exists only to preserve compatibility with software no one has maintained in a decade. Torvalds accepts these costs because he believes the alternative — a kernel that breaks things — would undermine the entire value proposition of Linux as infrastructure. "When the choice is between userland compatibility and better adherence to theoretical documentation of the kernel interface, tie goes to userland compatibility." Stability is the product.

## The Monolithic Kernel vs. Microkernel Debate

In January 1992, Andrew Tanenbaum (creator of MINIX) posted to comp.os.minix that "Linux is obsolete." His argument: monolithic kernels are an outdated design. Microkernels, which place most services outside the kernel, are the theoretically correct architecture for reliability and portability.

Torvalds replied that Tanenbaum's MINIX had design flaws, that monolithic kernels were faster in practice, and that the theoretical elegance of microkernels had not translated into better real-world operating systems. He acknowledged the theoretical argument — "I find the microkernel design superior from a theoretical and aesthetical point of view" — but rejected the practical conclusion.

The debate was never cleanly resolved theoretically. But Linux's subsequent history is a strong empirical argument for Torvalds' position. The kernel's monolithic architecture, continuously evolved, scaled to run on everything from embedded chips to the world's fastest supercomputers. MINIX itself became notable later primarily as the operating system Intel apparently embedded covertly in the Management Engine of their processors — a different kind of legacy than Tanenbaum envisioned.

## Git as Problem-Solving, Not Vision

Git was not designed as a product. It was designed as a solution to a specific, urgent problem: after BitKeeper revoked the free license Linux kernel developers were using in April 2005, Torvalds had no acceptable version control system available. In the Google Tech Talk he gave later that year, he described his design approach as asking himself "what would CVS never ever do" and then doing that. CVS was the dominant system; Torvalds considered it fundamentally flawed.

The resulting design centered on three things. First, correctness — data integrity guaranteed by SHA-1 content hashing: "If you put your data in git, you can trust the fact that five years later you can verify the data you get back is exact." Second, distribution — every repository is a complete history, not a checkout of a central store. Third, performance — merging and branching needed to be cheap so that the Linux kernel's development workflow (many parallel branches, frequent merges) remained tractable.

Git's original command interface was notoriously unintuitive. Torvalds has acknowledged this without particular regret. His position is that the underlying data model is sound and clean — "the core model is both very simple and very powerful" — and that the interface complexity reflects real complexity in the problem domain, not gratuitous design failure. A simpler interface would represent a simpler model with less capability.

## The "Nobody Should Start a Large Project" Principle

Torvalds has articulated what might be the most counterintuitive advice for anyone building something: "Nobody should start to undertake a large project. You start with a small trivial project, and you should never expect it to get large." (*Linux Times*, October 2004). This is not false modesty. He is describing how Linux actually happened — it began as an educational exercise in understanding his new hardware. The lesson he draws is that large projects built with large ambitions often fail because the ambition exceeds the feedback loop. Small projects that solve real problems grow because they attract people who have the same problem.

## What Makes a Technical Product Last

Across his public statements, three qualities emerge as Torvalds' criteria for technical products that endure. First, a clean core design that scales — both Linux and Git have this in common, with early architectural decisions that have proven extensible rather than limiting. Second, genuine backwards compatibility discipline — systems that break their users lose their trust irreversibly. Third, openness that attracts contributors who have a stake in quality, not just features — the GPL model creates this through structural incentives, not appeals to altruism.
