# Linus Torvalds — On Backend Engineering

## Systems Engineering: Know What the Machine Is Doing

Torvalds' backend engineering philosophy comes from operating systems development — the lowest level of software engineering. His standard for backend code: the engineer must know what the hardware is doing. Memory allocation, cache behaviour, lock contention, system call overhead, and I/O scheduling are not implementation details to be ignored — they are the primary constraints that determine what backend performance is achievable.

The backend engineering discipline: when optimising a backend system, understand the full call stack from application code to hardware. Profile with realistic workloads. Understand which operations are CPU-bound and which are I/O-bound. The correct optimisation depends on which is the bottleneck.

## C as the Right Tool for Systems Engineering

Torvalds' preference for C in the Linux kernel is not dogma — it is engineering: in C, there are no hidden costs. Every allocation is explicit (`malloc`/`free`). Every function call is a function call, not a virtual dispatch through a vtable. Every copy is explicit. The engineer who reads C code knows what the machine will do.

The backend engineering lesson for higher-level systems: understand the cost model of your language and runtime. Python's GIL, Java's garbage collector, Node.js's event loop, Go's goroutine scheduler — these are not implementation details to be ignored. They determine what performance is achievable and what failure modes to expect.

## Simple Algorithms Beat Complex Architecture

Torvalds is sceptical of architectures that add complexity in anticipation of scale. His engineering preference: choose the simplest algorithm that is correct, and optimise only when the simple algorithm is measurably insufficient. A hash table that is O(1) average is better than a tree that is O(log n) worst-case, if the worst-case never occurs in practice.

The backend engineering discipline: measure before optimising. Profile with realistic workloads. The bottleneck is almost never where you expect it to be.

## Never Break the API Contract

Torvalds' "never break userspace" principle applies directly to backend API design. An API that breaks its callers when it changes is not a stable API — it is a moving target that forces callers to constantly track the API's evolution. The backend engineering standard: once an API is published, its contract is permanent. Add capabilities; do not remove or change existing ones.

The practical implication: design APIs for longevity. The decisions made in an API's first version will constrain every subsequent version. Invest proportionally in getting the first version right.

## Kernel Architecture Lessons for Backend Design

The Linux kernel's architecture provides concrete lessons for backend design: clear layering (no upward dependencies), explicit interfaces between components, and separation of policy from mechanism. The kernel does not dictate how filesystems should work — it provides the VFS layer and lets filesystems implement the interface. The kernel does not dictate how network protocols should be structured — it provides the socket API and lets protocols implement it.

The backend engineering pattern: define the interface that your system's components must satisfy, and implement each component against that interface. The interface is stable; the implementations can be changed.

## Sources
- [Linux Kernel Mailing List — various technical discussions](https://lkml.org/)
- [Linux Kernel Architecture documentation](https://www.kernel.org/doc/html/latest/)
- [Linus Torvalds — talks and interviews on systems design]
- [Git internals documentation — git-scm.com](https://git-scm.com/book/en/v2/Git-Internals-Plumbing-and-Porcelain)
