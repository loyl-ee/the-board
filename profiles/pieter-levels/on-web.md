# Pieter Levels — On Web Development

## PHP and Vanilla JavaScript: The Anti-Framework Stack

Levels' web stack is deliberately old-fashioned and he is unapologetic about it. He uses PHP (without a framework), vanilla JavaScript with jQuery, SQLite, and plain HTML with SCSS. His flagship products — including Remote OK, which generates over $90K/month — run as single PHP files. He has tweeted the now-famous line: "remoteok.io is a single PHP file called 'index.php' generating $101,101 this month. No frameworks. No libraries (except jQuery)." (@levelsio, Twitter, April 2021.)

This is not a beginner's default — it is an informed rejection of complexity. Levels has evaluated modern JavaScript frameworks and found them actively harmful to the solo maker context:

- They require constant updates when new versions break APIs.
- They add build tool complexity (Webpack, Babel, TypeScript config) that has no proportional value for simple products.
- They optimize for team collaboration and code organization at the cost of development speed for solo developers.
- They create vendor dependency on framework ecosystems that may not persist.

His counter-argument for PHP: "PHP just stays the same and works." (Lex Fridman Podcast #440, 2024.) A PHP file written in 2014 still runs in 2026 without modification. A React component written in 2014 has been through several breaking API changes.

## The Framework Army

Levels has been notably provocative about JavaScript framework culture, describing "framework armies" that emerge on Twitter to defend their preferred tools. His critique is pointed: "I wanna ask the framework army, what have they built this week?" He is suspicious of the commercial incentives behind framework promotion: "There's money in this developer framework scene. There's hundreds of millions that goes to ads or influencer or whatever." (Lex Fridman Podcast #440, 2024.)

This critique is not purely technical — it is about the culture of discussing tools rather than building products. His position: someone shipping a useful product in PHP is more valuable to the world than someone debating React versus Vue on Twitter. "The people discussing what programming language is best are not shipping products." (MAKE book.)

## Simple Infrastructure for Resilience

Levels' infrastructure philosophy mirrors his framework philosophy: use the minimum infrastructure required. His 2014 MVP setup was a single Linode VPS ($40/month) running Nginx with PHP-FPM, Ubuntu LTS, and JSON text files as data storage. This entire stack can be understood by one person, debugged by one person, and migrated by one person.

He has used Cloudflare for CDN and DDoS protection (his Flight Simulator product was hit with 120 million requests and Cloudflare absorbed the attack), and Stripe for payments (which he treats as a required dependency, not an infrastructure choice). Beyond these, he minimizes third-party dependencies.

The practical advantage: when something breaks at 3am, a solo founder who understands the entire stack can fix it. A complex microservices architecture that breaks at 3am requires a team.

## SEO as a Growth Lever

Levels built Nomad List's organic traffic through systematic SEO rather than paid acquisition. The key mechanic: Nomad List generates a unique URL for every filtered combination of cities (e.g., /cities/safe/cheap/warm-weather/good-internet). Each filter combination becomes an indexable page with a unique long-tail keyword. This "programmatic SEO" approach creates hundreds of ranking opportunities from one data model without writing individual articles. (Nomad List Programmatic SEO Strategy, YouTube case study.)

Remote OK applies the same logic to job listings: each listing, each category, each location combination generates indexed URLs. At scale, this creates thousands of ranking pages from user-generated content.

The strategic implication: good URL architecture and structured data can substitute for a content marketing team if the product generates enough unique, useful, indexed pages through its natural operation.

## Anti-Complexity as Competitive Advantage

Levels argues that technical simplicity is a business advantage, not just a personal preference. His sites load quickly because they have minimal JavaScript overhead. They are easy to maintain because they have minimal dependencies. They are easy to understand because they have minimal abstraction.

For a solo founder, this means: every hour not spent debugging framework compatibility is an hour available for product improvement, customer support, or building a new product. The compounding effect of this decision over years is substantial.

He does not advocate this stack for all contexts — only for the indie maker context where speed, solo operability, and long-term maintainability without a team are the dominant constraints. He has acknowledged that building in this way is not "according to the rules" and explicitly warns against copying his workflow exactly: "it'd be a bad idea to follow how I do things exactly. It's probably better to just figure out your own workflow." (levels.io/how-i-build-my-minimum-viable-products/.)

## On No-Code Tools

Levels acknowledges in the MAKE book that non-technical founders can launch using no-code tools (Typeform, Zapier, Carrd) and that the technology choice matters less than shipping. "Build your idea with the tools you already know." This is not inconsistent with his PHP advocacy — the underlying principle is: use what you know, ship fast, don't let the tool choice be the bottleneck.
