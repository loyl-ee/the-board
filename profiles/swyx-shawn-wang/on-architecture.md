# Swyx / Shawn Wang — On Architecture

## The AI Product Architecture Stack

Swyx has mapped the emerging AI product architecture into explicit layers: data ingestion and processing, embedding and retrieval, prompt management and orchestration, model serving and inference, evaluation and monitoring. Each layer has specific engineering concerns, emerging tooling standards, and failure modes.

The architectural discipline: make conscious decisions at each layer rather than accepting the defaults a framework provides. Your retrieval strategy (semantic search, keyword search, hybrid) is an architectural decision with trade-offs. Your chunking strategy for RAG is an architectural decision. Your evaluation methodology is an architectural decision. Treat them as such.

## RAG Architecture: Retrieval-Augmented Generation

Swyx has documented the architecture of RAG systems in detail. The pattern: a user query triggers a retrieval step that finds relevant documents from a vector database, those documents are included in the context sent to the LLM, and the LLM generates a response grounded in the retrieved documents. The architecture has specific failure modes: retrieval can fail (wrong documents retrieved), context can be too large (relevant documents compete with irrelevant ones), and grounding can be lost (the LLM ignores retrieved context).

The architectural discipline for RAG: design and evaluate the retrieval step independently from the generation step. A RAG system where the retrieval is failing will not benefit from a better generation model.

## Defensible AI Architecture: Beyond the Wrapper

Swyx's central architectural argument is that "wrapper apps" — products that simply call a foundation model API with a system prompt — are architecturally fragile. They have no moat: a competitor can replicate the wrapper in a day. Defensible AI architecture requires something that cannot be replicated by changing an API call.

The architectural investments that create defensibility: proprietary training data (collected and curated by the product, not available to competitors), fine-tuned models (behaviour specific to the product domain), deep system integrations (the product is embedded in existing workflows), and proprietary evaluation infrastructure (knowing what good looks like for your specific use case).

## Multi-Model Orchestration

Swyx has documented architectures that use multiple models for different parts of a workflow: a small, fast model for classification or routing, a large model for complex reasoning, a specialised model for specific domains. The orchestration layer decides which model to call for which task.

The architectural advantage: matching model capability to task complexity reduces cost and latency without sacrificing quality on the tasks that require it. The architectural discipline: define the performance requirements for each task type, evaluate models against those requirements, and choose the smallest model that meets the requirement.

## Evaluation Infrastructure as a First-Class Architectural Concern

Swyx is emphatic that AI systems require evaluation infrastructure before they can be safely developed and deployed. Without the ability to measure whether a change to a prompt, a model, or a retrieval strategy improves or degrades system quality, development is blind.

The architectural investment: build the evaluation suite before building the product. Define what good responses look like for your specific use case. Build a dataset of test cases. Implement automated evaluation that can be run on every change. This is the architectural prerequisite for iterating on AI systems responsibly.

## Sources
- [swyx.io — Shawn Wang's writing](https://www.swyx.io/)
- ["The Rise of the AI Engineer" — swyx.io, 2023](https://www.swyx.io/ai-engineer)
- [Latent Space podcast — AI architecture episodes](https://www.latent.space/)
- [AI Engineer World's Fair — architecture talks](https://www.ai.engineer/)
