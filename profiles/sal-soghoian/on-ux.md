# Sal Soghoian — On UX

## The User as the Most Important Programmer

Soghoian's UX philosophy begins with an inversion of the conventional software hierarchy. In most product thinking, the user is the person the developer is designing for — the recipient of design decisions made elsewhere. In Soghoian's view, the power user is a programmer in their own right: they are designing their own workflow, their own automation, their own augmentation of the tools a developer has provided. The developer's job is to give that user programmer the APIs, the hooks, the scripting access, and the documentation they need to do their job.

This framing has direct UX consequences. A scriptable application needs a UX designed for two audiences simultaneously: the end user who never touches a script, and the power user who orchestrates the application from the outside. Both audiences need to be first-class citizens. An application that serves the first audience beautifully but ignores the second has failed at Soghoian's standard.

## Progressive Disclosure of Automation Complexity

One of the most useful frameworks that emerges from Soghoian's work — though he has not always labeled it as such — is the progressive disclosure of automation complexity. The Mac automation stack presents users with a spectrum of capability and complexity:

**Shortcuts** sits at the accessible end: visual blocks, no syntax, runs on iPhone and Mac, designed for general audiences. Users can build useful automations with no prior knowledge. The ceiling is real but the floor is almost nonexistent.

**Automator** sits in the middle: visual workflows, but more powerful action types, tighter integration with the file system and application data, and the ability to embed shell scripts and AppleScript for when visual building is insufficient. It asks more of the user but returns more power.

**AppleScript and JavaScript for Automation (JXA)** sit at the expert end: text-based scripting languages that directly address application internals via Apple Events, with full access to application data models. The syntax overhead is real; so is the power.

**Shell scripts and UNIX tools** complete the spectrum, giving technical users access to the entire POSIX environment.

Soghoian's UX insight is that these are not competing options — they are a ladder. A user can enter at any rung and climb as their needs grow. The failure mode is treating any of these rungs as the only legitimate one: building only for Shortcuts users abandons the experts; building only for AppleScript users abandons the newcomers.

## Power User UX vs. Novice UX

Soghoian does not believe in collapsing the distinction between power user UX and novice UX. He believes both are legitimate and both deserve serious design attention — but they serve different goals, and designing only for novices at the expense of power users is a choice with real costs.

The novice UX for automation is about discovery: showing users what is possible, giving them templates and starting points, making the first successful automation feel achievable. Automator's library browsing and template system serve this purpose. Shortcuts' gallery of pre-built shortcuts serves it on iOS.

The power user UX for automation is about control: giving experts the granular access they need to handle edge cases, combine arbitrary data sources, and build automation that no pre-built template anticipated. The AppleScript console, the scripting dictionary, the ability to query an application's full object hierarchy — these serve this purpose.

When Apple reduced Automator's development effort in the early 2010s and moved emphasis toward simpler automation metaphors, Soghoian publicly argued that the power user UX had been deprioritized in ways that would cost Apple its most loyal professional customers.

## Automation as User Capability, Not Convenience Feature

A key UX conviction for Soghoian is that automation is not primarily a convenience feature — it is a capability feature. There is a qualitative difference between an automation that saves a user thirty seconds and an automation that enables a workflow that was previously impossible. The latter is what he has always been most interested in. When Showtime Networks used AppleScript to produce 800-1000 menus per month automatically, they were not saving time — they were doing something they otherwise could not do at all.

UX design that treats automation as a convenience ("swipe to automate!") misses this entirely. The users who need automation most are the ones doing things that are genuinely not possible otherwise, and those users need a UX that takes their needs seriously.
