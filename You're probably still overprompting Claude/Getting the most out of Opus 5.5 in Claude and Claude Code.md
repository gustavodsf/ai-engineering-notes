# Getting the most out of Opus 5.5 in Claude and Claude Code

Source: https://claude.dev/blog/getting-the-most-out-of-opus-5-5/  
Author: Addy Osmani  
Date: September 22, 2026  
Note: with thanks to Molly Vorwerck for reviewing, as stated on the page.

## Key points

- The guide covers how to prompt Opus 5.5, steer a long run, and check results in Claude apps and Claude Code. Opus 5.5 works for longer on its own, reports plainly what it did, and thinks before every reply.
- Try this first: hand over the whole task and say what "done" looks like and when it should stop and ask; delete "think carefully" lines; when a long run ends, read what it needs from you first.
- Give the whole task in one message and name the finish line, such as "the tests pass" or "every endpoint is migrated." Opus 5.5's biggest gains versus prior Opus models are on multi-step work, and early testers had it run long coding tasks for hours with little oversight. A clear finish line tells it when it is done.
- Remove "think carefully," "think step by step," and similar lines from prompts and saved instructions. Opus 5.5 always thinks before it replies and decides how much. In Anthropic's testing in a chat product, removing a "think carefully" line made replies start sooner, with no clear drop in quality. For a quick answer, say "Answer directly." To change how much it thinks in Claude Code, change effort.
- You can add a follow-up while a run is in progress instead of restarting. Runs are longer now, so a restart costs more.
- For design work, list specific styles you do not want. A general "avoid a generic look" mostly swaps one default for another.
- In Claude Code, put a short CLAUDE.md rule about when to stop and ask versus when to keep going. Opus 5.5 sometimes stops to report or ask "Want me to continue?" instead of proceeding. A keep-going rule means fewer stops, so keep a check before anything destructive, and keep permission prompts on for destructive commands. For pair programming, you can instead ask for a one-line plan before it starts and a short recap at the end.
- For an audit, migration, or review across a large codebase, ask Opus 5.5 to split the work across subagents and check each result before accepting it.
- For a long run, keep the task list in a file (for example TASKS.md) and update it as you go. A file survives context summarization and is easier to read than scrollback.
- When a long run ends, first look for anything Claude is waiting on you for, then read the rest of the summary. You can specify a summary format in CLAUDE.md.
- Ask Opus 5.5 to review a diff or pull request before a person does. One early tester said Opus 5.5 at its lowest effort caught more bugs than Opus 5 at high effort, with fewer false alarms.
- For research and analysis, ask it to mark what it could not confirm and where it looked.
- In Claude apps, attach charts, diagrams, screenshots, or slides instead of retyping numbers. Ask it to check long documents for contradictions. When you want a spreadsheet or document, ask for the finished file, not an outline.
- In a long project chat, a follow-up can be slow because the model sometimes re-examines earlier answers. You can add an instruction to treat earlier answers as settled, but leave that out of long analysis where a later step may reveal an earlier mistake.
- Opus 5.5 launched with Fable-level bio and cyber safeguards. Most flagged messages move to an older model. You can switch back with the model picker or `/model`, and you can change whether the product switches automatically. Do not ask the model to reproduce its internal reasoning in the reply; that can be declined. Ask for a short explanation of the approach instead.
- Fast mode is a research preview in Claude Code for back-and-forth work. It is the same model, arrives sooner, needs extra usage turned on, and costs more per token than standard mode.

## Takeaway

Prompt Opus 5.5 with the whole task and a clear definition of done, remove thinking-style filler written for older models, and invest your effort in steering long runs and checking the result, including an automated review pass before a human looks.
