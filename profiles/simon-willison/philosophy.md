# Simon Willison — Core Philosophy

## Document Everything, Publicly

The foundational pillar of Willison's intellectual life is radical public documentation. He has blogged at simonwillison.net every working day since June 2002 — over two decades. On his 20th blog anniversary he reflected that he still does not see himself losing interest "for many decades to come." He maintains a TIL (Today I Learned) site at til.simonwillison.net where he posts short notes whenever he figures out anything new, no matter how basic. His explicit philosophy: even with 25 years of professional experience, you should celebrate learning even the most basic of things.

In a November 2022 post titled "What to blog about," he articulates his writing ethic plainly: "Writing about something is the cost I have to pay for building it." He recommends treating "write about it" as part of your definition of done for anything you build or create. He says a TIL "is the most liberating form of content I know of" because it carries no expectation of authority — only "I just figured this out: here are my notes, you may find them useful too."

This is not modesty performance. It is a deliberate epistemic strategy. By narrating his learning in real time, he creates durable reference for his future self, builds community, and surfaces his work to people who might find it useful. He notes there are "selfish benefits" to working in public: the discipline of writing forces clarity, and a blog becomes an externalized memory that outlasts any single project.

## Learning in the Open

Willison coined the phrase "learning in the open" to describe his practice. He defaults to sharing. He treats his blog less like a publishing platform and more like a running notebook that happens to be public. This extends to his TIL posts, his Substack newsletter, his annotated talk transcripts, his GitHub issues (which he uses as development diaries), and his social media. When he makes a mistake, he documents it. When something surprises him, he documents it. When he changes his mind, he writes about why.

He explicitly argues that the amount of influence a person can have on the world by consistently blogging about a subject "is just as high today as it was back in the 2000s when blogging first started." Naming things matters to him: he has argued that "if you really want people to engage with a technique, it's helpful to give it a name." He did this with "prompt injection," "git scraping," "baked data," "slop" (which he popularized), and "vibe engineering." Naming is an act of conceptual infrastructure.

## Tools for Thought, Tools for Journalists

Willison's work is anchored in a specific user archetype: the data journalist. This is not accidental — he worked at The Guardian on data journalism, spent a year as a JSK Journalism Fellow at Stanford specifically to build tools for journalism, and has repeatedly stated his goal is to write software that helps a journalist win a Pulitzer Prize. Datasette was built to make it possible for journalists with no programming background to explore and publish structured datasets.

This orientation shapes his entire approach to tool design. He does not build for himself alone. He builds for the person who has the data and the story but lacks the technical infrastructure to get from one to the other. He is interested in "tools for thought" as a category — tools that extend what someone can understand or communicate, not just automate existing work.

## Pragmatic AI Use: What Works, Not What Is Theoretically Impressive

Willison has been among the most important voices pushing back against AI hype. He insists on evaluating tools empirically — on the basis of what they demonstrably do, not what they might theoretically be capable of. His annual year-end reviews ("Stuff we figured out about AI in 2023," "Things we learned about LLMs in 2024," "2025: The year in LLMs") are exercises in evidence-based synthesis. He writes about what he has tried, what worked, what failed, what surprised him.

He coined the memorable phrase that LLMs are "fancy autocomplete" — not as dismissal, but as a corrective to anthropomorphization. He insists on this characterization precisely because accurate mental models lead to better decisions. If you think the model understands you, you will be confused when it fails; if you understand it is predicting tokens, you will know when to trust it and when to verify.

He has been vocal that the best current use case for LLMs is code generation, partly because code can be verified by running it. "You can run generated code to see if it's correct" is one of his key arguments for why code is the domain where LLM assistance is most reliable. He extends this to his golden rule: he will not commit any code to his repository that he could not explain to someone else, regardless of whether an LLM wrote it.

## Prompt Engineering as Legitimate Craft

Willison takes prompt engineering seriously as a discipline. He pushes back against dismissals of it as "just talking to the computer" and equally against overclaiming it as secret sorcery. In his 2023 year-end review he acknowledged that prompt engineering remains "vibes-based" — there is no rigorous scientific methodology for determining whether a prompt improvement is real. But he argues the craft is real even if the measurement is hard. He has written extensively about structuring prompts, managing context, using system prompts, and the specific challenges of different model families.

## The Perfect Commit and Software Craft

Willison's software practice is governed by what he calls "the perfect commit": a commit that bundles together the implementation, tests, documentation, and a link to an accompanying issue thread. He writes: "The commit is our principal unit of work. It deserves to be treated thoughtfully and with care." This philosophy reflects a broader commitment to software as a craft that deserves methodical attention, not heroic improvisation.

## Openness as Strategy, Not Ideology

Willison is an open source developer but he is not an ideological purist. He works in open source because he believes it is strategically correct for his goals: he wants his tools to be adopted widely, to outlast any single organization's interest, and to be improved by contributors he cannot predict in advance. He advocates building exclusively on open source "because most ventures eventually decline, making proprietary code a poor long-term investment." His plugin architecture for both Datasette and LLM reflects this: plugins allow the ecosystem to grow without requiring his review or approval.
