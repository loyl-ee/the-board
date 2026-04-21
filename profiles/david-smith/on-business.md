# David Smith — On Business

Business strategy is perhaps the domain where David Smith has been most consistently public and most analytically precise. Across 15 years of blogging, two podcasts, and multiple interviews, he has documented in unusual detail how he thinks about the economics of indie iOS development.

## Foundation Income and the Portfolio Model

Smith's financial architecture has always depended on a portfolio of apps rather than a single product. The first anchor was Audiobooks (2009), which generated steady income from downloads and later advertising. This foundation income funded experimentation — the dozens of apps that failed, and the eventual development of Pedometer++, Sleep++, and eventually Widgetsmith.

He has described thinking about his business in terms of revenue per day as a management tool: "I tend to think of my app business in terms of revenue per day, breaking it down to that level to keep a close eye on it and know how well or poorly I'm doing." Tracking at that granularity makes trends visible before they become crises.

The portfolio approach is both a risk management strategy and a creative one. No single app needs to be a hit. Each app can serve a specific user need. If Apple sherlock one, another may benefit. If one category declines, another may hold. The tradeoff is attention: managing multiple apps as a solo developer means none of them ever gets a full team's focus.

## The Collapse of Paid Apps

Smith has written directly about the structural shift in App Store economics. At some point in the mid-2010s, paid app revenue became "a vanishingly small proportion" of his income, and advertising grew to comprise nearly 80% of total revenue. He was explicit that this change was market-driven, not a change in his own values: "the change has mostly been in the App Store market, rather than in my own attitudes."

His response was pragmatic adaptation. He followed consumer behavior rather than lecturing users about why paid software was the right model. He states: "the less I fight back with anachronistic ideas about how software should be sold, the more sustainable a business I have."

## Freemium and Subscription Evolution

Widgetsmith launched in 2020 as a free app with no immediately visible monetization. When the app went viral and reached the top of the App Store, Smith needed to convert scale into revenue quickly. He implemented a subscription model — approximately $1.99/month or $19.99/year for Widgetsmith Premium — and chose RevenueCat to manage subscriptions rather than building a custom backend.

He has described his rationale for using RevenueCat bluntly: "My homegrown solution would have not been able to scale as quickly or as cleanly as their system did." At peak virality, Widgetsmith was processing hundreds of new subscribers per second. RevenueCat handled this without downtime. His verdict on the tool reflects a broader philosophy: "The best thing I can say for RevenueCat is that I don't think about it. It's always worked."

Widgetsmith Premium offers weather and tides data sources for widgets, along with exclusive widget styles. The core app remains free. This is a conscious decision: the free tier drives organic discovery and word-of-mouth sharing (people share screenshots of their home screens, which advertises the app); the premium tier captures value from engaged users who want more.

## Surviving Algorithm Changes

Smith has launched apps — including Emoji++ — that were made effectively irrelevant by Apple incorporating similar functionality into iOS itself, with no warning and no recourse. His response to being "sherlocked" is instructive: he analyzes whether Apple's native version creates a larger category (in which case the third-party app may benefit from the attention) or whether it eliminates the reason to seek alternatives (in which case the app may be unsalvageable). He has experienced both outcomes and treats sherlocking as a platform risk to be anticipated rather than a grievance to be nursed.

More broadly, he advocates staying close to Apple's latest APIs and releasing on day one of new OS versions. This serves two purposes: it signals to Apple's editorial team that the app is actively maintained (improving featuring prospects), and it positions the app to capture users who are excited about new platform features before competitors have caught up.

## Customer Support at Scale

One of Smith's most practically detailed public discussions concerns scaling customer support as a solo developer. Drawing on his experience with Pedometer++ and Widgetsmith, he developed a three-tier funnel:

1. App design that minimizes the need for support in the first place
2. Self-service FAQs and embedded video tutorials (remotely updatable without an App Store release)
3. Direct email as the last resort

The data from his Pedometer++ v5 launch measured this: 82,000 people watched video tutorials, 4,214 got answers from FAQ pages, and 259 sent emails — a roughly 20x falloff at each tier. Only 0.5% of active users ever contact support directly. He cautions developers against over-optimizing for the vocal 0.5% at the expense of the silent 99.5%.

## Avoiding Servers

A consistent theme across Under the Radar and his blog is the maxim: do not run servers unless absolutely necessary. Server infrastructure creates ongoing maintenance costs, security obligations, scaling headaches, and dependencies that outlast any individual app's revenue cycle. For Widgetsmith's shared photo widgets, Smith used iCloud's shared albums rather than building a custom backend — achieving the functionality without the liability.

He frames this as a focus question: "Features like syncing, account management, and backups become expected immediately upon release. They deserve minimal investment relative to unique, visible features." His device-first philosophy leverages the computational power of modern iPhones and Apple's own infrastructure (CloudKit, HealthKit, WeatherKit) to avoid backend complexity entirely.

## Going Indie: The Financial Foundations

Under the Radar episodes 115 and 116 ("The Going Indie Spreadsheet") provided a detailed roadmap for developers considering the transition to independence: business entity setup, taxes, income requirements, health insurance, retirement planning, and professional services. The core argument was that going indie is a calculable decision, not a leap of faith — by building a detailed financial model of actual costs and required income, developers can make the transition a deliberate choice rather than a desperate one.
