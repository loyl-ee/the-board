# Linus Torvalds — On Architecture

## Simplicity as the Primary Architectural Value

Torvalds' architectural philosophy begins with a single, non-negotiable requirement: the architecture must be understandable by the engineers who maintain it. An architecture that requires a diagram to explain is an architecture that will be misunderstood. An architecture that a new engineer cannot trace from first principles in a day is an architecture that accumulates bugs.

His position on complex distributed architectures: they are appropriate at the scale of Google or Amazon, and inappropriate for almost everything else. The engineering cost of distributed systems — eventual consistency, network partition handling, distributed transactions, debugging tools — is genuinely high. Accept that cost only when the alternative (a single server, a single process) is genuinely inadequate.

## Layered Architecture: No Upward Dependencies

The kernel's architecture is explicitly layered: hardware drivers at the bottom, memory management above, file systems and networking above that, system calls at the top. Dependencies flow strictly downward — a higher layer may depend on a lower layer, but a lower layer may never depend on a higher one.

This constraint is not aesthetic. It prevents the circular dependencies and spaghetti couplings that make large systems unmaintainable. Any system above a certain size benefits from an explicit layering discipline: define the layers, define what depends on what, and enforce the constraint in code review.

## The File System as an Architectural Analogy

Torvalds' architectural insight for Git — which he designed in two weeks — was to treat version history as a content-addressed file system. Every file, directory, and commit is a cryptographic hash of its contents. The history graph is an append-only tree of these hashes. The architecture is almost embarrassingly simple, and it is correct.

The architectural lesson: look for the simplest data model that is both correct and sufficient. Git's data model is so simple that the specification fits in a few pages. That simplicity is why Git is reliable, why it can be implemented in any language, and why it has lasted for two decades.

## Never Optimise Prematurely, Never Ignore the Dominant Term

Torvalds has a specific position on performance architecture: never optimise prematurely (do not add complexity before you have measured where the time is spent), but also never ignore the dominant term (if the algorithm is O(n²) and n is large, optimising the constant factor is wasted effort).

The architectural discipline: profile before optimising, and optimise at the level where the dominant cost is. Application-level algorithm choice dominates micro-optimisation. System call overhead dominates most application-level code. Get the big things right before tuning the details.

## Git's Architecture as an Engineering Reference

The architecture Torvalds designed for Git has three layers: the object store (content-addressed blobs, trees, commits, tags), the index (a staging area that mediates between the working tree and the object store), and the working tree (the files the user edits). The three layers have well-defined interfaces between them.

This three-layer architecture makes Git operations composable: any operation that is possible by combining layers (plumbing commands) can be composed into a higher-level operation (porcelain commands). Engineers who understand the architecture can build their own tools on the plumbing.

## Sources
- [Git data model documentation](https://git-scm.com/book/en/v2/Git-Internals-Git-Objects)
- [Linux kernel architecture documentation](https://www.kernel.org/doc/html/latest/)
- [Linus on software architecture — various LKML posts](https://lkml.org/)
- [Linus on Git design — Google Tech Talk, 2007](https://www.youtube.com/watch?v=4XpnKHJAok8)
