# Brent Simmons — On Frontend Engineering

## The Open Web as Engineering Commitment

Simmons' frontend engineering is grounded in the open web: HTML, CSS, and JavaScript as standards that are implemented by every browser, maintained by the W3C, and available to every developer without license or platform approval. His advocacy for the open web is partly philosophical — the web should remain an open publishing medium — and partly engineering: software built on open standards outlasts software built on proprietary platforms.

The engineering implication: when a web feature can be implemented with standard HTML and CSS, it should be. When JavaScript is required, vanilla JavaScript should be evaluated before frameworks. The question is not "which framework?" but "does this require a framework?"

## Semantic HTML as Engineering Quality

Simmons advocates for semantic HTML: using elements for their intended semantic purpose rather than as layout primitives. `<article>` for articles, `<nav>` for navigation, `<header>` for page headers, `<time>` for timestamps. Semantic HTML provides accessibility for free — screen readers understand semantic elements — and provides styling hooks that are more maintainable than class names invented to describe visual appearance.

The frontend engineering discipline: write HTML that is correct without CSS. If the document structure makes sense and is readable without styling, the HTML is semantically correct. Add CSS to express the visual design, not to compensate for structural deficiencies.

## RSS and Feed Engineering

NetNewsWire parses RSS and Atom feeds from thousands of publishers. The engineering discipline of feed parsing is specific: feeds are malformed, inconsistently structured, and occasionally adversarial. A feed parser must handle missing fields, incorrect date formats, HTML in fields that expect plain text, and encoding issues.

The engineering lesson from feed parsing: any system that consumes external data must be defensively written. Assume that the data will violate the specification. Parse permissively, fail gracefully, and log unexplained structures for future improvement.

## The Reading Experience as Frontend Engineering

NetNewsWire's article reader is a WebKit web view that renders article content from the feed. The engineering of a good reading experience in a web view includes: appropriate font sizing for the device, line length control, dark mode support, link detection, and performance (articles should render immediately, not after a visible layout reflow).

The frontend engineering standard for reading experiences: the reading experience should be better than the original web page, not a degraded version of it. If the web view renders worse than the original source, the engineering work is not done.

## Avoiding JavaScript Framework Dependencies

Simmons uses minimal JavaScript dependencies across his projects. NetNewsWire's website is a static site with minimal JavaScript. The engineering argument: JavaScript dependencies are maintenance liabilities — each dependency can introduce security vulnerabilities, break on major version updates, or be abandoned by its maintainers.

The frontend engineering discipline: prefer browser APIs over library equivalents when the browser API is adequate. `fetch` instead of axios. `document.querySelector` instead of jQuery. CSS animations instead of JavaScript animation libraries.

## Sources
- [inessential.com — Simmons' blog](https://inessential.com/)
- [NetNewsWire — GitHub (open source)](https://github.com/Ranchero-Software/NetNewsWire)
- [NetNewsWire blog](https://netnewswire.blog/)
- [Open web advocacy posts — inessential.com](https://inessential.com/)
