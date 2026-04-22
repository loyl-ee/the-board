# DHH — On Backend Engineering

## Rails: The Opinionated Backend

Hansson designed Ruby on Rails as an opinionated full-stack framework in which the backend architecture is predetermined by convention. The database schema, the routing layer, the model layer, the controller layer, and the mailer layer all follow conventions that every Rails developer knows. The engineering investment in learning the Rails conventions pays dividends across every Rails project.

The backend engineering argument for Rails: productivity comes from not making decisions that have already been made well. ActiveRecord's convention-based queries, the MVC structure, the asset pipeline, and the testing conventions are all decisions that 37signals made once and that Rails developers inherit. The energy that would have gone into those decisions is available for solving the actual business problem.

## The Database Is Not a Detail

Hansson's most important backend engineering position is that the relational database is the primary engineering artefact — not the application code. The database schema is the business model. The database constraints enforce the business rules. The database queries are the primary performance concern.

He has been critical of backend architectures that treat the database as a persistence layer behind an ORM that obscures SQL. ActiveRecord is designed to be transparent: when you need to understand what query is being executed, you look at the SQL, not at the ORM abstraction. Backend engineers who do not understand the SQL their ORM generates are not in control of their backend.

## REST and HTTP as the Backend API Standard

Hansson's backend API design philosophy follows REST conventions: resources are nouns, HTTP verbs express actions (GET for reads, POST for creates, PATCH/PUT for updates, DELETE for deletions), and responses use appropriate HTTP status codes. The API is the HTTP interface, not a JSON-over-HTTP RPC protocol.

Rails routing enforces this: `resources :articles` generates seven routes following REST conventions. Deviating from these conventions is possible but requires explicit decision, making non-RESTful design visible.

## Email as a First-Class Backend Concern

HEY's backend engineering demonstrates that email infrastructure is a significant engineering domain. Parsing, routing, storing, searching, and delivering email at scale requires backend engineering that most developers never encounter. Hansson has shared details of HEY's email architecture: custom IMAP integration, the "paper trail" routing system, and the feed aggregation.

The backend engineering lesson: email is more complex than it appears. SMTP, IMAP, DKIM, SPF, DMARC, and spam filtering are all backend engineering concerns for any application that sends or receives email.

## Background Jobs as Backend Architecture

37signals' applications make extensive use of background jobs for operations that should not block the HTTP request cycle: email delivery, image processing, report generation, and third-party API calls. Hansson's backend engineering discipline for background jobs: every job should be idempotent (safe to run more than once), should have a bounded execution time, and should fail visibly when it cannot complete.

The backend engineering standard: a background job that fails silently is worse than a background job that fails loudly, because silent failures accumulate undetected.

## Sources
- [The Ruby on Rails Doctrine](https://rubyonrails.org/doctrine)
- [HEY email architecture — various Signal v. Noise posts](https://signalvnoise.com/)
- [ActiveRecord querying — Rails documentation](https://guides.rubyonrails.org/active_record_querying.html)
- *Getting Real* — 37signals, 2006 (basecamp.com/gettingreal)
