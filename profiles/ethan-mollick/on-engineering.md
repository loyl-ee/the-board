# Ethan Mollick — On Engineering

## The Jagged Frontier as an Engineering Mental Model

Mollick's most useful contribution to engineering practice is the "jagged frontier" concept: AI systems are simultaneously superhuman at some tasks and surprisingly bad at adjacent tasks, with the boundary between these zones being non-obvious and irregular. The engineering implication is that you cannot assume an AI component will succeed or fail in a principled way — you must evaluate it empirically on your specific task.

For engineering teams integrating LLMs: do not extrapolate from a model's performance on one task to its performance on a similar-looking task. Benchmark your specific use case. The jagged frontier means that a model that writes excellent prose may struggle with a specific code generation task, or vice versa, in ways that cannot be predicted from general capability assessments.

## Human-in-the-Loop System Design

Mollick's research consistently supports human-AI collaboration over full automation. The engineering argument: for most knowledge work tasks, a human reviewing AI output produces better results than AI alone and is faster than a human alone. The engineering discipline is designing workflows where the human review step is integrated naturally — not as an awkward checkpoint but as the primary interface.

System design principle: place the human where they add the most value. In code generation, that is often review and specification, not line-by-line writing. In content generation, that is curation and fact-checking, not grammar correction.

## LLMs as Engineering Assistants, Not Oracles

Mollick is careful to frame AI tools as assistants — systems that augment human judgment rather than replace it. The engineering implementation of this framing: outputs should be presented as drafts or suggestions, with clear affordances for the human to edit, reject, or modify. UI that presents AI output as a fait accompli creates over-reliance; UI that presents it as a starting point creates appropriate collaboration.

For engineering teams: instrument your AI-assisted workflows to measure how often humans change AI suggestions. High acceptance rates may indicate the AI is doing well — or that users are not reviewing critically. The two look identical from the outside.

## Prompt Engineering as a Legitimate Engineering Discipline

Mollick treats prompt engineering seriously as a skill that transfers across models and tasks. His research and teaching at Wharton include systematic approaches to prompt design: specifying role, context, task, and constraints; using few-shot examples for complex tasks; iterating on prompts empirically rather than assuming first drafts are optimal.

The engineering standard: a prompt in production should be versioned, tested against a benchmark dataset, and reviewed when the model changes. Prompts are code.

## Evaluating AI Capabilities for Engineering Decisions

Mollick's approach to deciding whether to use AI for a task is empirical: try it, measure the output quality, compare to the alternative. He has developed frameworks for this evaluation that engineering teams can apply: define the quality criteria before testing, test a representative sample of inputs, and measure the actual improvement (time, quality, cost) against baseline.

The engineering discipline: before committing to an AI-assisted architecture, run a controlled experiment on your specific data and task. General benchmark results are not sufficient evidence for a production engineering decision.

## Sources
- *Co-Intelligence: Living and Working with AI* — Ethan Mollick, 2024
- [One Useful Thing — Mollick's Substack](https://www.oneusefulthing.org/)
- ["Centaurs and Cyborgs on the Jagged Frontier" — Mollick et al., 2023](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4573321)
- [Ethan Mollick — Wharton School faculty](https://mgmt.wharton.upenn.edu/profile/emollick/)
