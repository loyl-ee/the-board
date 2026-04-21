# Brent Simmons — On Safety

## Privacy as a Default, Not a Feature

Simmons treats privacy as infrastructure rather than a selling point. NetNewsWire's privacy policy opens with a declaration that is unusual for any software: "We don't want any private information. We really, really don't." The reasoning is not only ethical — it is practical. Private user data offers no value to a project whose only goal is to make a great RSS reader, and storing it securely would be a burden with no corresponding benefit.

This is a design principle, not a legal compliance posture. The absence of user data collection is not an accident of limited resources; it is the result of a deliberate choice to build software that does not need that data to function.

## What NetNewsWire Does Not Collect

NetNewsWire collects no behavioral data, runs no analytics, shows no advertising, and tracks no individual users. The netnewswire.com and inessential.com websites use "no cookies, JavaScript, or trackers" and display no advertisements. Crash logs are collected only from users who explicitly opt in, stored privately, and shared publicly only if they contain no personal identification. Website traffic logs are analyzed in aggregate only — download counts, popular pages — and logs are stored privately.

The only third-party services involved are opt-in: GitHub for the repository, Discourse for the community forum. Both use their own privacy systems, and both require explicit user action to join.

## RSS as a Privacy Architecture

There is a structural privacy advantage to the RSS model that Simmons has noted: because NetNewsWire fetches feeds directly from publishers' servers, there is no central server that knows what you are reading. Unlike a social media platform that tracks every article interaction, or a centralized RSS sync service that maintains a complete reading history, a locally-stored feed reader leaves no data trail on anyone's server.

This is not a coincidence of implementation. It is what a well-designed RSS reader looks like from a privacy standpoint: the user's reading behavior is their own.

## Crash Reporting and Responsible Disclosure

Even where data collection is necessary — crash logs — Simmons has been careful. The opt-in model for crash reporting, the commitment to storing logs privately, and the standard of sharing only de-identified reports all reflect a responsible approach to the minimum necessary data collection. He wants to fix bugs. He does not want to maintain a database of user activity to do it.

## Responsibility for Behavior

Simmons has written about responsible development in the context of transparency — software that does not behave mysteriously, that explains its own decisions to users, and that can be trusted to do what it says it does. This is safety in a broader sense: safety from unpredictable software behavior, safety from being surveilled by your own tools, safety from the guilt-generating accumulation of unread content that he explicitly designed against.

The absence of dark patterns in NetNewsWire — no forced sign-in, no data-harvesting account creation, no nagging for reviews, no "engagement" features designed to maximize time in app — is itself a form of user protection.

## Gap Note

Simmons has not written extensively about security topics in the technical sense — encryption, authentication, secure coding practices, or threat modeling. His privacy writing is primarily about data minimization and the ethics of not collecting what you do not need. For deep technical security questions, his perspective is most useful as a philosophy of restraint rather than as an implementation guide.
