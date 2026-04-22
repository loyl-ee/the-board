# Pieter Levels — On Backend Engineering

## One Server, Multiple Products

Levels' backend engineering is radically simple by the standards of contemporary infrastructure: multiple products running on a single Linode VPS. No Kubernetes, no Docker Swarm, no managed container orchestration. One server, SSH access, and a cron job scheduler.

The engineering argument: a server you can SSH into and understand completely is a server you can debug at 2am. A Kubernetes cluster is not debuggable at 2am by one person without a dedicated DevOps team. The engineering overhead of container orchestration is only justified at a scale that most indie products never reach.

## PHP as the Right Tool for Solo Backends

Levels uses PHP for his backends. He has never apologised for this. PHP is mature, widely hosted, fast enough for his use cases, and — critically — immediately deployable. A PHP file on a server is served by Apache or Nginx without a build step, a daemon, or a process manager. It starts when a request arrives and exits when the request is done.

The engineering argument for PHP (or any well-understood language over a fashionable one): a language you have used for years is a language you can debug efficiently. The engineering cost of switching to a fashionable language includes the time to develop the intuitions that make debugging fast.

## Postgres and Redis: The Minimal Backend Stack

Where Levels uses a database server (rather than flat files for very early MVPs), he uses Postgres for relational data and Redis for caching, session storage, and rate limiting. This is not a complex stack — it is the minimum necessary for a production web application that handles user accounts, payments, and real-time data.

The backend engineering discipline: resist adding stack components until they are genuinely required. Each component is an operational liability. The question before adding a message queue, a search engine, or a graph database is: can the existing stack solve this problem, even if not optimally?

## Flat Files as MVPs

Levels has described using JSON files stored on the filesystem as the initial "database" for new products. A JSON file can be written by a cron job, read by the application, and replaced atomically. For a product that has not yet validated its data model, a flat file is faster to iterate on than a schema migration.

The backend engineering discipline: the data model should not be frozen until the product is stable. Flat files and simple key-value stores are appropriate for early-stage products where the data model is still being discovered. Migrate to a relational schema when the model is stable.

## Cron as Backend Architecture

Levels' products run hundreds of automated cron jobs that handle data ingestion, notification delivery, cache warming, and reporting. These are not microservices — they are PHP scripts scheduled by cron. The engineering discipline for cron-based backend automation: every cron job must be idempotent (safe to run more than once), must log its output, and must fail loudly (email or Slack notification on failure).

The backend engineering argument for cron over message queues: cron is simple, observable, and debuggable. A failed cron job produces output in the cron log. A failed message queue worker requires understanding the queue's consumer group state.

## Sources
- [levels.io — Levels' blog](https://levels.io/)
- *MAKE: The Indie Maker Handbook* — Pieter Levels, 2019
- ["How I build my minimum viable products" — levels.io, 2014](https://levels.io/how-i-build-my-minimum-viable-products/)
- [Lex Fridman Podcast #440 — Pieter Levels, 2024](https://lexfridman.com/pieter-levels/)
