# Linus Torvalds — On Design

## Design as Architecture, Not Aesthetics

When Torvalds talks about design, he means systems design — the structure of interfaces, the shape of data, the decisions that determine what a system can and cannot express. Visual design and human-computer interaction are largely outside his scope of interest. What he cares about is whether the underlying architecture of a system creates clarity or obscures it.

His 1995 Linux kernel coding style documentation, still in use today, opens with a statement that captures his entire design sensibility: "If you need more than 3 levels of indentation, you're screwed anyway, and should fix your program." Indentation depth is a proxy for complexity; complexity is a proxy for misaligned abstraction. A function that requires deep nesting has probably failed to decompose the problem correctly.

## The Aesthetics of Elimination

In his 2016 TED talk, Torvalds used a linked list traversal example to explain what good design looks like to him. The first implementation handles removal of the first element as a special case; the second uses an indirect pointer (a pointer to a pointer) to eliminate the special case entirely. He told the audience: "I want you to understand that sometimes you can see a problem in a different way and rewrite it so that a special case goes away and becomes the normal case, and that's good code."

The elegance he is pointing at is not aesthetic in the decorative sense. It is the recognition that when a design requires a special case, it often means the abstraction is wrong — that the problem has been framed in a way that creates artificial irregularity. The better design reframes the problem so that the irregular case and the regular case are the same case. This reduces code paths, reduces bugs, and reduces cognitive load simultaneously.

## Clean Interfaces and Their Cost

Torvalds has a deep appreciation for Unix's design philosophy — the idea of composable tools with clean interfaces. In *Just for Fun* (2001), he described it: "Unix is the opposite [of monolithic applications]. It gives you the building blocks that are sufficient for doing everything. That's what having a clean design is all about." An interface is clean when it does not expose implementation details that callers should not have to know about, when it is consistent, and when it degrades gracefully.

He applies this standard rigidly to the Linux kernel's interface with userspace — the system call interface. This interface must be backwards compatible forever (see *on-product.md*) precisely because it is the boundary between the kernel's internals and the world. Changes that seem locally sensible but break this boundary are not acceptable regardless of how elegant they are internally.

## Complexity as Offense

Torvalds is almost physically offended by gratuitous complexity. His assessment of Mach (the microkernel that powers macOS at a low level): "Frankly, I think it's a piece of crap. It contains all the design mistakes you can make" (*Just for Fun*, 2001). His view of XML: "XML is crap. Really. There are no excuses" (Google+, March 2014). His view of ACPI (Advanced Configuration and Power Interface, the standard for hardware power management): "ACPI is a complete design disaster in every way" (*Linux Journal*, November 2003).

These are not aesthetic opinions. They are claims that the complexity in these systems is not load-bearing — that the systems achieve their goals less well because of their complexity, not despite it. The charge against Mach is that it adds inter-process communication overhead to achieve theoretical separation that does not pay off in practice. The charge against XML is that it is verbose, hard to parse, and creates more problems than it solves relative to simpler formats.

## The Data Structure as the Design

The most direct statement of Torvalds' design philosophy: "Bad programmers worry about the code. Good programmers worry about data structures and their relationships." This is a claim about where design actually lives. The shape of the data — what it contains, how pieces relate to each other, what operations must be efficient — determines the shape of every algorithm that operates on it. Programs written around well-designed data structures tend to be short and obvious. Programs written without thinking about data structures are complex and brittle regardless of how clever the code is.

Git's design illustrates this. Its core is a content-addressable object store: blobs, trees, commits, and tags, each identified by a SHA-1 hash of its content. That data model — four simple object types in a Merkle tree — is what makes everything else in Git work. The distribution model falls out of it. The integrity guarantees fall out of it. The branching model falls out of it. Torvalds designed the data structure first, and the rest followed.
