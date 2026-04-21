# Swyx — Core Philosophy

## Learn in Public

The idea that made swyx famous before the AI Engineer framing is "Learn in Public" — published at [swyx.io/learn-in-public](https://www.swyx.io/learn-in-public) and now read by millions. The core claim is disarmingly simple: most people "learn in private," consuming content and accumulating knowledge without producing any artifacts of that learning. Swyx argues this is a missed opportunity — for the learner, for their community, and for the web.

His prescription: create "learning exhaust." Write blog posts, record videos, answer questions on Stack Overflow, give talks at meetups, maintain cheatsheets, build in public. Crucially, the primary audience is not followers or employers — it is your past self. "Make the thing you wish you had found when you were learning." The biggest beneficiary of helping past-you is future-you.

He is explicit that this is not about performing expertise. "Try your best to be right, but don't worry when you're wrong. Repeatedly." The public nature of the work creates an error-correction mechanism that private learning lacks: others will point out mistakes, and corrections compound over time. He calls this trading "self review for peer review and increased velocity."

The mechanism that makes this more than self-help advice is what he calls "luck surface area." By doing more things and telling more people about them, learners attract mentors, opportunities, and serendipitous collaborations that are structurally unavailable to those learning privately. His essay "How to Create Luck" ([swyx.io/create-luck](https://www.swyx.io/create-luck)) extends this into a framework: luck is not purely random — it is a function of exposure, preparation, and accumulated signal.

A parallel document, the [Digital Garden Terms of Service](https://www.swyx.io/digital-garden-tos), establishes the social contract for learning in public spaces: the right to be incomplete and wrong, the obligation to steelman opponents, the duty to correct mistakes promptly, and the expectation that criticism is welcome if constructive.

## The AI Engineer as a Distinct Role

Swyx's second major philosophical contribution is defining what an "AI Engineer" actually is and why this role is categorically different from both ML researchers and traditional software engineers.

In "The Rise of the AI Engineer" (June 2023), he argues that a talent-supply mismatch creates an entirely new discipline. There are approximately 5,000 LLM researchers globally but 50 million software engineers. Foundation models have made powerful AI capabilities available via API. The natural result: a large class of engineers who build *with* AI rather than *of* AI will emerge. These engineers need different skills, different training pathways, and different community infrastructure than either existing group.

He identifies three stages of AI engineering development:
1. **AI-enhanced engineers** — developers using AI tools (Copilot, Cursor) to improve their own productivity
2. **AI products engineers** — developers building products that expose AI capabilities to end users via APIs
3. **AI agents engineers** — developers delegating significant work to agents that execute autonomously

The key insight is that "one can be quite successful in this role without ever training anything." His examples of highly effective AI Engineers — Simon Willison, Riley Goodside, Pieter Levels — have no formal ML backgrounds. They succeeded by learning quickly, building rapidly, and understanding the capability envelope of existing models.

He is also specific about what AI Engineering is *not*: it is not pure prompt engineering. "Prompt Engineering is Overhyped" is a position he holds explicitly — the real skill is going "beyond the Prompt Engineer and write *software*." The AI Engineer combines traditional software engineering fundamentals (90% of the job, he says) with enough understanding of AI systems to architect products responsibly.

## Software 3.0 as Paradigm Shift

Swyx builds on Andrej Karpathy's "Software 2.0" framing (neural networks as code) and extends it. In his "Software 3.0 and the AI Engineer Landscape" talk ([swyx.io/ai-landscape](https://www.swyx.io/ai-landscape)), he argues that the most important shift is that "the hottest new programming language is English" — foundation models generalize across domains in ways that earlier neural network systems could not.

Software 3.0 is not purely about prompts. He frames it as a "Code Core vs. LLM Core" architecture: successful AI applications combine human-written code that orchestrates LLM capabilities with the LLMs themselves. The skill of composing these two is what AI Engineering requires.

## Community as Infrastructure

Swyx has consistently treated community building as a technical discipline, not a marketing function. His career in developer relations at Netlify, AWS, Temporal, and Airbyte gave him a systematic view: the North Star metric for developer communities is "monthly active developers," and DevRel's value lies in enabling the community to teach each other at scale, not in reach alone.

He applies this to the AI Engineer community explicitly. His conferences are designed not as networking events but as community-defining moments — analogous to NeurIPS for ML researchers or KubeCon for cloud-native engineers. The goal is to give the AI Engineering discipline the shared vocabulary, shared problems, and shared institutions it needs to cohere as a field.

## Building Taste Through Consumption

A thread across all of swyx's philosophy is that good judgment must be earned before it can be exercised. He describes a "taste gap" — the period when a learner can recognize quality they cannot yet produce. His advice: spend time in that gap, producing anyway, learning in public, receiving correction. The path through it is not waiting but building — accepting the failure rate that comes with high-volume creative output and using curation ("saying no a lot") to extract quality from quantity.

This applies to AI products specifically: building a dozen small experiments ("smol" projects) before trying to build the definitive version is not a failure to commit — it is how builders develop the taste required to commit correctly.
