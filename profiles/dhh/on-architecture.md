# DHH — On Architecture

## Monolith First, Always

Hansson's architectural position is unambiguous: start with a monolith. The "majestic monolith" — a single deployable unit containing all the application's functionality — is not a technical debt to be paid off by eventual extraction into microservices. For most applications, it is the correct permanent architecture.

His argument: microservices solve problems of scale and team organisation that most applications never encounter. The distributed systems complexity introduced by microservices — network calls between services, distributed transactions, eventual consistency, service discovery, deployment coordination — is real and significant. It should only be accepted when the alternative (a monolith that has grown unwieldy) is demonstrably worse. "Extract services when you feel the pain, not in anticipation of it."

Basecamp 3 is a monolith serving millions of users on a small team. That is the proof of concept.

## The Database as the Backbone

Hansson's architectural philosophy centres on the relational database as the primary source of truth and the primary expression of business logic. The schema is the architecture. Migrations are the version history of the architecture. Constraints, foreign keys, and indices are not implementation details — they are the system's guarantees encoded in the database.

He is resistant to architectural patterns that treat the database as a detail — event sourcing, CQRS, and similar patterns that push business logic into application code and use the database only for persistence. For most applications, the simpler model (database as truth, application as logic) is more correct and more maintainable.

## Convention-Driven Architecture

Rails' "convention over configuration" is an architectural principle as much as a framework feature. The architecture of a Rails application is defined by Rails conventions: `app/models`, `app/controllers`, `app/views`, database tables named for models, routes defined by resource names. Any Rails developer can orient in any Rails codebase because the architecture is predetermined.

The architectural lesson: choose conventions and enforce them consistently, even when a specific case might be better served by deviation. The consistency of a conventional architecture is worth more than the local optimisation of deviating from it.

## Vertical Scaling Over Horizontal Scaling

Hansson has argued consistently for vertical scaling (bigger servers) over horizontal scaling (more servers) for most applications. Modern servers are extremely powerful. A single server with 64 cores and 512GB of RAM handles more concurrent requests than most applications will ever need. The complexity of horizontal scaling — load balancers, distributed caches, session affinity — is only justified when vertical scaling is genuinely insufficient.

37signals runs on a small number of powerful servers. The Basecamp monolith does not need a Kubernetes cluster.

## The Shape Up Architecture of Work

Hansson's "Shape Up" methodology (how 37signals plans and executes engineering work) has architectural implications: features are designed in "six-week cycles" with a clear "appetite" (how much time the feature is worth) rather than estimates (how long the feature will take). The architecture of the work matches the architecture of the product: bounded, opinionated, with explicit trade-offs rather than open-ended requirements.

## Sources
- [The Majestic Monolith — Signal v. Noise](https://signalvnoise.com/svn3/the-majestic-monolith/)
- [The Ruby on Rails Doctrine](https://rubyonrails.org/doctrine)
- *Shape Up* — 37signals, 2019 (basecamp.com/shapeup)
- [37signals on infrastructure — various blog posts](https://signalvnoise.com/)
