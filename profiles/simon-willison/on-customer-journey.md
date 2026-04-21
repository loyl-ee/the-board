# Simon Willison — On Customer Journey

## His Primary User: The Data Journalist

Willison has articulated a clear and specific primary user archetype throughout his career: the data journalist. This is someone who has data, has a story they suspect is in the data, but lacks the technical infrastructure to get from one to the other efficiently. He spent time at The Guardian working alongside people in exactly this situation. His JSK fellowship at Stanford was explicitly organized around building tools for this user. His stated ambition is to write software that helps a journalist win a Pulitzer Prize.

This is not an abstract persona. It shapes every tool decision. Datasette's interface supports arbitrary SQL queries but also provides a point-and-click table browser for users who are not comfortable writing SQL. The plugin architecture means capability can be added without making the core interface more complex. Datasette Cloud offers a hosted version specifically to remove the barrier of installing and managing software.

## Broadening the Audience Without Losing the Core

Willison is aware that his primary user — data journalists, archivists, researchers — is not the only user. Museums, local governments, scientists, and open data advocates use Datasette. He describes the broader audience as "anyone else who has data that they wish to share with the world."

His approach to this broader audience is additive rather than re-centered. He does not redesign for the widest possible user; he extends capability and documentation so that users with more varied backgrounds can find entry points. The plugin ecosystem does this organically — different plugins address different use cases without requiring him to anticipate all of them.

## Open Source Community Building

Willison treats his open source community as a key stakeholder group. He ran regular office hours for Datasette — live video sessions where users could ask questions and observe development. He responds to GitHub issues. He writes detailed changelogs and annotated release notes. He signals that the project is actively maintained and that users who invest in it will be supported.

His plugin architecture is also a community strategy. By making it easy for external developers to extend Datasette and LLM, he creates a network of invested contributors who have skin in the ecosystem's success. A developer who has built a plugin for Datasette is a more committed advocate than a passive user.

## How He Thinks About User Research

Willison's user research is mostly informal and embedded. He talks to journalists directly. He reads GitHub issues carefully. He writes about his own use of his tools, which generates feedback from readers who have similar or different use cases. He does not conduct formal usability studies, and he has not written extensively about user research methodology.

What he does do is stay very close to the actual use cases. His work at The Guardian gave him firsthand exposure to journalism workflows. His JSK fellowship gave him a year of structured contact with the journalism education community. His regular blog writing attracts a readership that includes many of his users, who engage with posts and surface problems.

## Making Complex Data Accessible

The central customer journey Willison designs for is: user has data in a CSV or database file → user wants to explore it, share it, or publish it → user uses Datasette. Every barrier in that journey is a product problem. He has worked systematically through the barriers: installation friction (solved by Datasette Cloud), SQL requirement (solved by point-and-click UI), publish friction (solved by deployability to serverless hosting), collaboration friction (ongoing work).

He is not designing for a user who wants to outsource the thinking. He is designing for a user who wants to do the thinking themselves, but needs tools that do not get in the way.
