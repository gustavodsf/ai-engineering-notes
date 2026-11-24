# Keep Claude working toward a goal

Source: https://code.claude.com/docs/en/goal  
Publisher: Claude Code Docs (Anthropic)  
Page last modified: November 21, 2026 (from the official docs page metadata)  
Verified: HTTP 200 on November 23, 2026

## Key points

- The `/goal` command sets a completion condition, and Claude keeps working toward it without you prompting each step.
- After each turn, a model checks whether the condition holds. If it is not yet met, Claude starts another turn instead of returning control to you.
- The goal clears automatically once the condition is met, if the model judges the condition impossible to satisfy, or if a turn fails on an error you have to fix. You can also run `/goal clear`.
- Use a goal for substantial work with a verifiable end state, such as migrating a module until tests pass, implementing a design doc until acceptance criteria hold, or working through a labeled issue backlog until the queue is empty.
- One goal can be active per session. The same command sets, checks, and clears it depending on the argument.

### How to use it

Set a goal by running `/goal` followed by the condition. If a goal is already active, the new one replaces it. Setting a goal starts a turn immediately, with the condition itself as the directive. You do not need to send a separate prompt.

Example from the official docs:

```
/goal all tests in test/auth pass and the lint step is clean
```

- Run `/goal` with no arguments to see status: the condition, how long it has been running, how many turns have been evaluated, the current token spend, and the evaluator's most recent reason.
- Run `/goal clear` to remove an active goal before it resolves. Aliases for `clear` are `stop`, `off`, `reset`, `none`, and `cancel`. Running `/clear` also removes any active goal.

### Writing a good condition

The evaluator judges the condition against what Claude has already surfaced in the conversation. It does not run commands or read files independently, so write the condition as something Claude's own output can demonstrate. A condition that holds up across many turns usually has:

- One measurable end state (a test result, a build exit code, a file count, an empty queue)
- A stated check (how Claude should prove it, such as `npm test` exits 0)
- Constraints that matter (for example, "no other test file is modified")

The condition can be up to 4,000 characters. To bound how long a goal runs, include a turn or time clause, such as `or stop after 20 turns`.

### Other verified details

- A goal does not change your permission mode. To let goal turns run unattended, run `/goal` in auto mode. In Manual mode, Claude still asks before tool calls that your settings do not already allow.
- `/goal` is a wrapper around a session-scoped prompt-based Stop hook. After each turn, Claude Code sends the condition and the conversation so far to the configured small fast model, which returns one of three verdicts: not yet met, met, or impossible.
- Auto mode on its own approves tool calls within a single turn but does not start a new one. `/goal` adds a separate evaluator after every turn. The two are complementary.
- Evaluation tokens are billed in addition to main-turn spend.
- Official requirements stated on the page: `/goal` follows the same workspace trust rule as hooks in settings files, and it is unavailable when `disableAllHooks` is true or when `allowManagedHooksOnly` is set in managed settings.
- The official docs page does not state a minimum Claude Code version for `/goal` itself. It does state later version floors for related behavior, such as check-ins (v2.1.234+) and idle check-ins (v2.1.236+).

## Takeaway

Give `/goal` a condition that Claude can prove in the transcript, preferably in auto mode if you want it to run unattended, then let a separate evaluator decide when the work is done.
