# David Smith — On UX

## Simplicity as the Primary Constraint

Smith's UX philosophy centers on a single imperative: do not make users think. This principle from Steve Krug's writing is Smith's operational north star. He has applied it repeatedly in his health tracking apps, where the mental model must be simple enough to be understood at 7am before coffee: a single number, a color, a goal indicator.

For Pedometer++, this means a step count against a daily goal, rendered as a progress arc. When the goal is met, the screen "explodes in confetti" — a moment of celebration that is disproportionate in the best way, designed to make the user feel something rather than simply note a number. For Sleep++, the same constraint applies in a quieter register: a sleep duration, a quality score, a binary sense of whether the night was restorative.

## Automatic Over Manual

Where a health tracking behavior can be automated, Smith automates it. Sleep++ 3.0 (2018) removed the requirement to manually start and stop sleep tracking sessions. The app simply reads motion, heart rate, and activity data from an Apple Watch worn overnight and computes sleep duration and quality retrospectively. This change was explicitly motivated by the failure mode of manual tracking: users who most need sleep data are the users who are too tired to remember to start the app before bed.

The willingness to sacrifice precision for reliability is a consistent UX value. Sleep++'s automatic tracking is less precise than a manual session, but it generates data every night rather than sporadically. The readiness score compounds this data over 30 days of rolling history, making the long-term pattern more visible even when any individual night's measurement is approximate.

## Progressive Disclosure

Smith's apps surface their most important information immediately and reveal detail on demand. This pattern — primary summary, secondary decomposition — appears across his health apps:

- **Pedometer++**: Step count at a glance, then charts of daily and weekly activity for users who want trend analysis
- **Sleep++**: Duration and quality score on the main screen, then component values (HRV, resting heart rate comparison to 30-day baseline) accessible via a single tap
- **Widgetsmith**: Theme gallery as the primary entry point, then granular color, font, and border controls for users who want full customization

This architecture serves both the casual user who wants a single number and the engaged user who wants to understand the underlying data. It avoids the common failure mode of overwhelming new users with configuration options they don't yet have context to use.

## Onboarding Complexity in Widgetsmith

Widgetsmith is a UX exception in Smith's portfolio — and he knows it. The app requires users to understand a multi-step process: create a widget in the app, add a widget placeholder on the home screen via long-press, select the placeholder's type, then select the specific widget created in the app. This is iOS's widget architecture, not a choice by Smith, but it creates onboarding friction that most apps don't face.

His response was infrastructure: FAQ pages, embedded video tutorials (which proved roughly 20x more effective than text in explaining the widget setup process), and design of the in-app experience to guide users as clearly as possible toward the correct sequence. The video-first support strategy emerged directly from observing that 80,000 users watched setup videos compared to 4,000 who read text instructions for the same task.

## Contextual Notifications

Smith designs notifications as moments of service rather than interruption. Sleep++ delivers its morning summary "within a few minutes of first unlocking your iPhone" — respecting the natural behavior of checking a device after waking, rather than pushing a notification that might interrupt sleep or arrive hours after the fact. Pedometer++'s bedtime reminder emphasizes conscious choice: it helps users "make a conscious choice in those situations" about whether to try to hit their step goal, rather than delivering a guilt-inducing notification.

## Accessibility as a UX Requirement

Smith treats accessibility as a UX requirement rather than a compliance checkbox. Dynamic Type scaling is tested across all text sizes. VoiceOver compatibility is built in, not added as an afterthought. His Design Diary documents specific decisions about how elements scale with Dynamic Type, including custom solutions for elements that do not automatically scale correctly. His analytics show that a meaningful proportion of his users — 18% in Widgetsmith's case — have non-default text size settings, making this a practical UX concern, not just a theoretical one.
