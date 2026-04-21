# DHH — On Design

## Design as Removal

Hansson's design philosophy is inseparable from his product philosophy: the primary act of design is removal, not addition. He has argued consistently that the hardest and most valuable design decision is deciding what not to include. Addition is easy — a team can always generate more features, more options, more settings. Subtraction requires conviction about what the product actually is.

This is not a novel position in design discourse (Dieter Rams said it, Steve Jobs said it), but Hansson applies it operationally. The question he asks is not "what else could we add?" but "what is the minimum that makes this irreplaceable?" That question has concrete consequences: HEY launched with far fewer features than Gmail, Basecamp has fewer fields and views than competing project management tools, and Rails comes with conventions that eliminate entire categories of configuration decisions.

## Functional Beauty

Hansson values aesthetic quality in software, but his aesthetics are inseparable from function. In the Rails Doctrine, he lists "exalt beautiful code" as one of nine core values — and he means this literally. Code that is elegant, readable, and clear is not just pleasanter to write; it is genuinely better software because it can be understood, changed, and maintained by humans. Complexity that has no functional purpose is ugly by definition.

This extends to interfaces. He has spoken approvingly of interfaces that make the right action obvious, that don't require explanation, and that don't fill the screen with options the user will never use. The Imbox metaphor in HEY — a visual inbox that only shows things needing immediate attention — is a design statement: attention is scarce, and the interface should honor that.

## What Design Is Not

Hansson is skeptical of design as styling or branding exercise. In his framework, a product that has sophisticated visual polish but confusing structure is not well-designed. Design is the structure of the thing — the decisions about what exists, what is hidden, what is primary, and what is not possible. The visual layer either communicates those structural decisions clearly or it obscures them.

He has noted limited documented views on pure visual design craft (typography, color, motion design) — his documented opinions focus on structural and interaction design rather than visual aesthetics per se.

## The Cost of Complexity

In Hansson's view, complexity is the primary design enemy. Every option added to a settings screen is a decision the user now has to make. Every feature added to a product is a surface that can break, a concept that must be learned, and an assumption about what users want that may be wrong. He has quoted approvingly from the adage "perfection is achieved not when there is nothing more to add, but when there is nothing left to take away" — though his application of it is characteristically blunt: most software has not even begun to approach perfection in this sense because most software has spent its entire life adding.

## Sources
- [The Ruby on Rails Doctrine](https://rubyonrails.org/doctrine)
- *Getting Real* — 37signals, 2006
- *Rework* — Jason Fried and David Heinemeier Hansson, 2010
- [HEY email design overview](https://www.hey.com/)
