# Simon Willison — On Web Development

## Deep Roots in Web Development

Willison has been a practicing web developer since 2000. He is not a theorist of the web — he is someone who has built web systems professionally for over two decades, across newspapers, startups, and open source projects. His web philosophy is shaped by this experience: he cares about things that work reliably at scale, that are maintainable over time, and that can be built quickly enough to be worth building.

He co-created Django in 2003–2004, which is itself a statement of web philosophy. Django emerged from the specific constraints of a newspaper: rapidly changing content requirements, tight deadlines, a need for a CMS that could be modified as fast as the news cycle demanded. "The web framework for perfectionists with deadlines" is not just a tagline — it reflects the environment that produced it.

## The Datasette Architecture as Web Philosophy

Datasette is built around a set of web philosophy choices that Willison has articulated clearly:

**SQLite as deployment unit.** A SQLite database is a single file. It can be copied, shared, deployed to serverless hosting, and versioned in Git. By packaging data as SQLite rather than requiring a database server, Willison makes deployment nearly frictionless. His breakthrough realization was that "read-only data packaged as a SQLite database could be deployed to inexpensive serverless hosting, where it could scale from zero up to handling an unlimited amount of inbound traffic."

**APIs as automatic output.** Datasette automatically generates JSON API endpoints for every table and query. Users get an API without having to build one. This reflects a philosophy that data should be machine-accessible by default, not just human-accessible.

**URLs as interfaces.** Datasette's URLs are designed to be shareable and bookmarkable. A filtered table view, a SQL query result, a specific row — all have stable URLs that can be shared. This is a web-native way of thinking about data: the URL is the document.

**Progressive enhancement.** The core browsing experience in Datasette works without JavaScript. JavaScript enhances the experience (faceted search, dynamic filtering) but is not required for basic access. This reflects a respect for the web's accessibility properties.

## Views on APIs

Willison is pragmatic about APIs. He builds them because they are useful, not because APIs are inherently good. His critique of over-engineered API design surfaces occasionally — he has written about preferring simpler CLI interfaces over REST APIs for AI agents, noting that CLI tools can be more accurate and cost-effective for many tasks because they are simpler to describe and invoke.

He has been a practitioner of REST since the early web, but he does not dogmatize about it. His tools expose JSON APIs where they are useful and omit them where they are not. He has built a GraphQL plugin for Datasette as an experiment — maintaining skepticism about GraphQL while allowing the community to explore it through the plugin mechanism.

## Git Scraping and Baked Data

Two techniques Willison named and popularized reflect his web thinking: "git scraping" and "baked data."

**Git scraping** is the practice of using GitHub Actions to periodically scrape a web source and commit the results to a Git repository. The repository becomes a time-series archive of the source. He has said that "if you really want people to engage with a technique, it's helpful to give it a name" — and git scraping became an officially supported pattern at GitHub, where they called it "Flat Data."

**Baked data** refers to generating static data files at build time rather than querying a database at request time. For data-heavy sites, serving pre-generated JSON or SQLite files from a CDN is more scalable and cheaper than running queries on live requests. This is a web architecture philosophy: bake complexity into the build, serve simplicity at request time.

## Speed of Development as a Value

Willison's web philosophy is deeply influenced by the newspaper context in which he developed it: speed is a constraint, not a nice-to-have. He has built web tools in a single afternoon, in a 17-minute session with Claude (documented in detail), and in 4.5 hours using Claude to port a Python application to JavaScript. He views the ability to build quickly as a product in itself. A tool that can be built fast enough to respond to a news story is worth building; one that would take months is not.

This philosophy has carried directly into his AI-assisted development work. He now maintains a repository of over 77 single-file HTML+JavaScript applications, each built through LLM prompting. The web platform — HTML, CSS, JavaScript — is the delivery mechanism he reaches for when speed matters most.

## The Django Legacy

Django's architecture reflects values Willison still holds: convention over configuration, batteries included, the admin interface as a default, the ORM as the standard way to interact with data. He has maintained his relationship with the Django community over the years, though his current work is more Python-and-SQLite than Python-and-Django. He contributed to the Datasette-Django integration (django-sql-dashboard) and continues to write about Django when relevant. His web thinking was shaped by building Django and has not fundamentally changed since.
