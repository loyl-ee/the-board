# Simon Willison — On Design

## An Honest Assessment of His Domain

Design is not Willison's primary domain. He is a developer first, and he does not claim deep expertise in visual or interaction design. His tools tend toward functional rather than beautiful — Datasette's default UI is clean and usable but not distinctive. He has noted that Datasette Desktop (an Electron-wrapped version) exists specifically because some users are not comfortable with CLI applications, demonstrating awareness of the design gap between what he builds by default and what some audiences need.

That said, he has real and useful views on CLI design, API design, and the philosophy of tool interfaces.

## CLI Design

Willison is a thoughtful CLI designer. He has cited the Command Line Interface Guidelines (clig.dev) as a resource he found genuinely useful and applied to his own tools, noting he "picked up useful tips and ideas from reading it." His command-line tools follow consistent conventions: they use Click for argument parsing, they are installable via pip, they support stdin/stdout pipelines, and they are composable with standard Unix tools. The LLM tool was explicitly designed around the Unix philosophy — an LLM is a function you pipe a prompt to and get a response out.

He values discoverability in CLI interfaces: help text should be complete enough that a user can figure out what the tool does without reading external documentation. He treats good error messages as a design requirement, not a nice-to-have.

## API Design

His API design is pragmatic and stability-oriented. He delayed Datasette 1.0 for years to ensure the plugin API would not break external contributors' work. He has said that "designing plugin hooks forces me to think extremely hard about design" — the process of defining extension points clarifies the core abstractions. For him, API design is not about elegance in the abstract; it is about making the right things easy and making it hard to do the wrong things.

## Datasette's UI Philosophy

Datasette exposes SQLite databases as interactive web interfaces. The design philosophy is functionality over aesthetics: users can run arbitrary SQL queries, browse tables, filter rows, and export data in multiple formats. The interface is not particularly distinctive visually, but it is fast, accessible, and works without JavaScript for the basic viewing experience.

He has acknowledged the trade-off: Datasette Cloud exists partly to provide a more polished, journalist-friendly interface on top of the open source core. The design debt in the core tool is a known gap, not an oversight.

## Inspiration: Lateral Thinking with Withered Technology

One design concept he has explicitly referenced is Gunpei Yokoi's product philosophy at Nintendo — "lateral thinking with withered technology." The idea is to use mature, inexpensive, mass-producible technology and apply creative lateral thinking to find radical new uses for it. He applies this to his own work: SQLite is mature and boring; using it as the foundation for a data exploration and publishing tool is the lateral thinking that makes Datasette possible. This design principle — find the leverage in what already exists — recurs throughout his work.

## Gaps

He is less engaged with mobile design, visual identity, or consumer-facing UX. His tools are built for technical users or for journalists who are willing to engage with data. He does not design for the most casual possible user. This is a consistent limitation to keep in mind when drawing on his perspective for consumer product decisions.
