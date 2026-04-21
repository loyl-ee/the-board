# Pieter Levels — On Safety and Ethics

## The Responsibility of Building Platforms at Scale

Levels does not write extensively about ethics in formal terms, but the question of what he owes to the communities his products have shaped has become increasingly visible as Nomad List's cultural footprint has grown. He predicted in 2015 that there would be 1 billion digital nomads by 2035 (levels.io/future-of-digital-nomads/). Whether or not that prediction holds, Nomad List was genuinely influential in popularizing the digital nomad identity and the specific cities — Chiang Mai, Bali, Lisbon, Medellín — that became nomad hubs in the 2014–2020 period.

This influence has come with criticism. Digital nomads have been widely blamed for contributing to gentrification, housing cost increases, and overtourism in the cities that Nomad List rated highly. Lisbon and Porto are frequently cited cases: as nomad populations grew, rents increased sharply, and local residents — earning median Portuguese wages of roughly €1,000/month against nomads earning minimum €2,800/month on special visas — found themselves priced out of their own neighborhoods.

## Levels' Documented Response to Gentrification Criticism

Levels has acknowledged this tension publicly. In a 2026 tweet, he reflected directly on the cultural moment Nomad List created circa 2014, recognizing that the platform contributed to a wave of migration to cities that were not previously equipped for or expecting it.

His position, as documented: he does not view the displacement effects as intentional or as something the platform creator can fully control, but he recognizes the platform's role in concentrating nomad populations in specific cities. His forward-looking response has been to advocate for immigration reform, nomad visas, and regulatory frameworks that integrate nomad populations more formally into local economies — rather than the shadow existence of long-stay tourists.

His Rebase project (2021), an immigration-as-a-service company helping remote workers obtain legal residency, can be read partly as a response to this critique: nomads should pay local taxes and participate in local economies as residents, not exploit tourist visa flexibility.

## AI Content Moderation

When building PhotoAI, Levels encountered the content moderation challenges inherent in AI image generation. He has discussed using Google Vision API to screen generated images before they are shown to users, and implementing prompt filters to prevent the generation of explicit or harmful content. "Google vision checks every photo before it's shown to the user." (Lex Fridman Podcast #440, 2024.)

This represents a practical safety architecture rather than a deeply theorized ethical framework — he is shipping a commercially successful AI product and implementing the safety measures required to operate it responsibly at scale without a trust-and-safety team.

## Privacy: An Evolving Position

The Nomad List community's early design — sharing location data, travel plans, and city preferences publicly among members — raised privacy concerns as the platform scaled. The model assumed nomads wanted to be findable by other nomads, but not all members shared that preference, and the data aggregated on the platform created potential risks (knowing where someone is, when they travel, where they stay).

Levels has not written a detailed public retrospective on Nomad List's privacy decisions, which is a genuine gap. His general position, inferred from blog posts and interviews, is that transparency and openness are goods — but that this default should be opt-in for user location data, not opt-out.

## The Solo Builder's Ethical Position

A recurring theme in Levels' writing is that indie makers occupy a distinctive ethical position: because they own their products entirely, are accountable directly to their users, and have no shareholders demanding growth at any cost, they have more latitude to make ethical choices. He argues in the MAKE book that "ethics as competitive advantage" — being honest with users, treating them fairly, and refusing extractive business models — is genuinely differentiated behavior in a market saturated with VC-funded companies optimizing for engagement over user welfare.

His "open startup" philosophy is an expression of this: radical transparency about revenue, user counts, and business health is itself an ethical stance. Users know exactly what they are paying for and what the business looks like.

**Gap note**: Levels' documented views on safety and ethics are practical and reactive rather than systematic or philosophical. He has not written a detailed ethical framework for platform responsibility. His responses to criticism have been public but brief. Anyone seeking a deep philosophical treatment of these issues from Levels will be disappointed — the documentation is thinner here than on business or product topics.
