# Pieter Levels — On Product

## MVPs in Days, Not Months

Levels' core rule: the prototype must be launchable within one month, and ideally within one to two weeks. Extended development without user validation is, in his view, a form of self-deception — you are building confidence in your idea by investing time rather than testing it against reality.

His 2014 blog post "How I build my minimum viable products" describes his actual process: sketch on paper, build a Photoshop mockup, construct the HTML/CSS version, implement responsive design, then add backend functionality. The sequence runs days, not months. He runs all sites on a single Linode VPS ($40/month), deploys via SSH in 15 minutes, and uses JSON text files as data storage for the first version rather than spending time on database architecture. (levels.io/how-i-build-my-minimum-viable-products/, 2014.)

The lesson is not that speed produces better products — it is that speed produces *validated* products faster. A bad product launched in a week generates feedback in week two. A bad product spent six months developing generates feedback six months late, with six months of sunk cost.

## Build What You Personally Need

Every major Levels product originated from direct personal experience of the problem. Nomad List was built because he was traveling as a nomad and had no structured way to compare cities for cost, internet speed, and safety. Remote OK was built because he needed remote work himself and found existing remote job sites poorly designed. PhotoAI emerged from his own frustration with professional headshots while traveling — he noticed that having good photos of yourself matters for social profiles but getting them required studios he couldn't access as a nomad.

He states in the MAKE book: "Always start from the problem, not the solution." This is not a platitude in his case — it is a strict operational filter. Products he has built for abstract "market opportunities" rather than personal friction have consistently underperformed.

## The "Just Ship It" Doctrine

Levels treats launching as the beginning of the product's life, not the end of development. The first version is often embarrassingly minimal. Nomad List 1.0 was a single spreadsheet. Remote OK launched as a simple aggregator. InteriorAI launched with a single input (upload a photo, get a redesign). This minimalism is intentional: it forces the product to stand on its core value proposition with no feature padding.

"Scrappy is the best way to validate new products or features and iterate towards making something that people actually want." (levels.io/deviance/.) The sequencing matters: ship, observe, iterate — not plan, plan, plan, then ship.

## Nomad List as Product Laboratory

Nomad List is Levels' most documented product-building case study. Its evolution illustrates his iterative approach:

- **Version 1** (2014): A Google Spreadsheet crowdsourced from Twitter.
- **Version 2**: A website pulling data from that spreadsheet.
- **Version 3**: Paid membership added ($5, later $99/lifetime, later recurring subscriptions).
- **Version 4**: Slack community integrated; members could find other nomads in the same city.
- **Version 5**: $300K–$400K/year, 1,250 cities, 250,000+ data points, nomad dating, climate finder, FIRE calculator.

Each version added only what users were actually requesting, funded by revenue from the previous version. No roadmap existed beyond the next user complaint worth solving.

## AI Products as Rapid Market Experiments

When Stable Diffusion became available on consumer hardware in late 2022, Levels treated it as a raw material for rapid experiments — not a technology to study, but a capability to ship. InteriorAI launched in September 2022 within weeks of the model becoming accessible. It went viral immediately and hit $10K in its first week, eventually reaching $40–50K/month.

PhotoAI launched February 2023, after Levels observed that people wanted professional-quality photos of themselves but had no easy, affordable path to get them. The product generated $87K MRR ($1M ARR) within 17 days of launch — the fastest any of his products had ever scaled. He has been transparent that this speed was partly a function of the 600K Twitter audience he spent a decade building: one mention from an influencer moved MRR from $12K to $40–50K overnight.

The AI products demonstrate his product philosophy applied to a new paradigm: find a problem the new technology creates a solution for, build the minimum version quickly, charge immediately, and iterate based on who pays and who churns.

## Iterating Based on Actual Usage

Levels distinguishes between what users *say* they want and what they actually do. His preferred method of insight is watching usage data and revenue signals rather than running formal user research. Features that get used survive; features that don't get used get removed or ignored.

He also maintains tight feedback loops: his products have featured visible feedback boxes and feature request mechanisms throughout their history. The Nomad List Slack community functioned as a real-time user focus group — active members were the heaviest users and loudest voices about what was broken.

The "hard part," he has said, "is figuring out what you shouldn't add, which you shouldn't build because you don't have time." (Lex Fridman Podcast #440, 2024.) For a solo operator, feature restraint is as important as feature velocity.

## Portfolio Product Strategy

Levels treats his portfolio of products not as competitors for his attention but as a diversified system. When one product's revenue plateaus or declines (as Nomad List did somewhat post-2020), other products compensate. When the remote work market normalized post-COVID, Remote OK's job listing revenue dipped, but PhotoAI's rapid growth absorbed the gap.

The strategic insight is that solo makers can sustain multiple small products simultaneously because automated infrastructure amortizes across the portfolio. One server, one payment system, one deployment pipeline, one support inbox can serve five products almost as easily as one. This is a fundamentally different model than the "single product company" that most startup advice optimizes for.
