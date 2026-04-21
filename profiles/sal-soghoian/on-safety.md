# Sal Soghoian — On Safety

## The Tension at the Center

Automation's power and security's constraints exist in genuine tension, and Soghoian has spent significant parts of his career managing that tension rather than dissolving it. His position is not that security doesn't matter — it is that security measures which disable automation capabilities represent a net loss for users, and that this trade-off deserves to be made consciously rather than as an unintended side effect of platform policy.

## Sandboxing and the Cost to Automation

The introduction of App Sandbox requirements for Mac App Store applications created serious problems for AppleScript-dependent software. Sandboxed applications cannot send Apple Events to other applications without requesting specific entitlements — and those entitlements require both developer action and user approval. The practical effect was that workflows which had worked reliably for years silently broke when the applications involved were updated to comply with sandboxing requirements.

Soghoian and Apple engineer Chris Nebel co-presented a WWDC session specifically addressing this tension: "Secure Automation Techniques in OS X." The session documented the new sandboxing constraints and how developers could work within them. The fact that a dedicated session was necessary speaks to how significant the disruption was: sandboxing had effectively treated inter-application communication as a security threat rather than a feature.

From Soghoian's perspective, the problem was one of priorities. The sandbox is designed to protect users from malicious applications doing things they didn't authorize. But it applied the same restrictions to automation scripts that users had explicitly written and chosen to run — scripts that represented the user's own intent, operating at the user's own authority level. His core argument, expressed throughout his career, is precisely that user automation "operates with the user's level of authority" — it does what the user could do manually, not what the user has restricted. Treating user-authored automation as a threat conflates two very different kinds of software.

## macOS Mojave and the Permission Parade

The automation security picture became more complex with macOS Mojave, which introduced approval dialogs for Apple Events: the first time a script sends an Apple Event to an application, the user must explicitly approve it. This was a genuine security improvement — it prevented scripts from silently controlling applications the user had not authorized. But it also created friction for established automation workflows, requiring users to approve interactions they had effectively already authorized by writing and running the script.

Soghoian's response to this kind of tension is characteristic: he acknowledges the security rationale while pushing back on implementations that prioritize security theater over user empowerment. A permission dialog that appears once and is then remembered is a reasonable design. A permission dialog that interrupts a long-running automated workflow at the worst possible moment is a design failure, regardless of its security motivation.

## Privacy in Automation: The Local-First Principle

Soghoian's post-Apple thinking on safety has extended into data privacy, shaped in part by his nephew Christopher Soghoian's work as a privacy researcher and activist. His guiding principle is explicit: "Once your data leaves your 'home,' it loses legal protections." (Rebooting interview, 2023.) His practical rule is to avoid joining the food chain — to keep data local and prefer automation tools that run on device rather than sending data to cloud services for processing.

This preference for local-first automation is both a privacy position and an autonomy position. Cloud-based automation tools can be discontinued, changed, or monetized in ways the user cannot control. Device-resident automation remains under the user's control as long as the device runs.

## What Responsible Automation Design Looks Like

From Soghoian's perspective, responsible automation design involves: clear user authorization for what automation can access; transparency about what a script or workflow does; preference for tools that keep data local; and security constraints that are calibrated to actual threat models rather than applied uniformly to all inter-application communication. The failure mode he opposes most strongly is security that treats the user's own automation tools as adversaries.
