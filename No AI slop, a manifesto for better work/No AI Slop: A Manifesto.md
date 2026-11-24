# No AI Slop: A Manifesto

Source: https://www.slopmanifesto.com/  
Authors: speakers and attendees of AIE Code Summit 2026  
Date: the official page does not list a publication date. Dex Horthy presented it during his AIE Code Summit 2026 talk. A Hacker News thread about the page is dated 13 November 2026. The summit itself was widely reported as 10-12 November 2026.  
Verified: HTTP 200 on 23 November 2026

The page thanks Philip Kiely, Swyx, Lucas Meijer, Rebecca Bakels, Tejas Kumar, Natalie Serrino, Francisco Javier Arceo, Kent C. Dodds, Ankit Jain, Brandon Waselnuk, Mihail Eric, Justin McCarthy, Raz Berman Gold, Yacine Mahdid, Justin Poehnelt, Lauren Tan, and Kyle Mistele for contributions, and is open for additional signatures.

## Key points

The manifesto is framed as a counterpart to the Agile Manifesto, for a moment when AI helps write code, docs, plans, and messages. It states five values:

- Outcomes over output
- Understanding over speed
- Our own thinking over a model's first draft
- Better work over easier work
- Improving the system over patching the output

Beliefs include:

- AI is the most useful tool most of the authors have worked with, but a swarm of agents can produce more work in a single day than a person can review in a lifetime.
- Slop is when we put less effort into producing something than we ask the consumer to spend understanding it.
- Using AI does not necessarily make something slop. Slop happens when we pass AI output along without taking responsibility for the quality or the reader's experience.
- AI cannot replace human judgement; it can only amplify judgement, or the lack of it.
- Slop is asymmetric: the cost of producing a thousand-line PR or a ten-page doc is approaching zero, while the cost of reviewing it remains constant.
- Even before AI, slop in code proliferates when teams work around problems instead of solving them, and when tools lean heavily toward adding rather than subtracting.
- A lot of slop comes from pressure, as companies push people to redefine what is humanly possible.
- Slop compounds: the more of it sits in a knowledge base, chat, or code, the more the next agent reads and copies. The more slop flies around a team, the more people lose the will to fight it.

Resolutions include:

- Optimize for using human time and attention wisely.
- Fight slop because AI should make work better, not just easier.
- Optimize systems for eliciting human intent and for human understanding.
- Do your own thinking, and understand the problem before the work starts.
- Own the intent, taste, and consequences of what you ship, however much AI helps.
- When an agent wrote something you are sending, make that clear, and check the parts that matter before it goes out.
- When someone sends slop, tell them kindly and ask them to review it first.
- There will always be alpha in reviewing something. As models improve, people may stop reading most of the code, but may still review a plan, design, or result.
- Agent reviews, linters, and verifiers are useful but not sufficient. For now, still review at least some subset of the outputs; the subset depends on the stakes.
- What shipped, who is using it, and how it is helping them matters far more than lines of code, PRs merged, tokens spent, or the number of agents running in parallel.
- Unreviewed output is not always bad. One-shot prompts and vibe coding can be high leverage. Slop is bad when it undermines the outcome: a useful product, a maintainable system, or saving teammates time and energy.
- When a mistake shows up twice, improve the system and its guardrails. Anything a linter, type checker, or automated check can catch, let it catch.
- None of the authors has this fully figured out, and there is no single right answer.

## Takeaway

The manifesto is not a ban on AI. It asks people to keep responsibility for quality and for the reader's time, and to improve the system instead of just shipping more unreviewed output.
