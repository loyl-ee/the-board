# Sal Soghoian — On Design

## Making Complex Things Simple Without Dumbing Them Down

The central design problem Soghoian has spent his career solving is one that has no clean resolution: how do you make powerful, complex automation accessible to people who are not programmers, without reducing it to something that no longer serves sophisticated users? His answer is not a compromise — it is a layered architecture where each layer is genuinely useful on its own terms.

Automator embodies this design philosophy most clearly. The visual workflow builder is not a simplified version of AppleScript. It is a different mode of expressing automation logic that is genuinely powerful for the tasks it handles well — batch processing, sequential multi-step workflows, data transformation pipelines. The fact that it is also easier than scripting is a design achievement, not a design concession.

## Visual Metaphors for Scripting Concepts

The Automator interface was designed around a specific visual metaphor: automation as assembly line. Actions are components on a conveyor belt; data flows left to right (in later versions, top to bottom); each station transforms the material and passes it along. This metaphor is powerful precisely because it matches how professional workflows actually work — a document moves through a production pipeline, being transformed at each stage.

This visual representation does important pedagogical work. A user who builds an Automator workflow learns, without being taught explicitly, what a pipeline is, what data types mean (because Automator shows you when types are incompatible), and how sequential operations compose. The design teaches the underlying concepts through the act of using the tool, rather than requiring the user to study concepts before using the tool.

At WWDC 2010, Soghoian described his own relationship with this design philosophy: "I don't want to know how to write the HTML but I'm forced to because of my job. But I just like using these tools of select this, select that, go, build, all right, done." (WWDC Session 302, 2010.) The best automation design, in his view, is one where the user can be productive without caring about the implementation.

## The Action Library as Interface

A less-discussed design decision in Automator is that the action library itself is a primary interface element. Users discover what is possible not by reading documentation but by browsing the library — by finding actions they did not know existed and connecting them in ways the designer never anticipated. This is discovery-driven design: the library communicates capability, not just function.

Soghoian and his team invested heavily in the quality and breadth of the initial action library precisely because they understood that users would assess the tool's power by what they found in it. An empty or poorly-organized library would signal a limited tool regardless of the underlying technical capability.

## The Console as Design Element

In his Omni Automation work, Soghoian championed an in-app JavaScript console — a direct line between the user and the application's automation layer. The design rationale is revealing: "If they have a console, well, you write a script, then you can watch it, the effect of it, immediately in the application. So if you're in OmniGraffle, you go add shape, quote circle, and then you give it a set of sizes and stuff and you hit return and then all of the sudden a circle shows up on your canvas." (Automators podcast, quoted in Rosemary Orchard's notes, 2018.) The console turns scripting from a write-run-check cycle into a conversation. That conversational quality is a design feature that dramatically lowers the learning curve for automation newcomers.
