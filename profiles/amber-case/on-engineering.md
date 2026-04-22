# Amber Case — On Engineering

## Calm Tech Engineering: Minimum Viable Interruption

Case's engineering standard for any system that communicates with users is "minimum viable interruption" — the smallest possible intrusion into the user's attention that is sufficient to convey necessary information. This is an engineering constraint, not a design preference. It means that before implementing any notification, alert, or background process, the engineering team must answer: what is the minimum signal that accomplishes this purpose?

The engineering discipline: enumerate every state the system can be in that might warrant communicating to the user. For each state, define the least intrusive communication mechanism that serves the user's actual need. Implement the communication mechanism, not the loudest version of it.

## Progressive Interruption as an Engineering Pattern

Case has developed an explicit framework of interruption levels — from zero (no user notification, system handles autonomously) to full alert (demands immediate user attention, blocks other tasks). Good engineering implements the lowest level that serves the functional requirement.

The engineering hierarchy: ambient display → status bar indicator → gentle badge → push notification → modal alert → blocking modal. Each level has a higher attention cost. The engineering decision is: given what the user needs to know, which is the minimum viable level? Systems that default to push notifications when a status bar update would suffice are engineering failures.

## Data Minimisation as an Engineering Principle

Case's calm technology framework applies directly to data: collect only what is necessary for the feature, store it only as long as necessary, and make it explicitly visible to the user what is being collected. This is not just a privacy policy position — it is an engineering architecture choice.

Data minimisation has engineering benefits beyond ethics: less data to store means simpler schemas, fewer privacy risks, smaller backup sizes, and lower compliance overhead. The engineering discipline: before adding any data collection, define the specific feature it enables and confirm there is no way to provide that feature with less data.

## Accessibility as Engineering Baseline

Case has worked extensively on designing for neurodivergent users — particularly people with ADHD and attention difficulties. Her engineering standard: a system that works for the most cognitively constrained user works better for everyone. Features that reduce cognitive load, minimise mode-switching, and avoid surprise state changes are accessibility features and quality improvements simultaneously.

The engineering checklist she has developed for cognitive accessibility: Does the system always tell the user what it is doing? Are there unnecessary distractions in the interface? Can the user control the pace of information? Are transitions predictable? These are not optional accessibility concerns — they are quality engineering requirements.

## Background Processes and Battery Engineering

Case's calm technology principles apply directly to background engineering: an app that does unnecessary background processing, maintains unnecessary network connections, or wakes the device unnecessarily is not just bad for battery life — it is a violation of the user's trust that the app is behaving as it should when they cannot see it.

The engineering standard: every background process should have a documented purpose, a defined trigger, and a defined termination condition. Background processes that run indefinitely without user-visible benefit are engineering debt.

## Sources
- *Calm Technology: Principles and Patterns for Non-Intrusive Design* — Amber Case, 2015 (O'Reilly)
- [calmtech.com — principles and pattern library](https://calmtech.com/)
- [Amber Case — caseorganic.com](https://caseorganic.com/)
- [The Calm Technology Institute](https://calmtech.com/)
