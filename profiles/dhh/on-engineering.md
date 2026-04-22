# DHH — On Engineering

## Opinionated Software Starts With Opinionated Code

Hansson's engineering philosophy is inseparable from his product philosophy: code must have a point of view. The framework that made him famous — Ruby on Rails — is a direct expression of this. Rails does not try to accommodate every architectural preference. It enforces conventions, chooses defaults, and makes the path of least resistance the path of good practice. The framework is the engineer's opinion encoded in code.

"Convention over configuration" is not a feature toggle — it is a position about how software should be built. When you name a database table `users` and a model `User`, Rails wires everything together without configuration. If you fight the convention, you pay a friction tax. The friction is intentional. It pushes engineers toward the path that experience has shown to be correct.

## The Majestic Monolith

Hansson coined the term "majestic monolith" as a direct pushback against the microservices hype of the 2010s. His argument: a single, unified codebase is easier to understand, easier to debug, easier to deploy, and easier to maintain than a distributed system — especially at the scale most teams operate at.

Basecamp 3 runs on a monolith serving web, iOS, Android, macOS, Windows, and email for millions of users, maintained by a team of roughly 12 engineers. The monolith is not a technical debt waiting to be paid — it is an architectural achievement. Complexity is the enemy. Distributing services creates distributed complexity, distributed failure modes, and distributed debugging nightmares. The majestic monolith acknowledges that most applications never outgrow a single process, and that premature decomposition is as harmful as premature optimisation.

## HTML First, JavaScript When Necessary

Hansson has been a vocal advocate for server-rendered HTML as the default web architecture. Hotwire — the framework he co-created and ships in every Rails project — delivers HTML over the wire instead of JSON, updates pages using Turbo Streams and Turbo Frames, and adds interactivity through Stimulus rather than heavy client-side JavaScript.

The engineering argument is not aesthetic: full-stack JavaScript frameworks require engineers to maintain two codebases (server and client), manage state in two places, and handle serialisation/deserialisation of every data type. Hotwire collapses this into a single coherent system. Pages are fast (HTML from the server is faster to parse than JSON plus a render cycle), progressive enhancement works by default, and a junior engineer can understand the full request cycle.

## Database as the Source of Truth

Hansson has consistently advocated treating the relational database as the primary source of business logic integrity — not just a persistence layer. Constraints, validations, and foreign keys belong in the database, not only in application code. Rails migrations are the canonical expression of this: schema changes are version-controlled, sequential, and applied consistently across every environment.

He is sceptical of ORMs that abstract the database into irrelevance. ActiveRecord is designed to be a thin, productive layer — not to hide SQL. When you need SQL, you write SQL. Knowing your database is part of knowing your application.

## Ship It, Then Improve It

Hansson's engineering ethic aligns with his broader philosophy on deadlines: scope is the variable, not time and quality. The Shape Up methodology that 37signals uses treats engineering in six-week cycles — appetites rather than estimates. The question is not "how long will this take?" but "how much is this worth?" If a feature can't be built in the available time with acceptable quality, it gets cut or redesigned, not rushed or extended.

"Real Artists Ship" is not permission to ship bad code. It is a reminder that finished beats theoretical. A working feature with a few rough edges delivers more value than a perfect feature that never lands.

## Sources
- [The Ruby on Rails Doctrine](https://rubyonrails.org/doctrine)
- [The Majestic Monolith — Signal v. Noise](https://signalvnoise.com/svn3/the-majestic-monolith/)
- [Hotwire](https://hotwired.dev/)
- *Shape Up* — 37signals, 2019 (basecamp.com/shapeup)
- [Building HEY with Hotwire — Full Stack Radio #151](https://fullstackradio.com/151)
