# Simon Willison — On Backend Engineering

## SQLite as the Right Default Backend Database

Willison's backend database philosophy begins with SQLite. For the majority of web applications, APIs, and data tools, SQLite is sufficient: it handles thousands of concurrent reads, supports the full SQL standard, requires no separate process, and produces a single file that can be backed up with `cp`. The engineering overhead of operating a Postgres cluster — backups, updates, connection pooling, monitoring — is non-trivial and often unjustified for applications below a significant scale.

His rule: start with SQLite and migrate to Postgres when SQLite genuinely cannot meet your requirements. The first such requirement is usually concurrent writes from multiple processes — which most applications never encounter.

## The Baked Data Backend Pattern

Willison's "baked data" pattern inverts the traditional backend architecture: instead of a live database queried by a server, pre-compute the query results into a static SQLite file and deploy it to object storage or a static host. The backend becomes a file and a CDN. Read performance is excellent (cached bytes), write performance is irrelevant (the database is read-only), and operational complexity is minimal.

The backend engineering use case: any API or application where queries far outnumber writes, and where the data can be updated on a schedule rather than in real time. Data journalism tools, public datasets, reference APIs.

## REST APIs as the Default Backend Interface

Willison's backend API design follows REST conventions: resources are addressable by URL, HTTP verbs express semantics, and responses use standard HTTP status codes and content types. He is sceptical of GraphQL as a default: it introduces a query language, a schema, and a resolution layer that are justified only when clients have genuinely heterogeneous data requirements.

The backend API engineering discipline: design the simplest API that satisfies the client's actual requirements. REST with well-designed URLs and clear semantics is simpler than GraphQL for most use cases.

## The Perfect Commit in Backend Engineering

Willison's "perfect commit" standard applies directly to backend engineering: a backend change is not complete until it includes the implementation, the tests (which test against a real database, not a mock), updated documentation (API docs, migration notes), and a link to the relevant issue thread.

The backend engineering standard: backend tests must test against a real database engine, not a mock. The differences between SQLite, Postgres, and MySQL in edge case behaviour are significant enough that tests against mocks give false confidence.

## Datasette as a Backend Engineering Pattern

Datasette — Willison's tool for exploring and publishing SQLite databases — is itself a backend engineering pattern: a Python application that wraps a SQLite database with an HTTP API, a browsable HTML interface, and a plugin system. The backend engineering decisions in Datasette are: HTTP caching headers for every response, async Python for concurrent request handling, and a plugin API that exposes the full request/response cycle for extension.

The backend engineering lesson: every API you build should have a browsable HTML interface, even if that interface is minimal. A browsable API is debuggable by humans. A JSON-only API requires a tool to explore.

## Sources
- [Datasette documentation — docs.datasette.io](https://docs.datasette.io/)
- ["The baked data architectural pattern" — simonwillison.net](https://simonwillison.net/2021/Jul/28/baked-data/)
- [sqlite-utils — sqlite-utils.datasette.io](https://sqlite-utils.datasette.io/)
- ["The Perfect Commit" — simonwillison.net](https://simonwillison.net/2022/Oct/29/the-perfect-commit/)
