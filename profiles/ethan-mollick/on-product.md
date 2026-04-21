# Ethan Mollick — On AI Products

## Note on Scope

AI product design is not Mollick's primary research domain. His thinking on products is inferential — derived from his research on AI adoption, his experiments with AI-enabled workflows, and his writing on what actually makes AI useful versus performative. These inferences are nonetheless high-signal because they come from someone who has watched hundreds of people encounter AI for the first time and documented what actually happens.

## The Gap Between Demos and Real Use

Mollick observes a consistent pattern in AI product adoption: what works in demonstrations rarely maps directly to what produces value in genuine daily use. The demo shows the best-case output. Real use involves the user's inability to write a prompt that elicits that output, frustration with hallucinations in contexts where accuracy matters, and abandonment when the product fails to deliver on its demo-level promise.

His research evidence: a study of doctors using GPT-4 for diagnosis showed no performance improvement compared to those without AI — despite AI's demonstrated diagnostic capability in controlled settings. Mollick attributes this to "algorithmic aversion" (distrust of machine recommendations) and the gap between theoretical capability and practical prompting skill. The AI was capable. The product workflow did not bridge that gap.

The implication for product design: a feature that impresses in a demo and fails in daily use is not an AI problem — it is an onboarding and interaction design problem. The capability exists. Getting users to the point where they can reliably access it is the product challenge.

## Genuine Utility vs. Performative AI

Mollick's framework for evaluating AI features is implicit but consistent across his writing. Genuine utility has these characteristics:

- It saves meaningful time or expands meaningful capability on tasks users actually need to do
- Users can verify whether the output is correct in their domain of expertise (they are "expert enough to spot its mistakes")
- It performs better than the realistic alternatives available to the user, not the theoretical best alternative
- It is inside the jagged frontier for the specific tasks the product is designed to support

Performative AI — AI features that look impressive but generate limited real-world value — tends to surface where products optimize for demo moments rather than workflow integration, where AI handles tasks where users cannot evaluate output quality, and where the feature addresses a problem users did not identify as significant.

## Iteration Speed as a Product Advantage

One of Mollick's most practically important observations is that AI radically compresses iteration cycles in product and startup development. In his Vibefounding course, MBA students built functional startup prototypes in four days that surpassed semester-long traditional coursework. The mechanism: AI accelerated idea generation, content creation, and prototyping to the point where "finding the endpoint of a bad idea, which is most ideas, is an incredible way to uncover the good ones."

For product teams, this reframes iteration differently: AI-assisted teams can test more ideas, fail faster, and reach validated concepts in shorter cycles than before. Products that take advantage of this are not just using AI as a feature — they are reorganizing their development process around AI-enabled speed.

## On Designing AI Onboarding

Mollick's "four-level framework" for AI prompting ("Innovation Through Prompting," April 2024) has direct implications for how products should onboard users to AI features:

1. **Pre-made prompts**: The lowest barrier to entry — give users tested, specific prompts they can use immediately without needing to understand prompting. This is the equivalent of a starter template.
2. **Customization**: Allow users to modify and adapt prompts to their specific situations, building intuition about what works.
3. **Creation**: Enable advanced users to build their own prompting workflows.
4. **Autonomous agents**: The highest level, where AI systems self-direct based on high-level goals.

Most AI product onboarding pushes users too quickly to levels 2-4 without establishing the level-1 success that builds confidence and intuition. Mollick's observation: users who have not had early wins disengage. Pre-made prompts calibrated to the user's actual job tasks are not training wheels to remove — they are trust builders that make advanced use possible.

## The "Building a GPT" Analogy

On AI products that allow customization, Mollick noted in "Strategies for an Accelerating Future": "Building a GPT is more like providing instructions to a person than coding a machine." This framing has significant implications for product design — AI features that require configuration should be presented as giving instructions to a knowledgeable assistant, not as setting technical parameters. The mental model the product surfaces shapes how well users can operate it.
