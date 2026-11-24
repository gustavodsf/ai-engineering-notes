# How Claude remembers your project

Source: https://code.claude.com/docs/en/memory  
Publisher: Claude Code Docs (Anthropic)  
Verified: HTTP 200 on November 23, 2026

This note focuses on `/doctor prompt-audit`, which is documented in the "Audit your instruction files" section of this page. The Commands reference and the "Check your setup with `/doctor`" section of the Skills page confirm the same command name and version floor.

Related official pages:

- Commands: https://code.claude.com/docs/en/commands (`/doctor [prompt-audit [path]]`; alias `/checkup`; `prompt-audit` requires Claude Code v2.1.283 or later)
- Skills, "Check your setup with `/doctor`": https://code.claude.com/docs/en/skills#check-your-setup-with-/doctor
- Best practices for Claude Code: https://code.claude.com/docs/en/best-practices

## Key points

- There is no `/prompt-diagnostic` command in the official Claude Code docs. The command is `/doctor prompt-audit`. `/checkup prompt-audit` is an alias.
- Plain `/doctor` is a setup checkup (installation, extensions, CLAUDE.md, permissions, and, on some plans, usage). To audit your instructions rather than your setup, run `/doctor prompt-audit`.
- `/doctor prompt-audit` checks instruction files for outdated or conflicting content. Official examples of problems it looks for: instructions written for older models, references to files or commands that do not exist, and files that contradict each other.
- You get a report of findings with proposed edits. Nothing in your files changes until you ask Claude to apply them.
- By default, the audit covers your CLAUDE.md, CLAUDE.local.md, and AGENTS.md files, plus the rules, skills, commands, subagents, and output styles under `.claude/` and `~/.claude/`.
- To audit one file or directory instead, pass its path. Official example:

```
/doctor prompt-audit .claude/skills/deploy
```

- The audit runs through the bundled `/claude-api` skill. It is unavailable while that skill is turned off in `skillOverrides` or with `disableBundledSkills`.
- `/doctor prompt-audit` requires Claude Code v2.1.283 or later.

The Best practices page states the same idea more briefly: `/doctor prompt-audit` flags instructions that were written for older models, point at files that no longer exist, or contradict each other.

## Takeaway

After a model upgrade, run `/doctor prompt-audit` on your CLAUDE.md and skills, read the report, and apply only the edits you want. It is an audit, not an automatic rewrite.
