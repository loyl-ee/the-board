# Marco Arment — On Web vs. Native

## Strong Preference for Native iOS

Arment is a committed native iOS developer. His entire post-Tumblr career has been built on native apps — Instapaper, Overcast, Quitter — and he has been consistently skeptical of web apps as a replacement for native experiences on iOS. His reasoning is practical rather than ideological: native apps can do things web apps cannot.

He observed this firsthand when the iPhone launched. Developers could only build web apps initially, but native apps became available in 2008 because developers genuinely needed them. Web apps had fundamental limitations on iOS: no background processing, no full-screen operation, unreliable caching (the cache manifest was "a recommendation, not a law on iOS, and can even be deleted automatically"), and JavaScript performance that was "getting better but not good enough." (An Event Apart, 2012, via lukew.com) For the category of app he builds — audio playback running reliably in the background while users do other things — a web app is not an option.

## The Native-Only Product That Could Not Be a Web App

Overcast is the clearest proof of his position. The app's signature features — Smart Speed and Voice Boost — require real-time audio processing in a background thread, precise control over audio sessions, interaction with iOS's audio routing and interruption system, and the ability to modify audio as it plays. "Overcast could almost certainly not have been created as a web app," as one analysis put it. Apps that interact with audio and video need native code to delve deep and tune performance, latency, and interaction at a level web technologies cannot reach.

Voice Boost 2 was written in pure C rather than even using Apple's AudioUnits framework, because Arment wanted maximum control and performance. The processing had to run in real-time at under 1% CPU on older devices. This level of optimization is native-platform work — not web work, not even high-level framework work.

## Instapaper and the Web Content Problem

There is a tension in Arment's relationship with the web. Instapaper was fundamentally a service for web content — it saved articles from web pages and made them readable on devices. He built a text-parsing and reformatting system that stripped web articles down to clean, readable text, which was the entire value proposition. In that sense, his most successful pre-Overcast product was deeply web-adjacent.

But Instapaper's interface was always native. The bookmarklet was a web tool; the reading experience was a native app. He understood early that the web is an excellent content delivery system and a poor user experience system for extended reading — hence the product. The "read later" category he helped pioneer is in many ways a verdict on the quality of the web reading experience: it is bad enough that people prefer to extract content from it and read it elsewhere.

## Marco.org as a Personal Publishing Platform

His blog at marco.org, launched in December 2006, is a personal publishing platform he has maintained for nearly two decades. He runs it himself rather than using any hosted blogging service — an unusual choice that reflects his views on ownership, control, and the importance of independent web property.

He has written about this: "Writing your own blog platform is like roasting your own coffee: it's impractical and you probably shouldn't do it, but for people who really, truly care about it, it's worthwhile to them..." (AZQuotes) The analogy is revealing — he knows it's not the efficient choice, but he values control over the publishing experience enough to maintain it anyway.

His departure from Twitter to Mastodon in late 2022 (following Elon Musk's acquisition) reflects the same preference: owned, decentralized, open protocol over corporate-controlled platform. He has consistently favored platforms and tools where users retain ownership and portability of their data and relationships.

## Views on App Ecosystems

Arment has argued that the shift from web to apps fundamentally changed how users find software. People look for apps; they do not necessarily go to websites. Instapaper had 30,000 web users when it launched in the App Store — the native app dramatically expanded reach in a way the web presence alone could not. He sees the App Store, despite its many flaws, as a genuinely powerful distribution mechanism for consumer software — which is why he has continued to invest in it despite his criticisms of Apple's policies around it.
