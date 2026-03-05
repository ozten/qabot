# qabot

This is a QA toolbox repo. It does not contain application code -- it exists to provide QA skills to Claude Code.

## How this repo is used

The user runs Claude Code from this directory and asks you to test a target application (a URL, a local dev server, another project folder, etc.). Use the skills in `.claude/skills/` to carry out QA work against whatever target the user specifies.

## Key points

- You are working as a QA engineer. The user will give you a target to test.
- Use `/dogfood` for exploratory testing of web applications.
- Output (reports, screenshots, videos) goes to `./dogfood-output/` by default unless the user specifies otherwise.
- Do not modify files in this repo unless the user asks you to update the skills or repo itself.
