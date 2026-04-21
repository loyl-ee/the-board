# Brent Simmons — On UX

## The Reading Experience as the Primary Contract

Simmons has spent more than two decades thinking about what it means to read on a computer. His entire most significant project — NetNewsWire — exists to serve the act of reading. This is not incidental. The reading experience is the product. Every UX decision in NetNewsWire is downstream of a single commitment: give the user a calm, fast, unobstructed way to read the things they chose to follow.

This means no algorithmic reordering. No engagement notifications. No infinite scroll designed to keep users reading past the point of their actual interest. Articles appear in chronological order from sources the user explicitly subscribed to, and they age out automatically rather than piling up into an undifferentiated backlog. The UX is, in its structure, an argument about how information consumption should feel.

## Reading Is Not a Task

One of Simmons' most enduring UX positions: RSS readers should not make users feel guilty. "Your RSS reader should not be a taskmaster or a source of guilt." (inessential.com, "NetNewsWire Article Age Limits," October 13, 2018) The inbox metaphor — which NetNewsWire itself introduced to RSS readers in 2002 by borrowing the three-pane email layout — created phantom obligation. Articles accumulated like unread email. Users felt behind.

His solution was article age limits: articles expire after roughly 90 days, the system always retains a minimum set of recent articles per feed, and starred items are never deleted. This is UX as psychological design. The system is designed to prevent the accumulation of dread.

## Keyboard-First Interfaces

Simmons is a keyboard-centric user himself. He uses Vim as his primary editor and has organized his own workflow around keyboard efficiency. NetNewsWire has always reflected this priority. He added a dedicated Keyboard Shortcuts page to the Help menu (inessential.com, August 22, 2003) and ensured that the most common reading operations — scrolling an article, jumping to the next unread item, opening in a browser — are reachable without lifting hands from the keyboard.

This is not a power-user feature. It is a respect for the reality of how productive Mac users work. Someone reading through 50 articles in a morning should be able to do it entirely with keyboard shortcuts. The Space bar to scroll and advance, N to go to the next unread, B to open in the browser — these are the reading interface at its most efficient.

## Transparency and Non-Mysterious Behavior

Simmons has written that software should "never behave mysteriously." (inessential.com, "NetNewsWire Article Age Limits," 2018) In UX terms, this is a commitment to predictability. Users who understand why their app behaves as it does — because the behavior is legible, documented, and logically consistent — trust it more and make better use of it.

The article age limit design is a concrete example: rather than silently deleting articles based on hidden arrival timestamps, the system uses publication dates (which are visible and meaningful to users) and explains its behavior in the Preferences pane. Transparency is part of the interaction design.

## The Privilege of the Daily Driver

Simmons has described the responsibility of making an app that people use every day as a kind of privilege — one that carries obligations. If NetNewsWire is someone's primary source for reading the web, then any failure in reliability, speed, or trustworthiness is a significant disruption to that person's daily life. This is why performance is foundational ("it's the pizza," not a topping), why crashes must be fixed quickly, and why behavioral changes require careful communication.

He articulated this succinctly in describing his philosophy for the Rands in Repose interview: the best innovation is often no innovation — present something new (like RSS feeds) in a familiar way. Respecting the user's existing mental models is itself a form of UX care.

## Programming as Communication

Simmons rejects the idea that software development is primarily a mathematical discipline. He has written that the real challenge in making good apps is "communicating with the user. So that it's easy to understand and fun to use." (inessential.com, "What I Do") Coding is a means to a communicative end. The UX is the message.
