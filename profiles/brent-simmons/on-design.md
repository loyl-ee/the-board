# Brent Simmons — On Design

## Mac-Native as a Design Philosophy

Simmons' design aesthetic is inseparable from his view of what the Mac is. He does not think in terms of visual styling or color palettes; he thinks in terms of platform fit. A Mac application that feels at home on the Mac earns that feeling by honoring the conventions of the platform: menus, multiple windows, the Responder Chain, keyboard-first navigation, and interfaces scaled for a precision pointer rather than a fingertip.

His 2016 essay "On UIKit for Macs" (inessential.com) catalogued precisely what distinguishes Mac design from iOS design: "On iOS you don't have to deal with multiple, resizable, movable windows open at the time, or with being open but not frontmost, or with a window moving between screens with different resolutions." These are not implementation details — they are design constraints that shape every decision about how an application presents itself and how it behaves when partially occluded, when focus shifts, when the user switches windows.

## Direct vs. Indirect Interfaces

Simmons wrote a careful 2019 essay distinguishing direct (touch) from indirect (keyboard + pointer) interfaces. (inessential.com, "Direct and Indirect Interfaces," June 26, 2019) His argument: indirect interfaces are not deficient versions of touch interfaces. They are optimized for different strengths. "When you have a hardware keyboard and a precision pointer that takes very little energy to move, then you can do things that would be non-ergonomic for a direct interface." Higher information density, smaller interaction targets, multiple monitors, the ability to work efficiently for eight-plus hours — these all emerge from indirect input design.

This matters for design in a concrete way: iOS design patterns, imported uncritically to the Mac, sacrifice the advantages that make the Mac valuable. Navigation controllers make sense on a device with a single full-screen view; they are wrong in a multi-window environment. Larger tap targets make sense on a touchscreen; they waste precious screen real estate on a Mac with a precision mouse.

## The 2025 Critique: Design as the Star

Simmons is not uncritical of Apple's own design direction. His 2025 essay "Tough Season in the Apple Fields" (inessential.com) took direct aim at the Liquid Glass design language introduced with macOS 26: "The UI has become the star, but the drunken star, blurry, illegible, and physically unstable." His concern was not aesthetic conservatism — it was that Apple had amplified existing legibility problems rather than solving them.

This is consistent with his view that good Mac design is functional before it is beautiful. The platform's visual traditions exist to serve productivity and clarity. When design starts to compete with content for attention, it has failed at its primary job.

## Design as Cultural Fit

Simmons understands design as a form of cultural expression. Mac users have a particular relationship with their computers — they use them for sustained work, they care about quality, they support indie developers and small businesses "passionately." Design that honors these values is not just aesthetically appropriate; it is commercially intelligent. Software that feels at home on the Mac finds an audience that rewards it.

He has also been consistently skeptical of aesthetic trends imported from other platforms. When iOS-style design elements arrive on the Mac — translucency, motion-first interfaces, navigation paradigms built for portrait phones — they degrade the experience for users who have spent years learning to work efficiently in a different idiom.

## Gap Note

Simmons has not written extensively about the visual design process — icon design, typography, color systems, or the particulars of visual hierarchy. His design thinking is architectural and idiomatic rather than graphic. For questions of visual craft, his perspective is most useful as a constraint-setter: he can tell you what a Mac app's design must not violate, even if he is not the right voice for deciding what it should look like.
