# Your coding agent just learned to write its own glue code

LinkedIn post (draft, 23 Nov 2026).

## Post

**Your coding agent just learned to write its own glue code. Your permission hooks need to catch up.**

Anthropic added an experimental "Code Mode" to Claude Code. Instead of asking for one Bash/Read/Edit call at a time, the model writes a small JavaScript script that runs several tool calls, in parallel or chained, and returns only the output it needs. It's off by default (env flag, Claude Code v2.1.323+), and it only works in interactive terminal sessions.

Why it matters for teams shipping with agents:
• Context gets leaner. One early comparison reported in the article: 20–25% smaller context and, on a larger task, 37% fewer tokens and 19% lower cost. It wasn't faster, though, and on a tiny task it cost more.
• The security model shifts. Each call inside the script still goes through deny/ask rules and PreToolUse hooks, but in auto mode the classifier reviews the script before it runs, without seeing values computed at runtime. A hook that only matches "git push" can now receive "cd 'app' && git push", so hooks have to parse every part of a command.
• It doesn't make MCP obsolete. Auth, authorization and audit stay the same. What changes is how much of each result reaches the model.

My take: the "agent writes code to orchestrate tools" pattern (Cloudflare and Anthropic's own MCP work were there first) is turning into the default way to keep agents cheap. The guardrails have to move from "approve each call" to "verify the whole plan".

Are your agent guardrails ready to review a script instead of a single command?

Source: https://www.infoq.com/news/2026/11/claude-code-mode/

#AIEngineering #ClaudeCode #AIAgents #DevTools #SoftwareEngineering

## Articles

- [Claude Code Adds Experimental Code Mode to Orchestrate Tool Calls with JavaScript](Claude%20Code%20Adds%20Experimental%20Code%20Mode%20to%20Orchestrate%20Tool%20Calls%20with%20JavaScript.md)
