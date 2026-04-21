# Ethan Mollick — On UX and Prompting

## Prompting as a Practical Skill, Not an Art Form

Mollick's most sustained contribution to AI UX is his work on prompting — not as a technical discipline requiring special expertise, but as a practical skill that most people overcomplicate. His 2023 essay "A Guide to Prompting AI (for what it is worth)" opens by debunking the "prompt influencer" phenomenon: the claim that there are secret prompts, magic formulas, and esoteric techniques that unlock AI's true power. His conclusion: "There are no secret prompts."

What matters instead is much more mundane:

- **Context and constraints**: Providing the AI with relevant background, intended audience, format requirements, and purpose shapes output more reliably than prompt engineering techniques.
- **Iterative dialogue**: Treating prompting as a conversation — request, evaluate, refine — outperforms attempts to craft one perfect prompt. "Just use it and see where that takes you."
- **Role definition**: Telling the AI what kind of entity to be ("act as a senior product manager") shifts outputs meaningfully, because it changes the statistical space of likely responses.
- **Examples**: Showing the AI the kind of output you want, rather than describing it, is often more efficient.
- **Step-by-step instructions**: Breaking complex tasks into explicit steps, especially for analytical or reasoning tasks, improves accuracy. This is the technique Mollick identifies as most reliably useful.

His position on prompt engineering as a long-term skill: "Being 'good at prompting' is a temporary state of affairs." As models improve, they require less engineered input. The practical skill is not prompt engineering — it is learning to communicate clearly with an unusual kind of interlocutor.

## The "Good Enough Prompting" Framework

In "Getting Started with AI: Good Enough Prompting" (November 2024), Mollick updated his guidance to reflect models that had become substantially more capable. His key shift: he no longer recommends thinking of AI as an intern. The new framing is "an infinitely patient new coworker who forgets everything" after each conversation.

The Good Enough framework has two modes:

**Task prompting**: When you need a specific output. Be explicit about what you want and for whom. Provide documents, context, and examples. Use the AI's capacity for quantity — ask for 30 ideas rather than 5 and select the best — to exploit AI's speed advantage. Maintain dialogue; do not expect a single prompt to produce a finished output.

**Thinking prompting**: Using AI as a thinking partner through natural dialogue, often by voice. The AI functions as what Mollick calls a "rubber duck" — a sounding board that helps you articulate and clarify your thinking. In this mode, the AI does not need to produce great outputs; it needs to produce useful responses to thinking-out-loud.

The division is practically important for product design: different AI use cases require different interaction patterns, and presenting them identically in a product interface is a UX error.

## What Actually Helps Users Get Better

Mollick's answer to this is consistently: use it more, on real work you care about, and develop intuitions you could not get from reading about AI. The ten-hour threshold is his operationalization of this. He is explicit that no amount of reading guides, watching tutorials, or attending workshops substitutes for accumulating genuine usage.

This has UX implications. Products that front-load tutorials before first use, or that require users to complete onboarding flows before doing real work, are working against this principle. Mollick's research and teaching suggest that the fastest path to user competence is immediate exposure to real tasks, with enough structural support (pre-made prompts, role definitions, examples) to prevent early failures that cause abandonment.

## The Persona / Role Technique

One technique Mollick endorses consistently is giving AI a specific persona or role before beginning a task. This is not about the AI "believing" it is a different entity — it is about shifting the statistical context of responses toward a more relevant domain. "Act as an experienced product manager who has shipped 10 consumer apps" will elicit different outputs than no role specification, not because AI has a manager persona, but because the training data associated with that description pulls responses in a different direction.

Mollick describes this in "On-Boarding Your AI Intern" (May 2023): "Several billion people just got free interns. They are weird, somewhat alien interns that work infinitely fast." The intern framing was his initial practical heuristic for helping new users calibrate expectations — not as capable as an expert, willing to do anything you ask, prone to making things up confidently, needs supervision.

## Consistency and Reliability in AI Outputs

A persistent UX challenge Mollick acknowledges: AI outputs are probabilistic, not deterministic. The same prompt on the same model will produce different outputs on different runs. This makes it harder to build reliable workflows and harder for users to develop stable intuitions. His practical guidance: use the AI's stochasticity as a feature rather than a bug by generating multiple outputs and selecting the best, rather than running a prompt once and accepting whatever comes back.

## On AI That Confuses Rather Than Helps

Mollick's research on doctors who gained no benefit from AI diagnosis tools despite AI's diagnostic capability points to a broader pattern: AI that is capable in principle but useless in practice because the interaction design does not bridge the user's expertise and expectations to the model's capabilities. The product failure was not the AI; it was the interface that put capable AI in front of users without giving them the scaffolding to use it.

He notes two root causes: algorithmic aversion (users distrust machine recommendations and override them even when correct) and difficulty understanding how to effectively use LLMs (users treat them like search engines or expecting polished first-draft outputs). Both are addressable through interaction design — not through better AI.
