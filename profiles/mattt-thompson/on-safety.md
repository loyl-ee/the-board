# On Safety — Mattt Thompson

## Security in iOS Development

Thompson has addressed iOS security in his NSHipster writing, most directly through his framing of secret management as "one of the great unsolved questions in iOS development" — specifically: "How do I store secrets securely on the client?" This honest acknowledgment of an unsolved problem is characteristic: rather than providing a false resolution, he identifies the genuine tension between developer convenience and security hygiene on a platform where app binaries are distributed to untrusted devices.

His NSHipster article on Device Identifiers and Fingerprinting on iOS (October 2019) engaged with privacy as a security concern — examining how device identifiers can be used to track users across apps and sessions, and how Apple's deprecation of older identifier APIs represented an attempt to limit this surface area. The article treats privacy and security as developer responsibilities, not purely platform problems.

## Responsible Open Source Maintenance

Thompson's most developed thinking on safety comes through his "Stewardship" article (January 2014), which treated the responsible lifecycle of an open source library as an ethical obligation. A library widely adopted by other developers carries safety implications: a breaking change, an unannounced deprecation, or an unmaintained security vulnerability can propagate to every product that depends on it.

His practical framework for responsible stewardship included: semantic versioning as a contract with consumers, clear deprecation announcements, migration guidance when sunsetting, and credit to contributors. The AFNetworking deprecation notice (January 2023) — which formally acknowledged the library's end of life and directed users to Alamofire — was consistent with this framework, even if it came years after Thompson had stepped back from the project.

## The Ethics of Widely-Used Libraries

AFNetworking, at its peak, ran on the majority of iOS devices. This scale creates ethical weight: a security vulnerability in AFNetworking was not a problem for one product but a problem across an ecosystem. Thompson was aware of this — his emphasis on the AFNetworking community as "the most important feature" of the library reflects an understanding that maintenance is a distributed responsibility precisely because the blast radius of failure is distributed.

## Honest Gap Note

Thompson's public writing does not address security engineering in depth. He has not published NSHipster articles on cryptography, certificate pinning implementation, or secure networking protocols in technical detail. His security-related writing is more about developer awareness and responsibility than about security engineering practice. For deep iOS security architecture decisions, Thompson's perspective is that of an engaged generalist rather than a security specialist. His value is in framing security as a developer responsibility, not in providing specific hardening guidance.
