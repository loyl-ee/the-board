# Amber Case — On Product

## The Eight Principles of Calm Technology

Case's primary product framework is the eight principles of calm technology, developed from Weiser and Brown's original research and codified in her 2015 O'Reilly book. These are not aesthetic preferences but structural requirements for products that respect user attention.

**Principle I: Technology should require the smallest possible amount of attention.**
The product's ambient state — doing its work in the background — should generate no cognitive demand. Only transitions, completions, errors, or genuine urgencies should surface to consciousness. Designing for the default state of calm is the first product requirement.

**Principle II: Technology should inform and create calm.**
"A person's primary task should not be computing, but being human." The product exists to support the user's life, not to become the center of it. Every feature should be evaluated against the question: does this help the user accomplish their actual goal, or does it add computing overhead?

**Principle III: Technology should make use of the periphery.**
Information should live at the edge of awareness by default, moving to the center only when action is required. Ambient displays — status lights, subtle audio tones, haptic feedback — are peripheral communication channels that do not interrupt. Good product design identifies which information belongs at the periphery and keeps it there.

**Principle IV: Technology should amplify the best of technology and the best of humanity.**
Machines should do machine things (consistent processing, reliable memory, pattern detection at scale) so humans can do human things (judgment, creativity, relationship). Product design fails when it forces humans to act like machines (following rigid scripts, monitoring dashboards) or when machines pretend to act like humans (simulated emotion, anthropomorphized decision-making). "Machines shouldn't act like humans and humans shouldn't act like machines."

**Principle V: Technology can communicate, but doesn't need to speak.**
Voice and text alerts are the most cognitively expensive communication channels because they require language processing. Products should explore the full space of communication: light (traffic lights, status indicators), sound (tones, chimes), touch (haptics), and visual patterns (trend graphs, status colors). The Roomba's use of tones is her often-cited example — a tone that communicates "I'm stuck" across any language, without demanding that the user read or listen to an explanation.

**Principle VI: Technology should work even when it fails.**
Graceful degradation is a product requirement, not an edge case. When a smart system fails, it should default to its simplest usable state rather than becoming non-functional. The escalator that becomes usable stairs is the canonical example. Products that require perfect connectivity or perfect state to function have failed this principle.

**Principle VII: The right amount of technology is the minimum needed to solve the problem.**
Feature minimalism is not a stylistic preference — it is a product discipline. Every additional feature adds cognitive overhead for the user, maintenance burden for the team, and potential failure points in the system. "The right amount of technology is the minimum needed to solve the problem." Product decisions should be evaluated against this question: is this feature necessary, or does it add complexity without proportionate value?

**Principle VIII: Technology should respect social norms.**
New technology should be introduced gradually, leveraging existing familiar behaviors rather than demanding users adopt entirely new mental models. Products that create social friction — by making private things public, by demanding attention in inappropriate contexts, by behaving unpredictably — erode trust even if they function correctly.

## Notification Design as a Core Product Discipline

Case treats notification design as one of the most consequential product decisions a team makes. The key framework: use the lowest-interruption channel sufficient to communicate the necessary information. In ascending order of interruption cost:

- Ambient status (no notification; the product state is visible if looked for)
- Haptic (private, non-visual, low cognitive cost)
- Status light (visible, requires no decoding, non-disruptive)
- Status tone (brief audio signal)
- Badge or counter (visible when user looks at device)
- Banner notification (appears, then disappears)
- Alert/popup (demands response before proceeding)

The default should be the most peripheral option that reliably communicates the information. Alerts and popups should be reserved for deletions, emergencies, or explicitly opted-in streams. "Alerts and notifications are overwhelming us. Calm tech is about giving us back our attention."

## Ambient Displays as Product Paradigm

Case draws heavily on ambient display examples — devices or interfaces that communicate ongoing status without demanding active attention. The tea kettle, the office window as a light source that varies with weather, the Sleep Cycle app's data visualization, the airplane lavatory occupied/vacant indicator. These are products that have solved the problem of information delivery without interruption.

For software products, ambient display thinking translates into: what information does the user need to be aware of, and how can it be present without being intrusive? Dashboard widgets, status bars, color-coded indicators, and subtle progress indicators all operate in this register.

## The Product Audit Framework

Case's workshops introduce a practical audit process: identify every notification and alert a product generates, classify each by interruption level, and ask whether the interruption level matches the actual urgency of the information. In practice, most products fail this audit — they use high-interruption channels (alerts, badges, banners) for low-urgency information because those channels were easy to implement or because engagement metrics rewarded attention capture. The audit makes the mismatch visible.
