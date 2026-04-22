# Pieter Levels — On Security

## Practical Security for the Solo Developer

Levels' security approach is pragmatic rather than comprehensive. He focuses on the security measures that provide the most risk reduction for the least engineering effort — the 80/20 of security. For solo developers with limited time, this means: HTTPS everywhere, Stripe for payment processing (never handle card data yourself), parameterised queries (no SQL injection), and daily backups.

The security engineering principle for small teams: perfect security is not achievable. Prioritise the vulnerability classes that are most likely to be exploited and most damaging if they are. SQL injection and payment data exposure are in this category. Theoretical vulnerabilities in systems that are not targeted are not.

## Never Handle Payment Data Directly

Levels uses Stripe for all payment processing across his portfolio — Nomad List, Remote OK, PhotoAI, InteriorAI. The security argument is absolute: card data handled by your systems is card data that can be breached from your systems. Stripe's PCI compliance, fraud detection, and security infrastructure represent a security investment that no solo developer can match.

The engineering security rule: never write code that stores, processes, or transmits card numbers. Use a payment processor that is PCI-compliant and handles all card data on their infrastructure. The engineering integration cost is a one-time payment; the ongoing security benefit is permanent.

## HTTPS as a Non-Negotiable Baseline

Every Levels product uses HTTPS. He has discussed this as a baseline, not a feature — something that is configured before the first line of application code is written. Modern hosting platforms make HTTPS free and automatic (Let's Encrypt, Cloudflare). There is no engineering reason to run unencrypted HTTP for any user-facing application.

The security standard: configure HTTPS, HSTS (HTTP Strict Transport Security), and secure cookie flags before writing application logic. These are infrastructure decisions, not application decisions, and they should be made once.

## Backups as a Security Practice

Levels takes daily backups of every database across his portfolio. He has described this publicly as essential infrastructure: not for disaster recovery alone, but as a security response capability. If a server is compromised, the backup is the path to restoration. If data is accidentally deleted (by a bug, by a malicious actor, by a misconfiguration), the backup is the path to recovery.

The security engineering standard: automated daily backups, tested restoration, and off-site storage. A backup that has never been restored is not a backup — it is a hope.

## Rate Limiting as Security Infrastructure

Levels implements rate limiting on authentication endpoints and API routes to prevent brute force attacks and credential stuffing. For a solo developer, this is one of the highest-leverage security controls: it prevents a large class of automated attacks with relatively simple engineering.

The security engineering checklist for any web application: rate limit login attempts, limit password reset requests, and limit API calls per IP address and per authenticated user. These are not sophisticated security measures — they are table stakes that prevent the most common automated attacks.

## Sources
- [levels.io — Levels' blog](https://levels.io/)
- *MAKE: The Indie Maker Handbook* — Pieter Levels, 2019
- [Lex Fridman Podcast #440 — Pieter Levels, 2024](https://lexfridman.com/pieter-levels/)
- [Stripe documentation — stripe.com](https://stripe.com/docs)
