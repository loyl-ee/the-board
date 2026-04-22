# Mattt Thompson — On Backend Engineering

## API Design as the Primary Backend Engineering Concern

Thompson's backend engineering philosophy centres on the API as the most important engineering decision. An API is a contract between the backend and its callers. Once published, that contract is permanent — breaking changes require versioning, coordination, and migration paths. The engineering discipline is getting the contract right before it is published, because changing it afterward is expensive.

The backend API design process he advocates: document the API before implementing it. Write the API reference — the endpoints, the parameters, the response schemas, the error codes — and have the API reviewed by the team that will consume it before writing a line of implementation. The documentation review is the API design review.

## HTTP Semantics: Use Them Correctly

Thompson has written extensively about correct HTTP semantics — the proper use of methods, status codes, headers, and caching directives. A backend that returns 200 for an error, that uses GET for state-changing operations, or that ignores cache control headers is a backend that is lying to its callers and to any infrastructure between them.

The backend engineering standard: every endpoint should return the correct HTTP status code for every response. A 404 for a missing resource, not a 200 with an error field. A 422 for validation failure, not a 400 for every client error. A 429 for rate limiting, with a `Retry-After` header. HTTP semantics are the shared vocabulary of the web — use them correctly.

## Documentation as Backend Infrastructure

Thompson treats API documentation not as a downstream deliverable but as backend infrastructure. The Alamofire and AFNetworking documentation are engineering artefacts maintained with the same discipline as the code. When an API changes, the documentation changes simultaneously. When a feature is added, it is documented before it is shipped.

The backend engineering discipline: documentation debt is technical debt. An undocumented API endpoint is an API that clients must explore by trial and error. The engineering cost of documentation is small compared to the engineering cost of callers who cannot use the API correctly.

## Protocol-Oriented Backend Design

Thompson's protocol-oriented approach extends to backend design: define the interfaces that your backend services must satisfy, and implement each service against those interfaces. A service that is defined by a protocol can be replaced without changing its callers, and can be mocked for testing without requiring a running service.

The backend engineering pattern: define a `UserStore` protocol rather than depending on a concrete `DatabaseUserStore`. Test with an `InMemoryUserStore` that satisfies the protocol. Deploy with the `DatabaseUserStore` implementation. When the database changes, only the implementation changes.

## Understanding Before Using Backend Frameworks

Thompson's NSHipster principle — "understand before using" — applies directly to backend frameworks. A developer who uses ActiveRecord without understanding SQL is a developer who will write inefficient queries and not know it. A developer who uses Redis without understanding its memory model will fill up the cache without knowing why.

The backend engineering discipline: before relying on a framework's abstraction for a performance-critical path, understand what the framework does at the level below. Read the query log. Understand the cache keys. Know what happens when the system is under load.

## Sources
- [NSHipster — nshipster.com](https://nshipster.com/)
- [Alamofire — GitHub](https://github.com/Alamofire/Alamofire)
- [Swift API Design Guidelines](https://swift.org/documentation/api-design-guidelines/)
- [HTTP RFC 9110 — IETF](https://www.rfc-editor.org/rfc/rfc9110)
