# Linus Torvalds — On UX

## Honest Limitations

Torvalds uses Linux at the command line. He uses a minimal text editor (uemacs, his own maintained fork of MicroEMACS). He does not use graphical desktop environments habitually, and his home office workflow is radically different from any consumer user. He has acknowledged this distance in multiple interviews, and it is relevant when weighing his opinions on user experience questions.

His primary domain of thought about interfaces is developer tooling — specifically, kernel interfaces and version control systems — where the "users" are engineers who are willing to invest time learning powerful tools. Consumer UX, in the sense of designing for people with no technical background or patience for learning curves, is largely outside his experience.

## What He Thinks Good Tools Do

Even within his limitations, Torvalds has articulated a coherent view of what makes tools excellent for their actual users. The core principle: tools should be honest about what they are. A tool that simplifies by hiding the underlying model is making a tradeoff — easier first contact at the cost of confusion when the hidden complexity surfaces.

His defense of Git's steep learning curve fits this view. Git's interface is complex because the underlying model — distributed, content-addressed, branch-aware — is genuinely complex. A simpler interface would present a simpler model, which would be a lie. When the user eventually encounters a merge conflict or a detached HEAD, a simpler interface leaves them with no mental model for what to do. Git's interface, while forbidding, teaches the model as you use it. This is a specific UX philosophy: build the model, then expose it.

## On Git's Interface and Learning

In a 2005 Google Tech Talk on Git, Torvalds acknowledged that the interface was not going to win any friendliness awards. He described his design priorities as performance, correctness, and distribution — interface came after. Junio Hamano, who took over as Git's maintainer shortly after its creation, has done most of the work of making Git's interface more learnable over time, and Torvalds has credited him for it.

Torvalds' view on this, inferred from his public statements, is that a tool with a sound model is learnable; a tool with a broken model is not — the interface is secondary. In his 2020 Tag1 Consulting interview, he described selecting Hamano as Git's maintainer partly because Hamano had the "good taste" to solve problems cleanly, which includes interface problems.

## The GNOME Criticism

Torvalds has been publicly critical of GNOME, the Linux desktop environment. In a December 2005 post to the GNOME usability mailing list, he wrote: "I personally just encourage people to switch to KDE. This 'users are idiots' mentality of Gnome is a disease." The specific complaint was about GNOME's design philosophy of hiding options and simplifying interfaces — he found this condescending to users and limiting in practice.

This is a meaningful signal: Torvalds' UX preference runs toward giving users capability and trusting them to learn, rather than making initial experience easier by removing power. This is consistent with the rest of his worldview, but it is a preference that applies most naturally to developer tools and technical users, not to general consumer software.
