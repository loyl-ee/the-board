# Amber Case — On Security

## Security UX: Don't Make Security Decisions Incomprehensible

Case's calm technology principles apply directly to security UX: security decisions presented to users in incomprehensible terms are security decisions made without user consent. A permission dialog that says "This app would like to access your location" when the feature that requires location could have been designed without it is not a security control — it is a consent theatre.

The security engineering standard: every permission request must be preceded by a clear explanation of what feature requires it and why the alternative (not granting the permission) is not viable. Users who do not understand why a permission is needed will either deny all permissions (breaking the app) or grant all permissions (abandoning security).

## Minimal Data as a Calm Technology Security Principle

Case's data minimisation principle is a security principle: the data you do not collect cannot be breached, subpoenaed, or misused. The calm technology standard for data collection is that any data collection that does not directly benefit the user's primary use case is noise — and noise in a calm system is eliminated.

The engineering security checklist: for each piece of data your system collects, identify the specific user-facing feature it enables. If no feature can be identified, do not collect the data. If a feature can be identified, collect only that data and nothing adjacent.

## Notification Honesty as a Security Property

Case has argued that notifications sent without genuine user relevance are a security and trust vulnerability: users who are overwhelmed by irrelevant notifications stop reading them, meaning that genuinely important security notifications (a suspicious login, a payment failure) are lost in the noise.

The security engineering standard: reserve notifications for events that require user action or awareness. Security-relevant notifications (login from new device, unusual account activity) must be distinguishable from marketing and engagement notifications. If they are not distinguishable, security notifications will be ignored.

## Designing Security for Neurodivergent Users

Case's work on ADHD and attention emphasises that security systems that require continuous vigilance fail for neurodivergent users. Multi-factor authentication flows that require switching between apps, security alerts that appear at unpredictable times, and session timeouts that discard unsaved work all disproportionately burden users with attention difficulties.

The security engineering discipline: design security flows for the user with the most difficulty completing them. A security flow that works for a user with severe ADHD works for everyone. A security flow designed for a neurotypical user with full attention fails a large portion of the actual user population.

## Background Process Transparency as a Security Interface

Case's calm technology principles require that background processes be transparent to users. The security implication: an app that runs background processes without user knowledge cannot be trusted by users with the permissions those processes require. Transparency about what runs when is a prerequisite for informed security decisions.

The security engineering standard: document every background process in your app in the privacy policy and in the app's settings. Users who understand what an app does when they are not looking at it can make better security decisions about what permissions to grant.

## Sources
- *Calm Technology: Principles and Patterns for Non-Intrusive Design* — Amber Case, 2015 (O'Reilly)
- [calmtech.com — principles and patterns](https://calmtech.com/)
- [Amber Case — caseorganic.com](https://caseorganic.com/)
- [ADHD design considerations — various conference talks]
