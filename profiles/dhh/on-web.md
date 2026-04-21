# DHH — On the Web

## The Web Platform as Sufficient

Hansson's web philosophy is a defense of the web as a platform against what he sees as unnecessary complexity layered on top of it. His core position: HTML and CSS, properly used and served from a server, are capable of building sophisticated, responsive, and delightful web applications. The decision to replace server-rendered HTML with client-side JavaScript frameworks was not primarily a technical improvement — it was a fashion, and it has imposed real costs on developers and organizations who adopted it.

## HTML Over the Wire

In late 2020, Hansson introduced Hotwire (HTML Over The Wire), a collection of techniques and libraries for building modern web applications without the complexity of client-side JavaScript frameworks. The key insight is simple: instead of sending JSON from the server and reconstructing the interface in the browser, send HTML fragments. The server renders the view; the browser inserts it.

This approach, formalized through the Turbo and Stimulus libraries, powers both Basecamp and HEY. HEY shipped with roughly 40KB of JavaScript to the client — a fraction of what a React or Vue equivalent would require. The full application, including mobile-native behavior, runs as what Hansson calls a Majestic Monolith: a single Rails application that serves web, iOS, Android, macOS, and Windows from the same codebase.

Hansson described the HTML over the wire approach as paying off "complexity loans" taken out during the JavaScript SPA era: "The price for pursuing JavaScript for everything has been a monstrosity of modern complexity."

## Rejecting JavaScript Complexity

Hansson's critique of JavaScript-heavy frontend development is specific, not aesthetic. His objections:

**Scale mismatch**: The architectures popularized by Facebook and Google (React, microservices, GraphQL APIs) were designed for companies with thousands of engineers managing massive, distributed systems. Most web applications are not that. Applying enterprise-scale architecture to a team of five produces the overhead without the benefit.

**Human comprehensibility**: His standard for good architecture is whether a single developer can understand the full system. Client-side JavaScript frameworks, build pipelines, state management libraries, and API layers collectively exceed what one person can hold in their head. The Majestic Monolith — a Rails app with Hotwire — can be understood by an individual. That comprehensibility matters for debugging, onboarding, and long-term maintenance.

**Developer experience**: Hansson has stated that it was extraordinarily easy to build for the web in the late 1990s, and that much of what has happened since has been a regression — not in capability, but in the ratio of capability gained to complexity added.

## The Majestic Monolith

Hansson coined this term to describe and rehabilitate a software architecture that became unfashionable: the single, unified application. In the architecture debates of the 2010s, microservices — many small, independently deployable services — were presented as the modern approach. Hansson has consistently argued that microservices impose coordination overhead, distributed system complexity, and operational burden that most applications do not need and most teams cannot manage.

His tweet summarizing this: "It feels like we've regressed a lot when it comes to basic scaling and architecture for the web. Basecamp launched in 2004 on a SHARED server. We ran with a single box until we had thousands of paying users. One majestic monolith." (Twitter/X, 2020)

He has also argued for migrating back from microservices when teams recognize the costs outweigh the benefits, and 37signals has published accounts of doing exactly that.

## Server Ownership and Cloud Skepticism

In a widely-discussed 2023 move, 37signals announced it was leaving the cloud — migrating off AWS to owned hardware in data centers. Hansson documented the economics: at 37signals' scale, owned hardware was dramatically cheaper than cloud computing, and the operational complexity of self-managed servers was manageable for a team with their expertise.

He was careful not to generalize this into universal advice. His argument was specific: at sufficient scale and with sufficient infrastructure competence, owned hardware wins on cost. Smaller teams or teams without infrastructure expertise may rationally choose the cloud.

## The Web as a Universal Platform

Underlying all of Hansson's web philosophy is a belief in the web as a universal, open, interoperable platform. He has argued that excessive JavaScript complexity balkanizes the web — making it harder for different backend languages to participate, making it harder for independent developers to build and maintain applications, and concentrating power in a small number of JavaScript frameworks controlled by large companies.

Hotwire is explicitly designed to restore backend language diversity: Rails uses it, but it works with any server-side framework. The HTML-first approach means Ruby, Erlang, Clojure, Python — any language that can generate HTML — can participate in building modern web applications without JavaScript expertise.

## Sources
- [Hotwire: HTML Over The Wire](https://hotwired.dev/)
- [HTML over the wire — Signal v. Noise](https://signalvnoise.com/svn3/html-over-the-wire/)
- [The Majestic Monolith — Signal v. Noise](https://signalvnoise.com/svn3/the-majestic-monolith/)
- [Building HEY with Hotwire — Full Stack Radio #151](https://fullstackradio.com/151)
- [How to Recover from Microservices — world.hey.com/dhh](https://world.hey.com/dhh/how-to-recover-from-microservices-ce3803cc)
- [DHH on X: Basecamp monolith tweet, 2020](https://x.com/dhh/status/1225106054079336449)
