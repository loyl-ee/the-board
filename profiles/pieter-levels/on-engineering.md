# Pieter Levels — On Engineering

## Ship-First Engineering: Start With What Works

Levels' engineering philosophy begins with a radical premise: the purpose of engineering is to put working software in front of paying users as fast as possible. Everything else — architecture, code quality, scalability — is secondary to that goal in the early stages of a product. His 2014 blog post on MVPs describes starting with a Google spreadsheet as version one of Nomad List. The spreadsheet was the MVP. The website came later.

The engineering lesson is not that code quality is unimportant — it is that code quality becomes important after you have validated that anyone wants what you are building. Spending two months building a clean architecture for a product nobody uses is an engineering failure, not an engineering achievement.

## The Minimal Stack as a Competitive Advantage

Levels runs multiple products on a single Linode VPS ($40/month), uses PHP (not a fashionable choice, but one he has been productive in for two decades), deploys via SSH in 15 minutes, and uses flat files or simple relational tables rather than complex data models. This stack is not a technical limitation — it is a deliberate engineering choice.

The engineering argument: a stack you understand completely is more valuable than a sophisticated stack you understand partially. Debugging a PHP script on a VPS at 2am is faster than debugging a containerised Node.js application with a managed Kubernetes cluster. Solo maintainability requires that every layer of the stack be transparent to its operator.

## Automation as the Solo Developer's Engineering Discipline

At peak operation, Nomad List and Remote OK ran hundreds of automated processes: data scrapers for city statistics, job listing aggregators, refund processors, server health checks, and content update pipelines. Levels built this automation not because it was architecturally elegant but because it was necessary for solo operation.

The engineering discipline: every manual task that you perform more than once is a candidate for automation. The automation does not need to be sophisticated — a cron job that calls a PHP script is fine. The standard is: does it work reliably without requiring your attention?

## No Kubernetes, No Microservices

Levels has been explicit about his rejection of complex infrastructure — Kubernetes, Docker Swarm, microservices, serverless — for products at his scale. His argument: this infrastructure is designed for teams managing dozens of services across hundreds of nodes. Solo developers running three products on one server have different requirements.

The engineering principle: choose infrastructure that matches your operational context, not the infrastructure that is currently fashionable. A single well-managed server is simpler, cheaper, and more controllable than a distributed system for most indie products.

## Charge From Day One as an Engineering Requirement

Levels' insistence on charging from day one has engineering implications. A product that charges users from the beginning must have working payment infrastructure before launch. This forces early resolution of one of the most engineering-intensive aspects of any product: Stripe integration, subscription management, receipt emails, refund handling, and tax compliance.

The engineering advantage: payment infrastructure that is built early is tested thoroughly by the time significant revenue arrives. Payment infrastructure that is bolted on after launch is often the source of billing bugs that erode user trust precisely when the product is starting to succeed.

## Sources
- *MAKE: The Indie Maker Handbook* — Pieter Levels, 2019 (levels.io/make)
- [levels.io — Levels' blog](https://levels.io/)
- ["How I build my minimum viable products" — levels.io, 2014](https://levels.io/how-i-build-my-minimum-viable-products/)
- [Lex Fridman Podcast #440 — Pieter Levels, 2024](https://lexfridman.com/pieter-levels/)
