# Simon Willison — On UX

## Documentation as UX

Willison's most distinctive UX position is that documentation is user experience. A tool's usability is not solely a property of the interface — it is a product of the interface plus its documentation. A confusing UI with excellent documentation is more usable than a polished UI with no explanation. He treats documentation as a first-class component of the product, not a supplement to it.

This manifests in his practice of writing annotated versions of his conference talks: after each public presentation, he publishes a full text version with extra notes, links, and context that the slides could not convey. The talk itself is an interface; the annotated transcript is the documentation that makes it fully usable.

## Discoverability

He cares deeply about discoverability — the ability of a user to figure out what a tool can do without external help. In CLI tools, this means comprehensive help text. In Datasette, this means the interface exposes its own capabilities through the API and through visible navigation. He has said that a good CLI tool should be explorable: a user who reads the help output should understand what the tool does and what options are available.

The LLM tool is built around this principle. Running `llm --help` gives a complete picture of its capabilities. Each subcommand has its own help. Plugin models appear in the model list automatically when installed. The tool does not hide its seams.

## The Importance of Good Error Messages

Error messages are UX. Willison does not treat them as afterthoughts. A tool that fails silently or with cryptic messages is harder to use than a tool that fails loudly with an explanation of what went wrong and, where possible, how to fix it. He has discussed this in the context of both Datasette and LLM — when something goes wrong with an API call, the error should tell the user what the API said, not just that something failed.

## UX Decisions in the LLM Tool

The LLM command-line tool makes several explicit UX decisions worth noting:

**Streaming by default.** When you run a prompt, the response streams to the terminal in real time rather than appearing all at once. This makes long responses feel responsive and allows the user to interrupt if the output is going in the wrong direction.

**Conversation history.** The tool logs every prompt and response to a SQLite database by default, making every past conversation searchable and reviewable. This is a UX decision driven by his data journalism instincts: logged information is queryable information.

**Plugin discoverability.** Models available through plugins appear in the same model list as built-in models. Users do not need to know whether a model is native or plugin-backed — it simply appears in the list.

**Unix composability.** The tool is designed to be used in pipelines: `cat file.txt | llm "summarize this"` works as expected. This is a developer UX decision that makes the tool composable with the user's existing toolchain.

## Documentation as Self-Sufficient UX

His TIL (Today I Learned) posts often serve as the entire user onboarding for a technique or tool. A TIL about how to use a particular sqlite-utils feature, for example, is written to be self-contained — a reader should be able to follow it without prior context. He writes for "future me" explicitly: the TIL is the documentation he wishes had existed when he first encountered the problem.

## Gaps

Willison's UX thinking is heavily weighted toward developer tools and CLI interfaces. He has less documented experience with consumer-facing UX, onboarding flows, or mobile interfaces. For products targeting non-technical users, his instincts will be useful for principles (clarity, discoverability, documentation) but less directly applicable to the specific design challenges of consumer products.
