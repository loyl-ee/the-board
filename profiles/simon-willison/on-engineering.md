# Simon Willison — On Engineering

## The Perfect Commit

Willison defines the "perfect commit" as the principal unit of engineering craft. A perfect commit bundles four things together: the implementation, the tests, the documentation update, and a link to the relevant issue thread. Nothing else counts as done. A commit that ships code without tests is deferred debugging. A commit that ships code without documentation is deferred explanation. A commit that has no issue link is a change without context.

He writes: "The commit is our principal unit of work. It deserves to be treated thoughtfully and with care." This is not bureaucratic overhead — it is the discipline that keeps a codebase legible to its future maintainers, including your future self.

## Documentation-First Development

Willison treats documentation as concurrent with code, not downstream of it. Writing about a feature before and during implementation clarifies what you are actually building. He uses GitHub issues as development diaries: long threads where architectural decisions are argued, alternatives are considered, and trade-offs are recorded. These threads are the primary design documents. The code is the outcome.

This practice has a secondary benefit: public GitHub issues generate external signal before a feature ships. Contributors find bugs, suggest improvements, and describe their actual use cases. He learns faster about whether he is solving the right problem than private development would allow.

## SQLite as the Right Default

Willison's database philosophy is anchored in SQLite: use it unless you have a specific reason not to. For most web applications, SQLite provides sufficient performance, zero infrastructure overhead, and the full power of SQL. His Datasette project is built on SQLite and has demonstrated that it scales to hundreds of millions of rows for analytical workloads. The "baked data" pattern — static SQLite files deployed alongside a read-only server — eliminates the operational complexity of a running database entirely.

The engineering argument: developers consistently underestimate SQLite's capabilities and overestimate the point at which they need Postgres. Starting with SQLite and migrating if necessary is almost always the right order.

## Never Commit Code You Cannot Explain

Willison's golden rule for AI-assisted engineering: he will not commit any code — regardless of whether an LLM wrote it — that he could not explain to a colleague. This principle guards against a specific failure mode of LLM-generated code: it often looks correct and passes surface inspection while containing subtle bugs that the author, having not written it, cannot reason about.

The standard is not that you write every line — it is that you understand every line. If a generated function does something you cannot explain, you read it until you can, or you rewrite it.

## The Shot-Scraper Pattern: Build and Release Incrementally

Willison's approach to tool development is the "shot-scraper pattern": identify a sharp personal pain, build the minimal tool that addresses it, release it publicly, document it thoroughly, then observe whether others have the same pain. If they do, the tool gains traction. If not, he has still solved his problem.

This produces a portfolio of small, focused tools rather than large platforms. Each tool does one thing and does it well. The plugin architecture in Datasette and LLM allows the ecosystem to grow beyond what he maintains, without requiring his approval for every extension.

## Prompt Injection as an Engineering Constraint

Willison named and popularised the concept of "prompt injection" — attacks where malicious content in data processed by an LLM hijacks the model's instructions. He treats this as a fundamental security constraint for any application that processes untrusted content with an LLM. The engineering discipline: never route untrusted content through a model that has privileged access to tools, systems, or APIs. Treat LLM outputs as untrusted user input.

## Sources
- [simonwillison.net](https://simonwillison.net/)
- ["The Perfect Commit" — simonwillison.net](https://simonwillison.net/2022/Oct/29/the-perfect-commit/)
- [Datasette](https://datasette.io/)
- [LLM CLI tool — GitHub](https://github.com/simonw/llm)
- ["Prompt injection attacks against GPT-3" — simonwillison.net, 2022](https://simonwillison.net/2022/Sep/12/prompt-injection/)
