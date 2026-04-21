# On UX — Mattt Thompson

## API Design Is UX Design

Thompson's core UX insight is that APIs are user interfaces — the users happen to be developers, but the UX concerns are structurally identical. Discoverability, learnability, error recovery, and the emotional response to failure are all present in API interactions just as they are in consumer software. His entire body of work on AFNetworking and NSHipster is, viewed through this lens, a sustained argument for treating developer experience as a first-class UX discipline.

His AFNetworking 2.0 redesign operationalized this. The architectural decision to separate concerns into subspecs, the introduction of serializer protocols, the removal of complex registration patterns — each was a UX decision. Less configuration to achieve the common case. Fewer surprises when something goes wrong. Clearer conceptual model when the developer needs to extend the framework.

## Good Defaults as Respect for the User

Thompson's Principle of Least Surprise — articulated in the NSHipster book as "clear intent, reasonable defaults, and control" — is a UX philosophy before it is a technical one. Good defaults are a form of respect: they express the designer's judgment about what the user most likely wants and spare the user the burden of specifying it. Thompson's API designs consistently followed this principle: AFNetworking assumed JSON serialization by default because that was the common case; deviating from the default required explicit configuration rather than luck.

The counterpart to good defaults is *progressive disclosure*: the recognition that the full complexity of a system should be accessible but not initially visible. A well-designed API surface allows a developer to accomplish the common task in three lines, and also allows a developer to customize every aspect of the process when needed. Thompson did not coin this principle, but his frameworks and writing consistently practice it.

## Error Handling as Empathy

One of the most distinctive aspects of Thompson's UX thinking is his treatment of error handling as an act of empathy. His NSHipster article on `NSError` argued that error objects should carry human-readable information — `localizedDescription`, `localizedRecoverySuggestion`, `localizedFailureReason` — specifically because errors are the moment when a developer needs to understand what went wrong and communicate it to a user. Poor error design (cryptic codes, missing context, unhelpful messages) represents a failure of care toward both the developer and the eventual end user.

His observation that networking error documentation was "scattered" and made debugging "-1004" errors "surprisingly difficult" is a UX critique of Apple's own developer experience — an acknowledgment that even high-quality platforms produce UX failures, and that those failures have real costs in developer time and product reliability.

## The Human Dimension of Technical Communication

His NSHipster essay "Empathy" (March 2014) extends UX thinking beyond API surfaces to the experience of being a developer in a community. "Lacking many of the faculties to humanize and understand one another (facial expressions, voice tonality, non-verbal cues) we can lose sight of who we're talking to, and become less human ourselves." This is, effectively, a UX analysis of developer community platforms — GitHub issues, mailing lists, Stack Overflow — and the failures of empathy they produce.

His prescription is behavioral: before engaging, visualize the encounter in person. This is not a platitude but a specific UX intervention — using mental simulation to recover the social context that digital interaction strips away.

## What This Means for Product Decisions

Thompson's UX framework implies that any product decision touching a developer workflow should be evaluated by the same criteria as a consumer UX decision: How confusing is the first-use experience? What is the error message when something goes wrong? Does the default behavior match what most users need? Can advanced users get to the controls without wading through complexity intended for beginners? These questions apply whether the product is a framework, a CLI tool, a developer dashboard, or an API endpoint.
