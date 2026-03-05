# qabot

A meta-repo that packages up QA skills for [Claude Code](https://docs.anthropic.com/en/docs/claude-code). Instead of adding QA tooling to every project, you run Claude Code from this repo and point it at whatever you want to test.

This keeps QA skills centralized and avoids bloating your project's Claude context with lengthy QA instructions, templates, and references. Your projects stay focused on their own code; QA lives here.

## How it works

```
~/qabot/          <-- You run Claude Code here
  .claude/skills/ <-- QA skills live here (dogfood, etc.)

~/your-project/   <-- Claude works on this (or any target)
```

1. Clone this repo
2. `cd qabot`
3. Run `claude`
4. Tell it what to test: `dogfood https://myapp.com` or `dogfood http://localhost:3000`

Claude picks up the skills from `.claude/skills/` automatically. No installation or configuration needed beyond the prerequisites below.

## Prerequisites

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installed and authenticated
- [agent-browser](https://github.com/vercel-labs/agent-browser) installed (the `/dogfood` skill uses it for browser automation). See the agent-browser repo for install instructions.

## Available skills

| Skill | Description |
|-------|-------------|
| `/dogfood` | Systematically explore a web app, find bugs, and produce a report with screenshots, repro videos, and detailed repro steps for every issue |

## Adding skills

Drop new skills into `.claude/skills/` following the standard [Claude Code skill format](https://docs.anthropic.com/en/docs/claude-code/skills). They'll be available to everyone who clones the repo.

## License

MIT
