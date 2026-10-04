# Project Memory — Quick Start Card

This free card lets you try the method in one session. The complete Reader Kit — full templates, checkpoint and closing messages, connected-agent guidance, and the security review — is included in *Never Start from Scratch*.

## 1. Create the map

Create a private project repository and add `NOTES.md`:

```markdown
# [Project name]

## Goal
[What should this project accomplish?]

## Current state and known problems — verified [YYYY-MM-DD]
[What exists, works, is blocked, or is uncertain? Point to a file, test, output, or commit as evidence.]

## Repository map
[Where are the important files and evidence?]

## Decisions and failed approaches
- [Decision or failed attempt, with date and reason.]

## Next three tasks
1. [First]
2. [Second]
3. [Third]
```

Never put passwords, tokens, private keys, or confidential data in this file or any commit.

## 2. Open every session with one message

```text
Read this repository: [repository URL]
Start with NOTES.md, then inspect the relevant files and recent history.
Tell me what the evidence supports, what is uncertain, and what task should
come next. Wait for my confirmation before substantial work.
```

If the assistant cannot open the repository, attach `NOTES.md` and the relevant project files instead.

## 3. Close by saving the handoff

Before ending, ask the assistant to draft the updated state, decisions, failed approaches, next three tasks, files changed, checks run, and a commit message. Review the actual diff before committing.

That is enough to test the basic method. Mid-session checkpoints and the complete copy-ready workflow are inside the book so the public card stays short and useful.
