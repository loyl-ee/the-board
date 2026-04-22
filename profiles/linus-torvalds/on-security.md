# Linus Torvalds — On Security

## Security Through Code Review

Torvalds' primary security mechanism for the Linux kernel is code review. Every patch submitted to the kernel goes through review by maintainers before merging. The review is technical — does the code do what it claims to do, does it introduce memory safety issues, does it change behaviour in ways that could be exploited — and it is unsparing. Patches that contain security-relevant issues are rejected with an explanation.

The security engineering principle: code review is a security control. Not a complete one — review misses bugs — but a significant one that catches a substantial fraction of security issues before they reach users. Teams that skip review for velocity reasons accept a higher rate of security vulnerabilities as a consequence.

## Responsible Disclosure and the CVE Process

Torvalds operates within the kernel's established vulnerability disclosure process: security issues are reported privately to the kernel security team, a patch is developed privately, and disclosure is coordinated with distributions so they can ship the patch simultaneously with public disclosure. This gives users a path to the fix at the moment the vulnerability is known.

The security engineering standard: every project should have a documented process for receiving private security reports and coordinating disclosure. The absence of such a process means vulnerabilities are either disclosed publicly without a fix (maximising user exposure) or suppressed indefinitely (leaving users vulnerable while attackers may already know).

## Never Breaking Userspace as a Security Property

Torvalds' commitment to never breaking userspace is itself a security property. Applications that break on kernel update are not updated — which means they run on older, less secure kernels. By ensuring that every kernel update is backward-compatible with existing userspace applications, Torvalds maximises the fraction of users running the most secure available kernel.

The security engineering lesson: backward compatibility and security are not in tension. Breaking changes that force users to delay updates reduce the fraction of users on patched systems.

## Memory Safety as the Dominant Security Concern

The majority of kernel security vulnerabilities are memory safety issues: buffer overflows, use-after-free bugs, null pointer dereferences. Torvalds' engineering response has been cultural (rigorous review of memory-sensitive code) and increasingly architectural (exploring Rust as a memory-safe language for new kernel components).

The security engineering discipline: identify the dominant vulnerability class in your system and invest disproportionately in preventing it. For systems code, this is memory safety. For web applications, this is injection (SQL, XSS, CSRF). For AI systems, this is prompt injection.

## Open Source as a Security Model

Torvalds is a consistent proponent of open source security: public code is reviewed by a larger population of reviewers, including security researchers who are specifically looking for vulnerabilities. The alternative — security through obscurity — fails when the obscured system is eventually reversed or when source code is leaked.

The security engineering position: for security-sensitive code, more reviewers is better. Open source your security-critical components if the threat model allows.

## Sources
- [Linux Kernel Security — kernel.org](https://www.kernel.org/doc/html/latest/process/security-bugs.html)
- [Linux CVE database — cve.org](https://www.cve.org/)
- [Linus on Rust in the kernel — LWN.net, various](https://lwn.net/Articles/834021/)
- [Linux Kernel Mailing List — security-related discussions](https://lkml.org/)
