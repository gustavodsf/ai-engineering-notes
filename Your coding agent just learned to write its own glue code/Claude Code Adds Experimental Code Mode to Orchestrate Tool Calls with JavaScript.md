# Claude Code Adds Experimental Code Mode to Orchestrate Tool Calls with JavaScript

Source: [InfoQ, Daniel Dominguez, 23 Nov 2026](https://www.infoq.com/news/2026/11/claude-code-mode/)

## Key points

- **What it is:** instead of requesting each Bash, Read or Edit call separately, Claude writes a JavaScript script that drives its tools: commands in parallel, one result fed into the next call, and only the needed output returned to the model.
- **How to enable:** experimental and off by default. Requires Claude Code v2.1.323+ and `CLAUDE_CODE_EXPERIMENTAL_CODE_MODE=1`. Project settings cannot turn it on, and admins can block it via managed settings.
- **Best for:** edits repeated across many files, searches that need filtering, and independent commands.
- **Limits:** scripts Claude waits on stop after 10 minutes; in auto/bypassPermissions mode they can run in the background for up to 2 hours. Only interactive terminal sessions of the native build. Not available with `-p`, the Agent SDK, VS Code, Desktop, Bedrock, gateways or zero-data-retention orgs.
- **Permissions:** every call inside a script still goes through deny/ask rules and PreToolUse hooks. In auto mode the classifier reviews the script before it runs, not each call, and cannot see runtime values. A hook may receive `cd 'app' && git push`, so hooks must check every part of a command. A hook on the REPL tool can read the script from `tool_input.code`.
- **Numbers (community, not Anthropic):** across 8 Sonnet 5.5 runs, same results, 20–25% smaller context, and 37% fewer tokens and 19% lower cost on the bigger task. Not faster, and more expensive on a tiny task.
- **MCP is not obsolete:** auth, authorization and audit stay the same; what changes is how much context reaches the model.
- **Prior art:** Cloudflare's Code Mode for MCP (tools as a TypeScript API in sandboxed Workers), Anthropic's code execution with MCP (one workflow went from 150,000 to 2,000 tokens) and programmatic tool calling in the Claude API.

## Takeaway

Guardrails need to move from approving each call to verifying the whole plan.
