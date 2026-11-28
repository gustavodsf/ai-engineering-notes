# Yagni

Source: https://martinfowler.com/bliki/Yagni.html  
Author: Martin Fowler  
Date: 26 May 2015 (older, but the clearest statement of the "cost of carry")  
Verified: HTTP 200, full text read on 27 November 2026

## Key points

- Yagni ("You Aren't Gonna Need It"): don't build capability you only presume you will need.
- Four costs: cost of build, cost of delay (not building something more valuable), cost of carry (the extra complexity makes every later change harder and slower until the code is removed, plus the cost of removing it), and cost of repair.
- Footnote: Kohavi et al. analysed features built and deployed at Microsoft and found that, even with careful up-front analysis, only one third improved the metrics they were designed to improve. Fowler uses it to say the odds a presumptive feature is unnecessary are at least two thirds.
- Yagni only works if the code stays easy to change: refactoring, self-testing code and continuous delivery are enablers, not violations.
- Note: the article is about features not yet needed; the post applies the same "cost of carry" idea to shipped features nobody uses.
