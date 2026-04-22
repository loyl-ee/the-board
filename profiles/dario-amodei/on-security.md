# Dario Amodei — On Security

## AI Safety as a Security Discipline

Amodei's framework for AI safety is structurally similar to security engineering: identify the threat model, design mitigations into the system, test adversarially, and deploy with staged rollout. Constitutional AI — the methodology he championed — encodes safety constraints into the training process rather than applying them as post-hoc filters. This is analogous to secure-by-design software: building the constraint into the architecture rather than bolting on validation afterward.

The security engineering principle: security properties that are architectural (cannot be violated by any input) are stronger than security properties that are procedural (checked by code that could have bugs or be bypassed).

## Red-Teaming as a Security Engineering Phase

Anthropic's engineering culture treats red-teaming as a mandatory engineering phase before deployment, not an optional QA step. Red teams attempt to elicit harmful outputs, probe for jailbreaks, test edge cases in the safety training, and look for failure modes that the engineering team did not anticipate.

The security engineering discipline: budget explicitly for adversarial testing proportional to the potential impact of failure. The engineering teams most resistant to red-teaming are the ones that most need it.

## Responsible Scaling Policy as a Security Architecture

Anthropic's Responsible Scaling Policy (RSP) is an explicit framework for what capabilities would trigger a deployment pause and what safety mitigations are required before crossing specific capability thresholds. This is security architecture applied to AI development: define in advance what capabilities are dangerous, define the mitigations required to handle those capabilities safely, and commit to not crossing the capability threshold until the mitigations are in place.

The security engineering lesson: define your security requirements before you build the system, not after. What capability threshold would require you to stop and invest in additional safety engineering? Define it now.

## Constitutional AI as Security Policy Encoding

Constitutional AI works by training a model using a set of explicit principles (the "constitution"), then using the model itself to evaluate whether its outputs violate those principles and to generate improved outputs. The security analogy: the constitution is a security policy document, and the self-evaluation step is automated policy enforcement.

For security engineering more broadly: machine-readable security policies that can be automatically evaluated are more reliable than security policies that require manual review of every case. Invest in formalising your security requirements to the point where automated evaluation is possible.

## Privacy as a Security Requirement

Amodei frames privacy not as a compliance checkbox but as a security requirement: user data that is not collected cannot be breached, cannot be subpoenaed, and cannot be used to train systems in ways users did not consent to. The security architecture implication: data minimisation is a security control.

The engineering standard: before collecting any user data, define the specific security controls required to protect it and the specific user benefit that justifies the collection. Data that fails this analysis should not be collected.

## Sources
- [Anthropic's Responsible Scaling Policy](https://www.anthropic.com/index/anthropics-responsible-scaling-policy)
- [Constitutional AI: Harmlessness from AI Feedback — Anthropic, 2022](https://arxiv.org/abs/2212.08073)
- ["Machines of Loving Grace" — Dario Amodei, 2024](https://darioamodei.com/machines-of-loving-grace)
- [Anthropic Model Card — claude.ai](https://www.anthropic.com/claude)
