# Steve Troughton-Smith — On Safety

## A History of Responsible-Adjacent Disclosure

Troughton-Smith occupies an interesting position in the landscape of Apple platform security research. He is not a security researcher in the traditional sense — his work is not about finding exploits or bypassing protections for the purpose of demonstrating vulnerabilities. It is about understanding what Apple's platforms are doing internally, which occasionally means stumbling into information Apple had not intended to make public.

His most prominent example is the HomePod firmware incident in July 2017. Apple accidentally pushed a firmware bundle that contained references to the then-unannounced iPhone X, including its bezel-free design, the "Pearl ID" infrared facial recognition system, and internal codenames. Troughton-Smith analyzed the bundle — which Apple had made publicly available, however briefly — and published his findings immediately. He did not contact Apple privately first; the information was already public, even if inadvertently. His own public acknowledgment of the situation was characteristically direct: telling Wired, "This is a rough situation for Apple."

## The Ethics of His Methodology

His reverse engineering work involves three types of artifacts, each with different ethical standing:

1. **Publicly released firmware and code drops**: Apple ships these to the public. Analyzing them, even when Apple would prefer developers didn't look too closely, involves no breach of any agreement.

2. **Open-source Apple code**: Analyzing this is legally and ethically straightforward; it's released under open-source licenses by design.

3. **Developer toolchain artifacts**: His xrOS discovery came from submitting a crafted binary to App Store Connect — a tool available to any registered developer — which triggered an error message exposing the internal OS name. This is creative but legitimate use of a public developer service.

He does not, to public knowledge, jailbreak devices or bypass Apple's security protections to extract private data. His boundary appears to be: if Apple shipped it or made it accessible through legitimate developer channels, it is fair game for analysis.

## Relationship with Apple's Security Team

No public evidence of formal coordination between Troughton-Smith and Apple's security team exists. His discoveries are typically announced publicly rather than privately first, which is consistent with the view that his work involves no actual vulnerabilities — only embarrassing product disclosures. Apple has not, to public knowledge, taken any legal action against his analysis work, likely because he has not violated the Computer Fraud and Abuse Act or equivalent Irish law.

## On Platform Restrictions as Safety Theater

A distinct thread in his safety-related commentary concerns Apple's stated security rationale for platform restrictions. He is skeptical of arguments that JIT compilation restrictions, browser engine requirements, or limitations on background processes are primarily safety measures rather than competitive ones. When restrictions that Apple justified on security grounds were lifted in the EU under DMA pressure, he noted this as evidence that the restrictions were not purely technical necessities.

He is measured here — he does not claim Apple's security model is entirely pretextual — but he pushes back consistently on the conflation of security and control, arguing that transparent, auditable restrictions would be more credible than blanket prohibitions on developer capabilities.
