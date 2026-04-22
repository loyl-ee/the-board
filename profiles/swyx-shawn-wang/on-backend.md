# Swyx / Shawn Wang — On Backend Engineering

## The AI Backend Stack

Swyx has documented the emerging backend architecture for AI-powered products. The components: a vector database for semantic search and retrieval (Pinecone, Weaviate, pgvector in Postgres), an embedding model (OpenAI text-embedding-ada-002, or open-source alternatives) for converting text to searchable vectors, an LLM API for generation (OpenAI, Anthropic, open-source via Ollama), and an orchestration layer (LangChain, LlamaIndex, or custom) for connecting them.

The backend engineering discipline: understand what each component does and why it is in the stack. Vector databases are not just "faster text search" — they enable semantic similarity search that keyword search cannot. The choice of embedding model determines the quality of your semantic search. The orchestration layer determines how flexible your pipeline is when models or tools change.

## Embeddings and Vector Search Backend Engineering

The engineering of a retrieval-augmented generation (RAG) system starts with the embedding pipeline: documents are chunked, each chunk is embedded (converted to a vector by an embedding model), and the vectors are stored in a vector database. At query time, the user's query is embedded and the most semantically similar document chunks are retrieved.

The backend engineering decisions in this pipeline are numerous: chunk size (too small loses context, too large dilutes relevance), chunk overlap (prevents answers from being split across chunks), embedding model choice (accuracy vs. cost vs. speed), and retrieval strategy (top-k by cosine similarity, or hybrid with keyword search).

## LLM API Backend Engineering

Backend applications that call LLM APIs must handle a set of engineering concerns that traditional API calls do not have: streaming responses (LLMs generate token by token, and users should see output immediately), token budget management (prompts that exceed the context window fail), rate limiting (LLM APIs have strict rate limits per minute and per day), and cost management (LLM API calls have significant variable costs).

The backend engineering standard: every LLM API call should be logged with prompt length, response length, model used, and cost. Cost management without visibility is impossible.

## LLM Ops: Observability for AI Backends

Swyx has emphasised that AI backends require the same observability discipline as traditional backends, plus additional AI-specific concerns: prompt and response logging, latency histograms (LLM responses are much slower and more variable than database queries), model performance tracking over time, and cost per request tracking.

The backend engineering standard: before deploying an LLM-powered backend feature to production, implement logging for every LLM call. What was the prompt? What was the response? How long did it take? What did it cost? Without this data, debugging production issues is guesswork.

## Evaluation Infrastructure as Backend Engineering

Swyx has argued that AI backend quality cannot be evaluated with traditional unit tests alone. You need an evaluation framework: a dataset of representative inputs, a set of quality criteria (correctness, relevance, tone), and automated evaluation that runs on every change to the prompt, the retrieval pipeline, or the model.

The backend engineering standard: build the evaluation infrastructure before building the backend feature. Define what good looks like for your specific use case. Implement automated evaluation that can be run in CI. Treat evaluation regressions as build failures.

## Sources
- [swyx.io — Shawn Wang's writing](https://www.swyx.io/)
- ["The Rise of the AI Engineer" — swyx.io, 2023](https://www.swyx.io/ai-engineer)
- [Latent Space podcast — AI backend architecture episodes](https://www.latent.space/)
- [AI Engineer World's Fair — backend engineering talks](https://www.ai.engineer/)
