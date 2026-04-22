# Linus Torvalds — On Testing

## The Kernel's Testing Philosophy: Users as the Test Suite

Torvalds' testing philosophy for the Linux kernel is empirical: millions of users running the kernel on diverse hardware configurations produce more test coverage than any test suite could. A bug that affects real hardware under real workloads will be found and reported. A test suite that runs on specific hardware in controlled conditions will not find hardware-specific race conditions.

The testing principle: for systems software that runs on diverse hardware under unpredictable workloads, real-world usage is the most comprehensive test. Automated tests catch regressions in known scenarios; real users find scenarios you did not know to test.

## Bisect as the Primary Testing Tool

Torvalds built `git bisect` specifically to make regression testing efficient. The workflow: when a bug is reported, bisect the commit history to find the exact commit that introduced it. This requires that the test for the bug (a reproducer) be binary: pass or fail. Any regression that can be expressed as a binary test can be bisected to its source.

The testing discipline: every bug fix should be accompanied by a reproducer that fails before the fix and passes after. That reproducer becomes the regression test. Without it, the bug can be reintroduced by a future change without immediate detection.

## Code Review as the Primary Quality Gate

Torvalds has been explicit: the Linux kernel's quality assurance is primarily code review, not automated testing. A patch submitted to the kernel goes through multiple rounds of review by subsystem maintainers before it reaches Torvalds. Each maintainer is responsible for the technical quality of patches in their subsystem.

The testing principle: for code where correctness is paramount and test coverage is inherently incomplete (concurrency, hardware interaction, undefined behavior), code review by domain experts is a stronger quality gate than automated tests. Tests verify behavior; reviewers verify reasoning.

## Performance Testing: Measure, Don't Assume

Torvalds has written about performance optimisation with the discipline of measurement first. Before optimising, prove with a profiler that the code you intend to optimise is the bottleneck. After optimising, prove with a benchmark that the optimisation improved performance. The claim "this is faster" without measurement is not an engineering claim.

The testing discipline: performance tests are tests. A benchmark that establishes a performance baseline and fails when performance regresses is as important as a correctness test in a performance-critical codebase.

## Never Merge Untested Code

Torvalds' merge policy for the kernel: subsystem maintainers are responsible for testing changes in their subsystem before sending a pull request. He has publicly declined pull requests from maintainers who had not tested changes on real hardware. The engineering accountability is with the code's author and the subsystem maintainer, not with Torvalds as the final integrator.

The testing discipline: the person who writes the code is responsible for testing it. Delegating testing to a CI system or a QA team does not discharge that responsibility. The engineer who writes the change understands its implications and is best positioned to design the test that catches its failure modes.

## Sources
- [Linux Kernel Mailing List — testing and review discussions](https://lkml.org/)
- [Git documentation — git bisect](https://git-scm.com/docs/git-bisect)
- [Linux kernel development process documentation](https://www.kernel.org/doc/html/latest/process/)
- [Linus Torvalds — technical interviews and LKML posts on code quality]
