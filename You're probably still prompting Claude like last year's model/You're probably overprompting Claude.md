# You're probably overprompting Claude

Source: https://x.com/addyosmani/article/2115688494865465370  
Author: Addy Osmani  
Date: October 29, 2026

## Key points

- Newer models require less prompting than most people still use.
- For Opus 5.5, give Claude a single prompt with a clear goal and a way to verify that the goal was achieved, then let it work. Start with `/effort medium` and adjust as needed.
- If you do not yet know what you are trying to do, ask Claude to interview you until it could write a spec. Start a new session and use that spec to build what you want.
- Claude will stop on its own when it believes it is done.
- If Claude can run a check that is pass/fail or a number to beat, and can read the report, it can keep going without you watching.
- For long background tasks, `/goal` lets you specify a condition that a separate model checks after every turn.
- Recent Claude Code versions use auto mode as the default for interactive terminal sessions. A classifier analyzes Claude's actions instead of relying on the usual permission prompts. This is not a guarantee of safe behavior, and neither is blindly approving every prompt. When Claude reports back, ask it to show the command and output or a screenshot.
- For models like Claude Opus 5 and Claude Fable 5, over 80% of the Claude Code system prompt was removed with no measurable degradation of its coding evals.
- When a new model such as Opus 5.5 comes out, try the same experiment on your own instructions: remove some, then add back only those the model misses. The `/doctor prompt-audit` command flags instructions written for older models.
- Claude delegates to subagents on its own, so you rarely need to ask. Ask only for substantial, standalone work such as long audits or migrations, which Opus 5.5 can split across parallel subagents. For small jobs, subagents multiply cost and latency. They can parallelize work or provide a second opinion, but they do not, by default, make things smarter.
- For agents you build, a single agent with skills can outperform a subagent design on quality, often at lower cost and latency, from what Osmani has seen.
- Use Claude cloud sessions when you want to shut your laptop. Start one from claude.ai/code, the Claude app, or `claude --cloud`. Cloud sessions run in a separate VM with a fresh clone of your repo, so push any commits first. Keep a session local if the task needs resources only available on your machine.
- Parallel sessions only pay off once a single session can finish without you.
- Projects in Claude Code (public beta on Pro and Max) are one long-running chat that does most of the project management: you paste in issues and jobs, Claude creates a separate thread (usually a cloud session) for each and runs them in parallel, applies your instructions to new threads, and shows an Overview of completed tasks, ready PRs, and items pending your input. Without a project, you are the manager of multiple sessions.
- Review still matters. On the Claude Code team, most changes are reviewed and fixed by Claude at least once before a human is asked to look. Options include Code Review on Team and Enterprise plans, the lighter `/code-review` (a subagent that has not seen the conversation), or a new session given the spec and told to ignore stylistic issues.
- Every few months, audit how you work to make sure you are not building for how older models used to work.

## Takeaway

Give newer Claude models a clear goal and a verifiable check, prune instructions written for older models, and reserve subagents and extra process for work that actually needs them. Review still matters, but the default should be less prompting, not more.
