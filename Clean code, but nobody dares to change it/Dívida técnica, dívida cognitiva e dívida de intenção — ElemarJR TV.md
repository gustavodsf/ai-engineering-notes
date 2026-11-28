# Dívida técnica, dívida cognitiva e dívida de intenção

Source: https://youtu.be/9YG_Wt-8_x8  
Channel: ElemarJR TV (video in Portuguese)  
Published: 25 November 2026 · Duration: 26:01  
Verified: page loads (HTTP 200) and full transcript read on 27 November 2026 (transcript obtained through a machine-translated English version of the page's transcript; description and chapters read in Portuguese).

## Chapters

00:00 Clean code, but nobody wants to touch it · 02:55 The original metaphor of technical debt · 07:28 What the term became · 09:57 Cognitive debt: when understanding is lost · 14:00 Intent debt: when the "why" disappears · 18:42 How the three debts feed each other · 20:58 What AI changed · 23:52 Three questions to diagnose your system

## Key points

- Opening case: a system with clean code, good architecture, passing tests and no static-analysis alerts that nobody dares to change. In a company he consults for, a module applied interest and rounded it down in a specific situation. Tests proved the rule was applied correctly, but nobody remembered if it came from a legal requirement, a regulation or a past agreement with the client.
- Technical debt, original meaning: Ward Cunningham (1992, portfolio management system for finance) used debt to explain code that lags what the team has learned about the domain. Paying it means changing the code to express the current understanding. In a 2009 video he said he was never in favour of writing bad code. Bad code is not the debt, it is what prevents paying it.
- Fowler's quadrants (deliberate/inadvertent × prudent/reckless) are the modern reading. The metaphor was then stretched to cover duplication, outdated libraries, missing tests, disliked architecture.
- Running example: a recurring-revenue calculation that exists in four places, one outdated (technical debt). After merging, the calculation excludes suspended contracts and nobody can say how much revenue that removes (cognitive debt). Then sales asks to include them and nobody knows whether the exclusion came from an audit, an accounting rule or a departed director (intent debt).
- Cognitive debt (from Storey, grounded in Peter Naur's 1985 "Programming as Theory Building"): how much a system does that a team cannot explain. It lives in people. Not the same as cognitive load. Signs: fear of changing code, "only X understands it". Direct test: ask someone other than the author to explain the idea behind a piece of code. Paid by rebuilding understanding: pairing, reviews with questions (not only approvals), tests that explain expected behaviour. Documentation helps remember but does not replace understanding.
- Intent debt: missing goals, constraints and reasons recorded outside people's heads. Lives in artifacts. Two symptoms: keeping structures out of fear, or removing a rule that looked useless and breaking a guarantee (example: raising a 10 MB upload limit to 100 MB crashed an antivirus service sized for 10 MB). Paid with explicit records of decisions (ADRs, Michael Nygard), written when the decision is made. If the original reason is lost, make a new decision and record it with today's context.
- The three debts feed each other (technical → cognitive → intent → more technical, e.g. a fifth copy of the calculation), but this is a common pattern, not a law. Not every debt must be paid now: compare the cost of paying against the interest and risk.
- AI: producing code and building understanding can now be done separately. Four activities: produce, verify, understand, justify. Finishing the first does not mean the other three are done. Warning about "counterfeit payment": asking an AI to refactor, the code looks cleaner, metrics improve and technical debt seems paid, without verifying behaviour, understanding and decisions. AI can also help: reconstruct flows, compare implementations, challenge an expert to explain, draft an ADR from a discussion, always with someone validating.
- When all three appear together, suggested order of investigation: intent first, then understanding, then code. Not a rigid rule (if month-end is tomorrow, fix the number first).
- Three closing questions: Does the code represent what we understand today? Can we explain the system's behaviour and predict the effect of a change? Can we justify decisions and recognise when they should be revisited?
- Closing line: a company can own all its code and still have lost the ability to evolve it; its software assets are also the understanding it preserves and the decisions it can make.
