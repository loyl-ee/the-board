# Simon Willison — On Product

## Build the Tool You Need

Willison's product philosophy begins with the simplest possible motivation: he builds things he personally needs. Datasette began as a tool he wanted to have existed years earlier at The Guardian. Shot-scraper was built to keep documentation screenshots up to date. LLM was built because he wanted a unified command-line interface for all the different model APIs he was using. sqlite-utils grew from repeated pain manipulating SQLite databases for data journalism.

This "scratch your own itch" pattern is not accidental. It is a deliberate strategy. He argues that building for your own need gives you the best possible user research — you are the user. You know when something is too slow, too confusing, or missing a feature because you feel it directly. The risk is building something only you need; the mitigation is the JSK fellowship insight: data journalists face the same problems he faces, at scale.

## Documentation-First Development

Documentation is not downstream of product for Willison — it is concurrent with it. His "perfect commit" concept makes this structural: every commit includes the implementation, tests, updated documentation, and a link to the issue thread. Documentation is not what you do when you are done building; it is how you know what you are building.

This extends to how he thinks about product specification. He often writes about a feature or approach before implementing it, using the act of writing to clarify what he actually wants to build. He has described GitHub issues as development diaries — long threads where he thinks through architectural decisions, records what he tried, and explains why he made tradeoffs. These threads are not bureaucratic overhead; they are the primary design documents.

## The Shot-Scraper Approach: Solve Your Own Problem, Then Open Source It

A recurring pattern in his portfolio is what might be called the "shot-scraper pattern": identify a sharp personal pain, build the minimal tool that addresses it, release it publicly, document it thoroughly, then watch whether others have the same pain. If they do, the tool gains adoption. If they do not, he has still solved his problem and written something useful.

This is a low-waste approach to product development. The tool is valuable to him regardless of external adoption. External adoption is upside, not the precondition. This means he does not over-engineer for hypothetical users — he builds for the user he knows, which is himself, and trusts that overlap with others will be discovered through usage.

## Iterating in Public

Willison develops in the open — releasing early, releasing often, and narrating the development process. His Substack newsletter, blog posts, and GitHub issues provide a continuous stream of development updates. He does not wait for polish. He ships prototypes, describes their limitations, and invites feedback.

This has a product benefit that is easy to understate: public iteration generates external signal before the product is finished. People find bugs, suggest features, and describe their actual use cases. He learns faster about whether the tool is solving the right problem than he would through private development.

## The Plugin Architecture as Product Philosophy

Both Datasette and LLM use plugin architectures that allow external developers to extend the tool without modifying core. This is a product decision as much as a technical one. He has said that "designing plugin hooks forces me to think extremely hard about design" — the process of defining what should be extensible clarifies what the core product actually is. He delayed Datasette 1.0 for years specifically to ensure the plugin API was stable enough that external developers could build on it without being broken by changes.

Plugins also serve as product experiments. When he was skeptical about GraphQL, he built a GraphQL plugin for Datasette rather than adding it to core — letting him explore the idea without committing to it. This is a pattern of risk-managed exploration: new ideas live in plugins until their value is proven.

## AI-Assisted Product Development

Since 2022, Willison has integrated LLMs deeply into his product development process. His simonw/tools GitHub repository contains dozens of single-file HTML+JavaScript applications, every one of which was built through LLM prompting. He adds new prototypes at a rate of several per week. He has described this explicitly as changing his product ambitions: "This doesn't just make me more productive: it lowers my bar for when a project is worth investing time in at all. In the past I've had plenty of ideas for projects which I've ruled out because they would take a day—or days—of work to get to a point where they're useful. But if ChatGPT can drop that down to an hour or less, those projects can suddenly become viable."

The key product implication: AI tools make the viable idea space larger. Projects that previously required too much investment to justify now become worth building. This is not primarily about speed of execution — it is about the expansion of the set of things worth attempting.

## What He Avoids

Willison does not build for growth metrics. He does not A/B test, does not optimize for engagement, and does not describe his work in terms of funnels or conversion rates. His product language is entirely about capability: what can a user do with this tool that they could not do before? He is skeptical of product thinking that prioritizes retention over genuine utility. His tools are useful or they are not; if they are useful, people come back.
