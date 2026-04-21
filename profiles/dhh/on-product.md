# DHH — On Product

## Software With a Spine

Hansson's product philosophy flows directly from his belief that software should have a point of view. A product without opinions is not a neutral product — it is an indecisive one. The lack of conviction in a product shows up as feature sprawl, inconsistent UX, and the slow accumulation of options that nobody asked for and few people use.

## The Rails Doctrine: Convention Over Configuration

Ruby on Rails is the clearest expression of Hansson's product thinking. The central principle — convention over configuration — is a product decision disguised as a technical one. Instead of requiring developers to explicitly configure every aspect of their application, Rails establishes sensible defaults. If you follow the conventions, everything works. If you deviate, you bear the cost.

This is opinionated software at the framework level. Rails does not ask what kind of application you want to build and adapt itself accordingly. It assumes a certain kind of application and makes that kind extraordinarily easy to build. Applications that don't fit the mold are harder to build in Rails — and that is intentional. The framework's point of view is the product.

Hansson describes Rails as "omakase" — the Japanese restaurant concept of leaving the choice entirely to the chef. When you order omakase, you trust the chef's judgment rather than selecting each element yourself. Rails curates an integrated stack: database access, view rendering, routing, testing, all chosen and harmonized. The developer doesn't assemble these pieces; the framework has already decided.

The Rails Doctrine (published on rubyonrails.org) lists nine explicit values: optimize for programmer happiness, convention over configuration, the menu is omakase, no one paradigm, exalt beautiful code, provide sharp knives, value integrated systems, progress over stability, and push up a big tent. Each is a product decision with consequences — a choice about who Rails is for and what it rewards.

## Basecamp: The Product That Never Stopped Being a Product

Basecamp has been rebuilt three times (Basecamp Classic, Basecamp 2, Basecamp 3), and each version was a deliberate product statement rather than an incremental feature update. Hansson and Fried have described the company's approach as building products for the way they themselves want to work — not for the broadest possible market.

Basecamp does not try to do everything a large enterprise project management suite does. It lacks some features that competitors prominently advertise. This is not an oversight. It is the product's argument: that most work is simple enough that elaborate tooling adds friction rather than removing it. Small teams with one shared place for messages, to-dos, docs, and schedules need nothing more.

The Majestic Monolith (a term Hansson coined) describes the architectural expression of this product philosophy: a single, unified application rather than a distributed system of microservices. For Basecamp 3, the monolith serves web, iOS, Android, macOS, Windows, and email simultaneously. A team of roughly 12 programmers maintains the full product. That is only possible because the architecture is designed for human comprehensibility, not theoretical scalability.

## HEY: Opinionated Email From First Principles

HEY (launched June 2020) is the most publicly controversial expression of Hansson's product philosophy. The premise was that email, as inherited from decades of convention, was broken — not because of spam filters or interface clutter, but because the fundamental model was wrong. Email allowed anyone who had your address to command your attention. HEY reversed that.

The Screener requires approval before a new sender enters your inbox (called the Imbox — only things that need your immediate attention). The Feed handles newsletters and low-priority correspondence. The Paper Trail captures receipts and notifications. You cannot CC yourself into a conversation unless explicitly invited. Replies go to a separate stack.

These decisions are not options. They are the product. HEY does not let you turn off the Screener and behave like Gmail. That rigidity drew consistent criticism — and Hansson's response was consistent: if you want Gmail, Gmail exists. HEY is built for people who share its vision of what email should be. The product's point of view is its value proposition.

## Sources
- [The Ruby on Rails Doctrine](https://rubyonrails.org/doctrine)
- [Make Opinionated Software — Getting Real](https://basecamp.com/gettingreal/04.6-make-opinionated-software)
- [The Majestic Monolith — Signal v. Noise](https://signalvnoise.com/svn3/the-majestic-monolith/)
- [HEY email](https://www.hey.com/)
- [Building HEY with Hotwire — Full Stack Radio #151](https://fullstackradio.com/151)
