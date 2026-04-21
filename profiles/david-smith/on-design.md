# David Smith — On Design

## HIG as Foundation, Not Ceiling

Smith's primary design rule, stated explicitly in his Design Diary, is: follow Apple's Human Interface Guidelines. This is Rule 1, and he allows no exceptions. For a solo developer, this makes both practical and aesthetic sense: Apple's guidelines represent years of design research applied to the specific constraints of iOS, and building against them creates user confusion and rejection. Working within the guidelines means users arrive with correct mental models of how the app will behave.

But Smith treats the HIG as a foundation rather than a ceiling. Within Apple's design language, he pursues careful craft: custom SF Symbols, thoughtful typography choices, animation that rewards attention, and visual details that distinguish his apps from commodity implementations of the same APIs.

## Widget Design and the Aesthetics Problem

Widgetsmith forced Smith to develop a specific design sensibility that most iOS developers never encounter: designing for the home screen as a canvas. Widgets are always visible, often in groups, and persist in the peripheral vision of users for hours every day. They must look good not just in isolation but in combination with other widgets, with wallpapers, and across the dozens of visual contexts that different users create.

His approach to this problem evolved substantially between Widgetsmith's launch and its subsequent versions. The original design treated aesthetic customization as one configuration option among many. After the TikTok viral moment revealed a user base motivated primarily by visual self-expression, he redesigned the product's entry point around themes — curated, coherent visual starting points — while preserving full granular customization for users who wanted it.

He releases seasonal collections of new themes at the start of each season, describing this as providing "a fresh starting point for updating iPhone aesthetics in an inspirational rather than prescriptive manner." He has worked with professional type designers to offer font options that make home screens "look sharp," and partnered with designers for geometric and seasonal overlay artwork.

## The Design Diary Practice

Smith maintains a public Design Diary at david-smith.org documenting his design process in detail. The purpose, he explains, is not primarily to teach — it is to think. He cites the Field Notes slogan: "I'm not writing it down to remember it later, I'm writing it down to remember it now." Articulating a design problem forces precision that vague visual intuition cannot achieve.

His iterative process involves maintaining a running "punch list" in Reminders — an unfiltered inbox for every critique and idea that emerges while using an app in actual development. He then periodically processes this list, either fixing, building, or discarding items. He emphasizes the importance of specificity in these notes: "Misaligned bar header" becomes useless within days; "The top header in the settings tab looks too far to the right compared to the contents text" remains actionable.

## Accessibility as a Design Value

Accessibility features — Dynamic Type support, VoiceOver compatibility, sufficient color contrast — appear consistently in Smith's Design Diary as requirements, not optional enhancements. His apps scale correctly across all Dynamic Type sizes, which he tracks analytically: a 2026 blog post measured that 18% of Widgetsmith users had set their text size to something larger than default, a higher proportion than Display Zoom adoption (1.9%). These are not abstract statistics to him — they represent real users who will be poorly served by an app that ignores the setting.

## Kindness in Interface Design

A recurring theme in Smith's design writing is what he calls "kindness" in interfaces. This manifests as restraint in the emotional signals an app sends: Sleep++ does not aggressively signal failure if sleep was poor, because sleep quality is often outside a user's control. Pedometer++ celebrates goal achievement with confetti, but presents shortfalls without shame. He designs for the full range of user experience, including the users for whom the tracked metric is a source of difficulty rather than pride.
