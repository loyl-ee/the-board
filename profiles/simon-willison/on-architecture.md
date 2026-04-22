# Simon Willison — On Architecture

## The Baked Data Architecture

Willison's most original architectural contribution is the "baked data" pattern: instead of a live database and application server, pre-compute the data into a static SQLite file and deploy it alongside a read-only server. The SQLite file is "baked" from the source data, committed to the repository or uploaded to object storage, and served from any static hosting platform.

The architectural advantages are significant: no live database to maintain, no connection pool to manage, no database migrations to run, and sub-millisecond query performance for most analytical queries against large datasets. The limitation is obvious: baked data is read-only. For applications where queries far outnumber writes, this is often the correct trade-off.

## SQLite as the Correct Default Database

Willison's architectural default is SQLite. For the vast majority of web applications — particularly tools, APIs, and content sites — SQLite provides sufficient performance, zero operational overhead, and the full capability of a relational database. The common objection (SQLite doesn't support concurrent writes) is less significant than it appears: most web applications have far more reads than writes, and SQLite's write lock is typically held for milliseconds.

The architectural discipline: choose SQLite unless you have a specific requirement that SQLite cannot meet. The first such requirement is usually concurrent writes at high scale — which most applications never encounter. Migrating from SQLite to Postgres when that requirement appears is less painful than operating Postgres when SQLite would have been sufficient.

## Plugin Architecture for Ecosystem Growth

Both Datasette and the LLM CLI use plugin architectures that allow third-party developers to extend the tool without modifying core. The architectural design of the plugin API is the most important engineering decision in a plugin-based system: it determines what capabilities can be added, how stable the API is across versions, and how easy it is to write a plugin.

Willison delayed Datasette 1.0 for years to stabilise the plugin API. The principle: a plugin API is a public contract. Breaking changes to the plugin API are breaking changes to every plugin. Design it for longevity.

## Small, Composable CLI Tools

Willison's tool portfolio follows the Unix philosophy: small tools that do one thing and compose with other tools. The LLM CLI, shot-scraper, sqlite-utils, and Datasette are each focused on a specific capability. They compose: `llm prompt "summarise this" < data.txt | sqlite-utils insert results.db results -` is a valid pipeline.

The architectural principle: if your tool can be used in a pipeline, it is composable. If it requires a GUI or a specific workflow to be useful, it is not. Composable tools multiply their value through combination.

## Documentation-Driven API Design

Willison's API design process begins with documentation: what will the command-line invocation look like? What will the Python API look like? The implementation follows from the documentation, not the other way around. If the documentation is awkward, the API is awkward, and the API should be redesigned.

The architectural discipline: write the API documentation before writing the implementation. Use the act of documentation to discover design problems that would be invisible in code.

## Sources
- [Datasette architecture — docs.datasette.io](https://docs.datasette.io/)
- ["The baked data architectural pattern" — simonwillison.net](https://simonwillison.net/2021/Jul/28/baked-data/)
- [LLM CLI — llm.datasette.io](https://llm.datasette.io/)
- [sqlite-utils — sqlite-utils.datasette.io](https://sqlite-utils.datasette.io/)
