# David Smith — On Safety and Privacy

## The Core Commitment: Your Data Is Your Own

Smith's privacy philosophy is stated plainly in his Pedometer++ privacy policy: "Your data is your own. We make no claims to it and will only use it according to the policies outlined below." This is not boilerplate — it reflects a genuine architectural commitment that shapes how his apps are built.

His health apps (Pedometer++, Sleep++, Workouts++) integrate with Apple's HealthKit. The health data read from HealthKit is used solely within the app and is never collected, transmitted, or disclosed outside the user's local device. This is enforced at the data architecture level: the apps are built to not have access to a server that could receive health data even if they wanted to transmit it.

## The No Third-Party Analytics Position

For a developer who talks frequently about data and metrics, Smith's decision to avoid third-party analytics in his health apps is notable. He has not embedded Firebase, Mixpanel, Amplitude, or similar analytics SDKs into his health tracking products. The explicit rationale is that health data — step counts, sleep duration, heart rate variability — is among the most sensitive data a person generates, and any third-party SDK integrated into an app that touches this data introduces a privacy risk the user did not knowingly accept.

This extends to advertising. Pedometer++ and Sleep++ display ads for non-subscribers (using Google's AdMob), but Smith has explicitly disabled personalized ads and "all of Google's user tracking and analytics capabilities." The ads are contextual and non-personalized. This is a deliberate revenue compromise in service of privacy: he forgoes the higher CPMs that personalized ads command in order to honor a privacy commitment to users who have not paid for premium access.

## Health Data Sensitivity as a Design Constraint

Smith's sensitivity to health data shapes product decisions beyond privacy policy. He is careful about how sleep quality data is presented because the emotional stakes are higher than with step counts. A user who learns they slept poorly has received information they may find distressing, and Smith designs around this: the default presentation of Sleep++ data is supportive rather than judgmental, and he has written explicitly that he does not want to be "too dramatic" about health goal failures that may be outside a user's control.

This extends to the readiness score feature: he states that "it is important to treat this value as an indicator and not a clinical measurement." He is careful not to let his apps make health claims they cannot substantiate or create anxiety about data that is inherently approximate.

## Responsible Data Architecture: No Unnecessary Servers

Smith's "don't run servers" philosophy (documented extensively on Under the Radar) has a privacy dimension beyond the operational one. A server that receives user data creates a target for breaches, a legal obligation to protect and notify, and a business incentive to monetize that data. By building apps that process data locally on the user's device — leveraging Apple's HealthKit, CloudKit, and on-device computation — Smith avoids creating this vulnerability in the first place.

For Widgetsmith's shared photo widgets, he chose to use iCloud shared albums rather than a custom backend. This meant user photos never passed through his infrastructure: Apple stored them, Apple secured them, and Apple's privacy practices applied. He describes this as "avoiding privacy liability while maintaining functionality."

## Transparency Through Privacy Policies

Smith's privacy policies are notably readable. They explicitly list which third-party services receive what data, link to those services' own policies, and clearly distinguish between data that stays local and data that is transmitted. The Pedometer++ privacy policy, for example, specifies exactly what Mapbox and GPXZ receive when a user requests route planning or elevation data (GPS waypoints) and what Thunderforest receives for mapping tiles (general area data, not precise location).

This level of specificity reflects a philosophy of informed consent: users should be able to understand what is happening with their data, not just be presented with a legal document that technically satisfies disclosure requirements.

## Privacy as Competitive Differentiation

Smith has not written about privacy primarily as a competitive strategy, but the effect is real. In a landscape where many free apps monetize user data, his health apps attract users who specifically want a trustworthy alternative. Reviews of Pedometer++ and Sleep++ frequently cite privacy as a reason for choosing them over competitors. This is particularly relevant in health, where user data can include sensitive behavioral patterns that users are reluctant to share with unknown parties.

The irony is that by choosing not to collect data, Smith also limits his own product intelligence. He cannot run cohort analyses, study funnel drop-offs in the traditional sense, or personalize recommendations based on behavioral history. This is a deliberate trade — he has chosen to be a developer users can trust over a developer who optimizes every metric.
