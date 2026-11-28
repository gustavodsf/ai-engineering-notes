# From Technical Debt to Cognitive and Intent Debt: Rethinking Software Health in the Age of AI

Source: https://arxiv.org/abs/2603.22106 (published version: ACM Queue, https://queue.acm.org/doi/10.1145/3807966 — blocks automated requests, so the arXiv copy was read)  
Author: Margaret-Anne Storey, University of Victoria  
Date: submitted 23 March 2026, last revised 6 April 2026 (v4)  
Verified: arXiv page and PDF load (HTTP 200), full text read on 27 November 2026

## Key points

- Proposes a Triple Debt Model: technical debt in code, cognitive debt in people, intent debt in externalized knowledge. "Technical debt makes systems harder to change. Cognitive debt makes systems harder to understand. Intent debt makes it difficult to know what the system is actually for."
- Opens with a student team that hit a wall in week 8: simple changes broke things, nobody could explain design decisions, the shared theory of the system (Naur 1985) had fragmented.
- Generative AI may reduce technical debt (refactoring, test generation, review) while accelerating cognitive and intent debt. The code may work and be well architected, but the team may not understand it or remember why it was built that way.
- Cognitive debt is a team-level property, different from cognitive load and from individual "comprehension debt". It is not new; what is new is the rate at which the gap accumulates and the difficulty of detecting it with AI-assisted development.
- Intent debt: absence or erosion of explicit rationale, goals and constraints, which both humans and AI agents need to evolve the system.
- Mitigations: walkthroughs, retrospectives and knowledge transfer; intent-first workflows (ADRs, specs, domain models, acceptance criteria); resisting the automation of understanding (AI-generated docs can give the appearance of understanding without building it); monitoring all three layers together.
