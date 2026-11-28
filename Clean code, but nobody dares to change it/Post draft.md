Clean code, but nobody dares to change it

You can have clean code and passing tests, and still nobody wants to change a business rule. In a recent video, ElemarJR argues that this is often not technical debt, and that the wrong name sends the team to fix the wrong thing.

Imagine a billing service that skips invoices for paused accounts. Product asks: should we start invoicing them? Nobody can say how much revenue that holds back, or why the rule exists: a finance policy, a sales courtesy, or an old bug fix.

Margaret-Anne Storey's triple debt model gives each problem a name.

1. Technical debt lives in the code. The same skip might exist in checkout, invoices and refunds. Does the code still reflect what we understand today?

2. Cognitive debt lives in people. Everyone can read the line, but nobody can predict the effect of turning it off. Can someone other than the author explain it, and forecast what a change would break?

3. Intent debt lives in artifacts. This is the missing "why": we don't know if the rule still needs to exist. The fix is a short decision record, written when you decide, or a new one if the original reason is gone.

AI makes this sharper. An agent can merge those three implementations in minutes, and the debt looks paid. Storey notes that AI can reduce technical debt while speeding up the other two. That payment is counterfeit if nobody verified the behaviour, the understanding or the why.

ElemarJR's advice, when all three show up: pay the why first, then the understanding, and the code last, where AI helps most.

I use Claude and Codex every day, and I work with agents that open and review PRs. At Inoa and Dock I worked on ledger and money systems, where a rule without its reason is hard to change safely.

Which one hurts your team most right now: the code, the understanding, or the missing why?

Sources:
https://youtu.be/9YG_Wt-8_x8
https://arxiv.org/abs/2603.22106
https://martinfowler.com/fragments/2026-04-02.html

More detail in:
https://github.com/gustavodsf/ai-engineering-notes
https://github.com/gustavodsf/ai-engineering-notes/tree/main/Clean%20code%2C%20but%20nobody%20dares%20to%20change%20it

#SoftwareEngineering #SoftwareArchitecture #AIEngineering #TechnicalDebt
