# START HERE — один файл, один блок, ничего больше

You set this up **once**. After that, each AI session is **one paste** and the AI runs everything by itself. This file is self-contained: the block and the `NOTES.md` template are both right here. There is nothing else you need to download or open.

---

## 1. One-time setup (once, ~5 minutes)

1. Create **one private repository** for the project and put the project's files in it.
2. Copy the `NOTES.md` template from the end of this file into the repository.
3. Fill in **three sections by hand** (the rest of the note is filled for you by the AI later):
   - **Goal and definition of done** — what the project is for, and what "finished" looks like.
   - **Current state** — what exists right now, with today's date.
   - **Repository map** — where the project's files live.

That is the only hand-filling you will ever do.

---

## 2. The one block (paste once per session)

Paste this **together with your NOTES.md** (or with the repository link, if the AI can read it). This single block trains the AI to run the whole protocol by itself — open, checkpoints, closing. You never hunt for a file at a particular stage.

```
We are working on my project. Run this standing protocol every session, without me re-explaining.

START (before any work):
1. Read NOTES.md first, then inspect the relevant project files and recent history.
2. Report what the record supports about the current state, what you are unsure about, and what the next task should be.
3. Wait for my confirmation before starting work.

WHILE WORKING (automatic — do not wait to be asked):
When a decision is made, an approach fails, the state changes, or the priority changes,
draft a short checkpoint update (date, what changed, result, reason, next step) and show it to me.

BEFORE THE SESSION ENDS (automatic — do not wait to be asked):
Draft the closing update: decisions, failures, state (dated), the next three tasks, files changed,
and a proposed commit message. Show me the draft and the diff; after I review and approve, commit.

RULES:
- NOTES.md is the map; the repository files are the record. Verify against the files and history — never guess.
- Never put passwords, tokens, private keys, or confidential data in NOTES.md or any committed file.
- Say clearly when you are uncertain.
```

---

## 3. What a session looks like

- **Start:** paste the block + your NOTES.md → the AI reports state and next task → you say "yes" or "no, do Y".
- **Middle:** the AI drafts checkpoints on its own when something material happens → you glance and approve.
- **End:** the AI drafts the full closing update and commit message on its own → you fix anything wrong, say "commit".
- **You never re-type, re-fill, or maintain the note by hand after the first setup.**

## 4. If the AI can read your repository

First line becomes: `Read this repository: [repository URL]. Start with NOTES.md...` — the rest of the block is unchanged.

## 5. If the AI cannot read a repository

Add this line at the top of the block, keep the rest unchanged:

```
You cannot access the repository. Each session I will paste NOTES.md and the relevant files.
Run the same protocol against what I paste; I will apply your approved updates to the repository myself.
```

---

## The NOTES.md template (copy this into your repository)

```markdown
# [Project name]

## Goal and definition of done
[What does this project accomplish? What does finished look like? Write one to three specific sentences.]

## Current state — last verified [YYYY-MM-DD]
[What exists right now. What has been tested. What is broken, incomplete, or still unverified.]

## Repository map
[Where the worker should look next: code, documents, outputs, configuration, workflows, research, decisions, and any archive. This map is a route into the repository, not a replacement for those materials.]

## Decisions made
- [YYYY-MM-DD] [Decision]. Reason: [why].

## Failed approaches — do not repeat
- [YYYY-MM-DD] Tried: [what]. Outcome: [what happened]. Do not retry because: [reason].

## Known problems
[Open issues and current workarounds. If something is untested, say so.]

## Next three tasks
1. [Most important next task]
2. [Second priority]
3. [Third priority]

## External services and dependencies
[Names and purposes only. Never put passwords, API keys, tokens, private keys, or sensitive client data here.]

## Notes on sessions
- [YYYY-MM-DD] [What changed. What was verified. What remains.]
```
