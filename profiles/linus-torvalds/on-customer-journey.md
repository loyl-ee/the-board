# Linus Torvalds — On Customer Journey

## The Community as the Product

Torvalds has never framed Linux's users primarily as customers. The early framing was more radical: contributors are the product's co-authors, users are beneficiaries of the contributors' work, and the health of the contributor community determines the quality of the software. This is a different model from commercial software, where the customer relationship is distinct from the production relationship.

His view of this in the TED talk (2016): "Without doing the whole open source and really letting go thing, Linux would never have been what it is." The "letting go" was the decision to license under the GPL and accept patches from strangers — which meant accepting that the project would be shaped by people he did not know and could not control. The community became the primary unit of value.

## Meritocracy as Admission Policy

Torvalds' model for patch acceptance is explicit: code quality is the criterion, not the contributor's identity, seniority, or organizational affiliation. He has stated: "I'm 'special' only because — and as long as — people trust me to do a good job. And that's exactly how it should be" (Tag1 Consulting interview, 2020). His authority derives from demonstrated judgment, not from founding the project. This is how he expects the whole system to work.

In practice, this means patches from first-time contributors get the same technical review as patches from long-time maintainers. A patch from a senior Google engineer gets rejected if the code is wrong; a patch from an unknown student gets accepted if it is correct and well-written. This meritocratic model is the stated ideal. Its actual implementation has been contested — the Linux kernel community has had documented problems with inclusivity, which partly motivated the 2018 Code of Conduct — but the principle remains the explicit governance philosophy.

## Trust as the Infrastructure of Collaboration

In his 2021 Tag1 Consulting interview, Torvalds named trust as the single most important resource in a distributed open source community: "The most important thing is that you can trust each other. Because trust matters. A lot." He described the kernel's development model as a "network of trust" — he trusts a small set of maintainers who trust their own subsystem contributors, and the whole system scales because trust does not need to pass through a central bottleneck.

This model has specific structural requirements. Discussions must happen on public mailing lists with no membership barriers. There must be no important private conversations that create information asymmetry. Decisions must be made on the basis of visible technical arguments. He has explicitly warned against "cliques" — small groups who make decisions privately and present them to the community as settled matters.

## Documentation and Accessibility

Torvalds' attitude toward documentation is that it should exist but it is not his primary concern — his primary concern is the code. The Linux kernel has historically been better documented through its mailing list archives and comments than through formal documentation, partly because Torvalds views formal documentation as something that lags the code and creates false impressions of definitiveness.

For contributors trying to understand the project's expectations, the LKML archives function as a living documentation of what is and is not acceptable. The coding style guidelines (originally in the kernel source itself under Documentation/process/coding-style.rst) are another form of onboarding documentation. Both reflect the same principle: if you want to know how the project works, look at what the project actually does, not at what any document claims it does.

## The Path from User to Contributor

The Linux development model has a well-understood gradient from user to contributor: file a bug report, submit a small fix, submit a larger fix, become a subsystem maintainer. Each step involves more trust being extended by maintainers above you in the network. Torvalds' advice on entering the community — implied by his public statements about what gets patches accepted — is to start small, demonstrate good taste, and let the code speak.
