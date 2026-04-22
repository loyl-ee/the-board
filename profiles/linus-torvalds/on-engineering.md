# Linus Torvalds — On Engineering

## Code Quality Is the Only Metric That Matters

Torvalds has an unusually direct relationship with code quality: he reads it, judges it, and publicly rejects it when it fails to meet his standards. His Linux kernel mailing list posts are a documented record of what he considers good and bad engineering — blunt, specific, and unsparing. The standards he applies are not about style; they are about correctness, clarity, and long-term maintainability.

His core position: complicated code is almost always wrong code. If a patch is hard to read, it is probably hard to reason about, and therefore likely to contain bugs. Clever tricks that save ten lines at the cost of comprehensibility are not clever — they are a future bug. He has written that he prefers "boring" code: code that does what it says, says what it does, and contains no surprises.

## Never Break Userspace

The principle Torvalds holds most rigidly is backward compatibility for userspace: user-facing APIs, syscall behaviour, and binary interfaces must never break. If a kernel change causes a userspace application to stop working — even an application that is itself wrong — the kernel change is reverted. This has been a hard rule for decades.

The engineering wisdom here generalises far beyond the kernel: once your code is depended upon, that dependency is your responsibility. Changing an API to be "more correct" while breaking callers is not a quality improvement — it is a failure of stewardship. Design APIs knowing they will be permanent. Deprecate slowly. Never delete.

## Git as an Engineering Philosophy

Torvalds created Git in 2005 after becoming frustrated with the available version control systems. The result was a distributed, cryptographically content-addressed system that treats commits as immutable objects and history as an append-only graph. Git's design reflects his engineering values: every commit is a complete, self-contained snapshot; history is never rewritten in shared repositories; the data model is simple and correct even if the interface is initially intimidating.

The "perfect commit" is implicit in Git's design: a commit should contain a complete logical change, not a work-in-progress save. The commit message should explain *why*, not just *what*. The engineering discipline of small, complete, well-described commits is not bureaucratic overhead — it is how you maintain an auditable history of every decision.

## Code Review as Engineering Culture

Torvalds reviews kernel patches personally and in public. His reviews are famous for their directness and for the specificity of the feedback — not "this is bad" but "this pointer arithmetic is wrong for the following reason." The kernel development model requires every change to be justified in the commit message and to survive review from maintainers before merging.

The engineering principle behind this process: no individual is infallible, no change should skip scrutiny, and the person who knows most about the impact of a change is often not the person who wrote it. Code review is not about catching typos; it is about sharing understanding.

## Simple Systems Outlast Clever Ones

Torvalds is consistently sceptical of architectural complexity. He has criticised C++ features that obscure the memory model, object-oriented abstractions that hide what is actually happening, and distributed systems that solve problems that a simpler single-process design would not have. His preference for C in the kernel is partly historical, but also deeply principled: in C, there are no hidden allocations, no invisible copy constructors, no magic. The engineer knows what the machine is doing.

This generalises to architecture: systems that a new engineer can understand by reading the code are more durable than systems that require a diagram. The best architecture is the one that makes the correct path obvious.

## Sources
- [Linux Kernel Mailing List archives](https://lkml.org/)
- [Linus on Git design — Google Tech Talk, 2007](https://www.youtube.com/watch?v=4XpnKHJAok8)
- [Linus on C vs C++ — lkml.org, 2007](https://lkml.org/lkml/2007/1/11/225)
- ["Never break userspace" — documented kernel development policy](https://www.kernel.org/doc/html/latest/process/stable-api-nonsense.html)
