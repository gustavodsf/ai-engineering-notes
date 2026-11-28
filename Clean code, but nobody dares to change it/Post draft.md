Clean code, but nobody dares to change it

ElemarJR tells a story many of us have seen. A module applies interest and rounds it down in one specific case. The code is new and the tests pass, but nobody remembers if the rule comes from a law, a regulation or a deal with a client. So nobody touches it. That is not technical debt, and calling it that sends the team to fix the wrong thing.

Margaret-Anne Storey's triple debt model gives each problem its own name:

1. Technical debt lives in the code.
The code lags behind what the team has learned. Ask: does it reflect what we understand today?

2. Cognitive debt lives in people.
The team can't explain what the system does or predict what a change will break. Ask: can someone other than the author explain it?

3. Intent debt lives in artifacts.
Goals, constraints and reasons were never written down. Ask: do we know why we decided this, and when to revisit it?

AI makes this sharper. Storey notes it can reduce technical debt while speeding up the other two. A refactor by an agent can clean the code and leave nobody understanding it, or knowing why. ElemarJR's advice: when all three show up, pay the why first, then the understanding, and the code last, where AI helps most.

I use Claude and Codex every day and work with agents that open and review PRs. The code arrives ready, but the understanding only comes if someone goes after it. In ledger and money code, the reason behind a rule matters as much as the rule, so a change to a rule should carry its why.

Which one hurts your team most right now: the code, the understanding, or the missing why?

Sources:
https://youtu.be/9YG_Wt-8_x8
https://arxiv.org/abs/2603.22106
https://martinfowler.com/fragments/2026-04-02.html

More detail in:
https://github.com/gustavodsf/ai-engineering-notes
https://github.com/gustavodsf/ai-engineering-notes/tree/main/Clean%20code%2C%20but%20nobody%20dares%20to%20change%20it

#SoftwareEngineering #SoftwareArchitecture #AIEngineering #TechnicalDebt
