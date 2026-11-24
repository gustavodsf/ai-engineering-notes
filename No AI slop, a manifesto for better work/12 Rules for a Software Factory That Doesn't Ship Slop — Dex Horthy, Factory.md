# 12 Rules for a Software Factory That Doesn't Ship Slop — Dex Horthy, Factory

Source: https://www.youtube.com/watch?v=-NFMsM2y0Vk  
Speaker: Dex Horthy, Factory (he says that until about a week before the talk he was CEO and co-founder of Human Layer, which had become part of Factory)  
Channel: AI Engineer (https://www.youtube.com/@aiDotEngineer)  
Date: 23 November 2026, 12:00:40 Pacific Time (17:00 BRT), from YouTube's published metadata  
Talk page / official conference title: "A software factory needs pressure in both directions" (https://ai.engineer/code/2026/talks/dexter-horthy)

This note is based on the spoken content of the uploaded talk (YouTube captions) and was cross-checked against the official AI Engineer machine-generated transcript of the same session. Caption errors remain possible. The conference stream uses a different YouTube id; Gustavo's source is the standalone talk upload above.

## Key points

- Horthy is not arguing against software factories. He says he likes them, and that a factory done well is "just good engineering": standardize the process, not only the output.
- He distinguishes forward pressure (what starts new work, such as routing feature requests or incidents into the factory) from back pressure (how agents can improve quality before a human has to look: agentic review and testing, CI, linters, and other checks). Both are needed. More forward pressure without back pressure just creates a larger pile of output.
- He presents 12 practices for software factories. He does not always number them clearly in the talk. The clearly stated ones include:
  - Start work automatically, and make sure low-hanging issues are already fixed before a human touches the result.
  - "Know your enemy": he argues that unattended models do not do a great job of maintaining and improving codebase quality over time. If the system has to last, keep understanding of the code.
  - Plan before you build, in proportion to expected pain (how likely a change is later, times how hard it will be to change). He would not argue with a model about a button color, but would spend care on a database schema.
  - Align visually (mockups, tables, charts) instead of reviewing only walls of text.
  - Help agents test their work with screenshots, browsers, videos, curl, or a real build-and-run loop.
  - Fight slop with deterministic rules and linters (he mentions TypeScript anti-slop rules and a Factory ESLint plugin, and quality rules from Slop Code Bench).
  - Not all unreviewed or rough work is bad: vibe coding, prototypes, and work behind a feature flag can be high leverage.
  - Give models a feature-flagging system so they can try things and measure them.
  - Compound over time: eval everything and learn from past sessions.
  - Unify the "forge": keep designs, decisions, and code close together, instead of pasting agent answers back and forth in Slack.
  - You cannot buy all of your verification. Some of it is specific to your team and your repos.
- He cites a Faros study on more unreviewed PRs and more incidents. The exact figures should be taken from the Faros report, not from the spoken rounding in the talk.
- He mentions Slop Code Bench, with new data he said was released that day from a University of Wisconsin lab, as a still-unsaturated benchmark of whether models can evolve a codebase over time. Spoken scores in the talk should be treated as approximate.
- He then walks through the No AI Slop manifesto, restates its values and resolutions, and asks people to read and sign it at slopmanifesto.com. His closing line is that the useful rule is to care about the work.

## Takeaway

A software factory only works if quality checks get stronger as generation gets cheaper. Plan in proportion to the cost of being wrong, let automated checks do the easy review, and keep humans on the parts that actually matter.
