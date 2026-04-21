# Ethan Mollick — On Design

## Scope and Honest Gap Note

Design is not Mollick's primary domain. He does not write about visual design, interface design methodology, or design systems. What he does have are strong views on the *design of AI interactions* — how to structure human-AI collaboration, what makes prompting systems usable, and how to design educational AI experiences that actually produce learning. These views are grounded in his research and classroom experiments rather than design practice.

## The Design of Effective AI Prompts

Mollick's work on prompting contains implicit design principles. In "Getting Started with AI: Good Enough Prompting" (November 2024), he describes the key structural elements of prompts that produce useful outputs:

- **Explicit output specification**: Rather than "summarize this for me," a well-designed prompt specifies the audience, format, tone, and purpose — "a report on remote learning appropriate for a regional Midwestern university" tells the AI what kind of output to produce, not just what topic to address.
- **Role definition**: Giving the AI a persona ("act as an experienced product manager reviewing this spec") shapes outputs by orienting the model's statistical patterns toward a specific knowledge domain.
- **Step-by-step structure**: "Chain of Thought" prompting — asking the AI to reason through a problem step by step before giving an answer — improves accuracy on tasks requiring inference. Mollick describes this as the prompting technique he uses most frequently.
- **Examples**: Providing samples of desired output style or format significantly improves consistency.

These are, in product terms, design decisions about the interface between user intent and AI output. Products that bake these structures into their AI features — rather than surfacing a blank text box — dramatically lower the barrier to useful outputs.

## Interface Design as AI Design

Mollick offered a pointed observation in the context of structured prompting: "If you have to engineer the prompt it might be time to look at the interface design. How AI interacts with humans is extremely important!" This positions good interface design as a substitute for prompt engineering. If users need to learn complex prompting techniques to get value from an AI feature, the feature's interaction design has failed.

## Design of AI Tutoring Systems

Mollick and Lilach Mollick's work on AI in education ("Assigning AI: Seven Approaches for Students," 2023) is the clearest example of deliberate AI interaction design in Mollick's body of work. They define seven structured AI roles — tutor, coach, mentor, teammate, tool, simulator, student — each requiring distinct prompting configurations that orient the AI toward a specific pedagogical function.

This is a design framework: different use cases require different AI configurations, and those configurations must be deliberately designed, tested, and documented. An AI positioned as a tutor asks questions and waits for student responses. An AI positioned as a simulator creates realistic practice scenarios. The same underlying model, configured differently, produces fundamentally different learning experiences.

## Centaur vs. Cyborg as Workflow Design

Mollick's centaur/cyborg distinction ("I, Cyborg," March 2024) is also a design framework for human-AI workflows. Centaur designs have clear task boundaries: AI handles X, human handles Y. Cyborg designs are more fluid, with AI integrated throughout. Each has appropriate use cases. Centaur designs are more predictable and auditable; cyborg designs can produce deeper integration and more creative outputs. A product team designing AI into a workflow should be explicit about which model they are building toward and why.
