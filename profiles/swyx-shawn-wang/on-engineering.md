# Swyx / Shawn Wang — On Engineering

## The AI Engineer Discipline

Swyx coined the term "AI Engineer" to describe a distinct engineering role that sits between traditional software engineering and ML research. The AI Engineer does not train models — they build products and systems using models as components. The engineering stack is different: embeddings, vector databases, retrieval-augmented generation, prompt management, and model evaluation replace (or sit alongside) traditional backend concerns.

The engineering discipline he has articulated: AI Engineers must understand the properties of the components they are working with — context windows, hallucination rates, latency characteristics, cost curves — in the same way that backend engineers understand database query plans and cache invalidation. Treating an LLM as a black box is not AI engineering; it is API consumption.

## Defensive AI Engineering: Not Just a Wrapper

Swyx has been consistently critical of products that simply wrap a foundation model API with minimal additional engineering. His argument: API wrappers have no moat — they are instantly replicable when the underlying model improves or a competitor launches. Defensible AI engineering means building proprietary data pipelines, fine-tuned models, evaluation infrastructure, or workflow integrations that cannot be replicated by switching API providers.

The engineering investment that creates defensibility: proprietary training data, domain-specific fine-tuning, multi-model orchestration, or deep integrations with existing systems. Any of these requires genuine engineering, not just prompt design.

## The AI Product Stack

Swyx's map of the AI engineering stack is a practical framework for engineering decisions. The layers: data ingestion and processing, embedding and retrieval, prompt management and orchestration, model serving and inference, evaluation and monitoring. Each layer has specific engineering concerns and emerging tooling standards.

The engineering discipline: make explicit architectural decisions at each layer rather than defaulting to whatever a framework provides. Understand the trade-offs in your retrieval strategy (semantic vs. keyword vs. hybrid), your chunking strategy for RAG, and your evaluation methodology before committing to them in production.

## LLM Ops and Observability

Swyx has emphasised that AI systems require the same operational discipline as traditional software: logging, monitoring, alerting, and incident response. The specific requirements for LLMs include prompt and response logging (for debugging), cost tracking (queries to foundation models are expensive at scale), latency monitoring, and model performance evaluation over time.

The engineering standard: before deploying an LLM-powered feature to production, have a plan for observing it. What does a degraded response look like? How will you detect it? What is the incident response path?

## Learn in Public as an Engineering Practice

Swyx's "Learn in Public" philosophy (from his 2018 essay) is directly applicable to engineering: share what you are building before it is finished, document your learning in real time, and treat external feedback as engineering research. The engineers who learn in public build larger networks, get earlier feedback on their architectural decisions, and contribute to the field's collective knowledge.

For AI engineering specifically: the field is moving faster than any individual can track. Engineers who share what they are trying and what they are learning are better positioned to absorb new capabilities quickly than those who work in private.

## Sources
- [swyx.io — Shawn Wang's writing](https://www.swyx.io/)
- ["The Rise of the AI Engineer" — swyx.io, 2023](https://www.swyx.io/ai-engineer)
- [Latent Space podcast](https://www.latent.space/)
- ["Learn in Public" — swyx.io, 2018](https://www.swyx.io/learn-in-public)
- [AI Engineer World's Fair](https://www.ai.engineer/)
