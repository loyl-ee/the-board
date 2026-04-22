# DHH — On Frontend Engineering

## HTML First: The Hotwire Philosophy

Hansson's frontend engineering philosophy is articulated through Hotwire — the set of frontend libraries (Turbo, Stimulus, Strada) that he co-created and ships with Rails by default. The central premise: the web is a hypertext medium, and HTML responses from the server are the correct primitive for web applications. The engineering investment should go into making server-rendered HTML fast and interactive, not into a JavaScript application that replicates the server's logic on the client.

Turbo Frames and Turbo Streams allow specific parts of the page to update in response to user interactions without a full page reload. The engineering result: the interactivity of a single-page application without a separate JavaScript codebase, without client-side routing, and without the serialisation overhead of JSON APIs.

## The Cost of JavaScript Application Frameworks

Hansson has been consistently critical of heavy JavaScript frameworks for web applications — React, Angular, Vue, and their descendants. His argument is engineering, not aesthetic: these frameworks require developers to maintain two application models (server and client), manage state in two places, handle serialisation and deserialisation of every data type, and build client-side routing that duplicates server-side routing.

The engineering cost is significant and ongoing. A Hotwire application has one place where the application logic lives (the server), one data model (the database), and one routing layer (the server router). The frontend is a presentation layer, not a separate application.

## Stimulus: Behaviour Without Framework Lock-In

Stimulus — the lightweight JavaScript library Hansson co-created — is designed for adding behaviour to HTML rather than managing HTML from JavaScript. A Stimulus controller responds to DOM events and manipulates DOM elements; it does not manage component state or own the HTML structure. The HTML comes from the server; Stimulus enhances it.

The frontend engineering principle: HTML should be the source of truth for structure. JavaScript should enhance HTML, not generate it. A page that requires JavaScript to render its content has failed to be progressive.

## CSS Is Underrated

Hansson has argued that modern CSS — with custom properties, flexbox, grid, and nesting — is powerful enough to implement most of the interactive behaviours that frontend engineers reach for JavaScript to handle. `:hover` states, `:focus-visible` for keyboard users, CSS transitions, and CSS Grid for responsive layouts cover an enormous range of use cases without JavaScript.

The frontend engineering discipline: before writing JavaScript for a UI behaviour, verify that CSS cannot express it. The engineering investment in CSS correctness pays dividends in performance, accessibility, and progressive enhancement.

## Web Performance as an Engineering Ethics Commitment

Hansson has argued that slow web pages are not just bad UX — they are a form of disrespect for users' time. The engineering standard for web pages is not "acceptable performance" but "fast performance" — pages that load in under one second, interactions that respond in under 100ms, and transitions that run at 60fps.

Hotwire's architecture produces fast pages by construction: server-rendered HTML is faster to parse than a JavaScript bundle that generates the same HTML, and HTTP/2 push of the first HTML response is faster than a round-trip to an API.

## Sources
- [Hotwire — hotwired.dev](https://hotwired.dev/)
- [Turbo — turbo.hotwired.dev](https://turbo.hotwired.dev/)
- [Stimulus — stimulus.hotwired.dev](https://stimulus.hotwired.dev/)
- [Building HEY with Hotwire — Full Stack Radio #151](https://fullstackradio.com/151)
- [DHH on JavaScript frameworks — various blog posts and talks]
