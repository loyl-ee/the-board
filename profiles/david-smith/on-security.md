# David Smith — On Security

## Privacy Architecture: No Third-Party Data Collection

Smith's security and privacy architecture is built on a single principle: his apps do not send user data to third parties. There is no analytics SDK (no Mixpanel, no Firebase Analytics), no crash reporting that transmits without consent, no advertising framework, no A/B testing platform. The consequence: there is no user data at risk from a third-party breach.

The security engineering argument: every third-party SDK you integrate is a potential security vulnerability and a data collection mechanism outside your control. The SDK author's security practices, their data retention policies, and their response to law enforcement requests are outside your control. Minimise third-party code that has access to user data.

## HealthKit Security: Handling Sensitive Data

Smith's health apps — Pedometer++, Sleep++, Heart Analyzer — integrate with HealthKit, which stores some of the most sensitive user data on the device: health conditions, medications, reproductive health, sleep patterns. The security engineering requirements for HealthKit apps are specific: request only the HealthKit data types your app needs (principle of least privilege), explain clearly why you need each type before requesting it, and never retain HealthKit data outside of HealthKit.

The security discipline: health data that is not stored in your database cannot be breached from your database. Keep sensitive data in the platform-provided secure store (HealthKit, the iOS Keychain) rather than in your own persistence layer.

## App Store as a Security Boundary

Smith has discussed the App Store review process not just as a quality control mechanism but as a security boundary: Apple's review catches malware, validates entitlements, and ensures apps cannot access resources they have not declared. For users of Smith's apps, the App Store review provides a baseline security guarantee.

The security engineering implication: platform security controls that exist should be used correctly, not worked around. The correct use of App Store entitlements, sandboxing, and permission prompts is a security feature, not a compliance obligation.

## Transparency as a Security Practice

Smith publishes regular income reports and is transparent about the business decisions behind his apps. This transparency extends to privacy: his apps' privacy policies are written to be readable, not to obscure what is collected. A readable privacy policy is a security commitment — it creates accountability for the claims made.

The engineering standard: privacy policies should accurately describe what data is collected, how it is used, and how it is protected. A privacy policy that no one can read is not a security measure — it is cover for practices that cannot withstand scrutiny.

## iCloud Sync as a Security Architecture Decision

Several Smith apps use iCloud for sync rather than building a custom backend. The security argument for this: iCloud is maintained by Apple with Apple's security engineering resources, benefits from Apple's security investments, and does not require Smith to maintain a backend with user data. A backend Smith does not operate cannot be breached by attacking Smith's infrastructure.

The engineering principle: for data sync and storage, evaluate cloud platform providers by their security posture, not just their API convenience.

## Sources
- [david-smith.org — Smith's blog and privacy statements](https://david-smith.org/)
- [Widgetsmith privacy policy — public](https://apps.apple.com/app/widgetsmith/id1523682319)
- [Apple HealthKit security documentation](https://developer.apple.com/documentation/healthkit)
- [Developing Perspective podcast — privacy episodes (archived)](https://developingperspective.com/)
