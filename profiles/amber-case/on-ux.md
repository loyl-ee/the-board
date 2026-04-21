# Amber Case — On UX

## Minimum Viable Attention as the UX Standard

Case proposes a reorientation of the fundamental UX design goal. Standard UX asks: how do we help users accomplish their goals with the fewest steps? Calm UX asks a different question: how do we help users accomplish their goals with the lowest *mental cost*? These are not the same. A product can reduce steps while increasing cognitive load (through confusing interfaces, unexpected state changes, or attention-demanding notifications). A calm UX minimizes the total cognitive expenditure required to accomplish the task — including the background overhead of monitoring the product while doing other things.

"If good design allows someone to get to their goal with the fewest steps, calm technology allows them to get there with the lowest mental cost." This reframes the UX optimization target from efficiency (time and steps) to attention economics (cognitive expenditure).

## The Notification Audit

One of Case's most practical UX contributions is the notification audit framework, which she uses in workshops and consulting engagements. The process:

1. Inventory every notification, alert, badge, and communication the product generates
2. Classify each by channel (haptic, visual, audio, text) and by interruption level (peripheral, ambient, foreground, modal)
3. Assess the actual urgency of each notification — does the urgency level justify the interruption level?
4. Redesign notifications that use a higher-interruption channel than their content warrants

In practice, most products fail this audit substantially. Notifications are typically implemented at whatever level was easiest to build, or at whatever level maximized a short-term engagement metric (open rates, clicks), rather than at the level appropriate to the actual urgency of the information. The audit makes the mismatch legible.

The remediation is systematic: move low-urgency notifications down the interruption hierarchy. Turn alerts into badges. Turn badges into ambient status indicators. Turn status indicators into information that is available on demand rather than pushed. Notifications that survive the audit at their original interruption level are genuinely urgent; everything else has been reclassified to a less disruptive channel.

## Progressive Levels of Interruption

Case articulates a clear model of progressive interruption — the idea that any given piece of information has an appropriate channel, and that using a more disruptive channel than necessary is a UX failure with a measurable cost. The progression she describes, from lowest to highest interruption:

- **No notification** — the product is working; nothing to report
- **Ambient state change** — a subtle visual or environmental signal available if the user looks
- **Haptic** — physical, private, requires no visual attention
- **Status light or icon** — visible on glance, requires no decoding
- **Badge/counter** — quantified, visible when device is checked
- **Banner** — transient, appears and disappears, can be ignored
- **Sound/tone** — requires audio channel, moves through space
- **Full alert/popup** — demands explicit acknowledgment before proceeding

Each level up this stack represents a higher tax on user attention. The UX discipline is to use the lowest effective level — and "effective" means the information reliably reaches the user at the right time, not that the designer can prove the notification was seen.

## Designing for Users with Attention Constraints

Case's framework is particularly relevant for users with ADHD or other attention-affecting conditions. While she does not specifically address ADHD in most of her public writing (this is worth noting as a gap), her principles map directly onto what attention-constrained users need:

- Fewer, more meaningful interruptions (rather than constant background noise)
- Clear hierarchy of urgency (so users can calibrate their response threshold)
- Peripheral rather than central communication for ongoing state (reducing the burden of monitoring)
- Graceful failure modes that do not create anxiety or confusion
- Minimum necessary feature sets that reduce the cognitive overhead of managing the product itself

The principle that "although the number of alerts vying for our attention has increased, the amount of attention we have remains the same" is structurally identical to the experience of ADHD — a fixed attentional budget under constant competitive pressure. Calm technology design is, in effect, attention-accessible design.

## The Cost of Interruption

Case draws attention to the well-documented cognitive science finding that interruptions are disproportionately costly relative to their duration. An alert that takes three seconds to read may cost several minutes of productive focus — the time required to re-enter a flow state after being pulled out of it. "Notification fatigue" is the systemic result of products that individually impose small interruption costs but collectively exhaust the user's willpower and focus across the day.

This has a direct UX implication: the decision to send a notification is never a small decision. It carries an asymmetric cost — low for the sender, potentially high for the recipient. UX designers who treat notifications as free or low-cost signals are failing to account for this asymmetry.

## Unambiguous Input Design

Case advocates for "unambiguous input" as a UX principle — interfaces where the user's action produces a clear, predictable, single outcome. She uses buttons on a game controller or remote control as examples: physical buttons, one press equals one action, no ambiguity about state. This contrasts with gesture-based interfaces, AI-mediated inputs, or context-dependent controls where the same action produces different results in different states.

Unambiguous input reduces cognitive load because the user does not need to verify the outcome of their action — they know what will happen before they act. This is a distinct contribution to UX thinking that complements her notification work: calm UX is not just about what the product communicates to the user, but about how clearly the product interprets the user's communications back to it.

## The Trust Standard

Case ultimately frames UX success in terms of trust rather than delight or engagement. A product that users trust is one whose behavior is predictable, whose notifications are meaningful, and whose defaults respect their attention. Trust is earned through restraint: every unnecessary interruption is a small withdrawal from the trust account. Products that maximize engagement through attention capture may see strong short-term metrics while eroding the long-term trust that sustains use.
