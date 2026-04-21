# Paul Hudson — On Safety

## Accessibility as a Legal and Ethical Requirement

Paul Hudson's most direct statement on accessibility as an obligation comes from his tutorial series: "Accessibility isn't something that's 'nice to have' — it should be regarded as a fundamental part of your application design, and considered from the very beginning onwards." (hackingwithswift.com/books/ios-swiftui/accessibility-wrap-up)

He teaches that in many jurisdictions — particularly in the United States (Section 508, ADA) and across the European Union — apps distributed commercially are subject to accessibility requirements. An app that does not work with VoiceOver, does not support Dynamic Type, or does not accommodate reduced motion preferences is not just a design failure. For apps targeting government services, education, or broad consumer audiences, it may be a legal liability.

His practical response is to make accessibility instruction inseparable from iOS development instruction. Learners who complete any of his major courses have been exposed to VoiceOver labels, Dynamic Type support, Reduce Motion detection, and proper accessibility traits as part of the normal workflow — not as a compliance module at the end.

## Privacy in iOS Apps

Hudson teaches Apple's privacy model as a default assumption in iOS development. His tutorials cover:

- **Permission requests** — how to request camera, microphone, location, and biometric access correctly, including the requirement to provide clear usage descriptions in Info.plist that explain to users why the app needs a capability
- **Biometric authentication** — teaching Face ID and Touch ID implementation through the LocalAuthentication framework, including fallback handling when biometrics are unavailable
- **Keychain storage** — covering secure storage for sensitive data rather than using UserDefaults or plain text files for credentials and tokens

These topics appear throughout his project-based curriculum because the apps he teaches learners to build — to-do apps, notes apps, photo apps — encounter these requirements naturally. Privacy handling is not abstracted away as an advanced topic; it appears when learners first build an app that needs a camera or needs to store a password.

## Security Best Practices in Swift Tutorials

Hudson's approach to Swift code examples emphasizes correct practice from the start. This includes:

- **Error handling** — his tutorials teach proper use of `try`, `catch`, and `throws` so learners do not develop habits of ignoring errors that could indicate security-relevant failure states
- **Avoiding force unwrapping** — he teaches defensive Swift that checks for nil rather than force-unwrapping optionals, which prevents crashes that can expose unexpected application states
- **Network requests** — tutorials cover URLSession with appropriate handling of HTTPS connections, errors, and response validation

The 2023 "I screwed up" article about accessibility demonstrated an important behavior: when Hudson discovers his own teaching has contained an error — even a subtle one — he publishes it publicly and commits to fixing it across the entire catalogue. This models a professional approach to safety and correctness that goes beyond the specific accessibility issue he identified.

## What Hudson Does Not Cover

He is not a security researcher and does not publish content on penetration testing, vulnerability disclosure, cryptographic implementation, or application threat modeling. His security and privacy coverage is practical developer education — how to use iOS APIs correctly — rather than adversarial security analysis.

His 2025 app Hacktivate explores capture-the-flag security challenges, which suggests growing interest in the security education space, but the app is positioned as a learning tool for computer science skills rather than professional security training.

## Gap Note

Hudson does not write extensively about data retention policies, GDPR compliance workflows, privacy impact assessments, or legal compliance frameworks beyond what Apple's own App Store guidelines and Human Interface Guidelines cover. For legal compliance specifics, his teaching is a starting point rather than authoritative guidance.

## Sources

- hackingwithswift.com/books/ios-swiftui/accessibility-wrap-up
- hackingwithswift.com/articles/261/i-screwed-up-one-key-accessibility-behavior-and-now-i-m-on-a-mission-to-do-better
- hackingwithswift.com (LocalAuthentication, Keychain tutorials)
- x.com/twostraws/status/1980329586463502561 (Hacktivate, 2025)
