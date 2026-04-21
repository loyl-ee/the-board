# Amelia Wattenberger — On Safety

## Her Frame: Interface Design as Responsibility

Wattenberger does not use the vocabulary of AI safety research (alignment, robustness, corrigibility). Her concern is closer to product ethics: the interface design choices that shape whether users understand what the AI is doing, whether they maintain genuine agency, and whether the system creates appropriate rather than false trust. These are practical safety concerns — the kind that cause harm at scale before anyone calls it a safety problem.

## The Confidence Problem

Her most pointed safety-adjacent observation is about chatbot overconfidence. In "Why Chatbots Are Not the Future" (wattenberger.com, 2023), she notes that AI chatbots present themselves as "endlessly confident" — prose that sounds authoritative regardless of accuracy. Users cannot tell whether the AI understood the question or where the information came from. The fluent, well-formatted response is indistinguishable from a correct one.

This is a design failure with safety consequences. When interfaces do not signal AI uncertainty, users cannot calibrate their trust appropriately. They either over-rely (accepting wrong outputs as correct) or blanket-distrust (rejecting useful outputs as unreliable). Neither is safe. The responsible design choice is to make uncertainty visible — to show where the AI is confident and where it is guessing — rather than letting confident prose style substitute for epistemic honesty.

## No Man's Land as a Safety Concern

Her "No Man's Land" concept — the dangerous middle zone where the AI does the work but the human is nominally responsible for the outcome — is implicitly a safety argument. When users are "just pressing buttons and the machine is doing the work," they lose the understanding and engagement necessary to catch errors. This is the failure mode behind automation accidents in aviation, medical devices, and financial systems: the human is in the loop but not genuinely attending.

Her prescription — either fully automate or genuinely augment, but avoid the middle — is a safer design pattern. A fully automated system can be evaluated on its outcomes. A genuinely augmenting system keeps the human informed and engaged. The middle zone produces humans who are responsible without being capable of exercising that responsibility.

## Context as a Safety Feature

Her advocacy for embedding context into interfaces — rather than requiring users to type it — has a safety dimension. An interface that requires users to specify the AI's limitations via prompt places the burden of safe use on the user. An interface that makes limitations visible by design protects even users who do not know what to ask or warn against.

Her call for "couching AI-generated responses in larger frameworks and related context" (from "Putting Knowledge in Its Place") is also a safety argument: an AI answer shown in context, with related information and data visualizations, is easier to evaluate for correctness than a standalone assertion.

## Gap Note

Wattenberger does not write about AI safety in the technical sense — she is not focused on model alignment, adversarial robustness, or systemic risks from AI development. Her safety concerns are UI-layer concerns: false confidence, loss of agency, opaque outputs, inappropriate trust. These are real and consequential harms, but they are distinct from the deeper safety questions that researchers like Geoffrey Hinton or Stuart Russell address. She should be invoked for interface-level safety design, not for policy or technical safety questions.
