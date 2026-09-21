# START HERE — one block, one setup, done

**You do not maintain this by hand. You set it up once, paste one block, and the AI runs the rest.** Keep this file with the kit and read it before anything else.

---

## 1. One-time setup (you, once, ~5 minutes)

1. Create **one private repository** for the project and put the project's files in it.
2. Copy `NOTES.md` into the repository. Fill in **three sections by hand, in your own words** — and nothing else:
   - **Goal and definition of done**
   - **Current state** (with the date)
   - **Repository map** (where each kind of file lives)
3. Done. That is the only hand-filling you will ever do.

---

## 2. The one block (paste every session — or pin it)

Below is **one message**. At the start of a session, paste it **together with** your
current `NOTES.md` (or the repository link, if the tool can read it). This single block
"trains" the AI to run the whole protocol by itself — opening, checkpoints, and closing —
so you never hunt for the right file at the right moment.

```
We are working on my project. Run this standing protocol every session, without me re-explaining.

START (before any work):
1. Read NOTES.md first, then inspect the relevant project files and recent history.
2. Report what the record supports about the current state, what you are unsure about, and what the next task should be.
3. Wait for my confirmation before starting work.

WHILE WORKING (do this automatically — do not wait to be asked):
When a decision is made, an approach fails, the state changes, or the priority changes,
draft a short checkpoint update (date, what changed, result, reason, next step) and show it to me.

BEFORE THE SESSION ENDS (do this automatically):
Draft the closing update: decisions, failures, state (dated), the next three tasks,
files changed, and a proposed commit message. Show me the draft and the diff;
after I review and approve, you commit.

RULES:
- NOTES.md is the map; the repository files are the record. Never guess — verify against the files and history.
- Never put passwords, tokens, private keys, or confidential data in NOTES.md or any committed file.
- Say clearly when you are uncertain.
```

---

## 3. If the AI can read your repository

Use the same block, but the first line becomes:

```
Read this repository: [repository URL]. Start with NOTES.md, then inspect the relevant files and history.
Rest of the block unchanged.
```

---

## 4. If the AI cannot read a repository (upload or paste)

Use the same block, but add this line at the top:

```
You cannot access the repository. Each session I will paste NOTES.md and the relevant files.
Run the same protocol against what I paste: start with NOTES.md, report state and next task,
checkpoint after material events, and draft the closing update before I leave.
I will paste the files; I will apply your approved updates to the repository myself.
```

---

## 5. What your sessions now look like

- **Start:** paste the block + your `NOTES.md` → the AI reports state and next task → you say "yes" or "no, do Y".
- **Middle:** the AI drafts checkpoints on its own when something material happens → you glance and approve.
- **End:** the AI drafts the full closing update and commit message on its own → you fix anything wrong, say "commit".
- **You never re-type, re-systematize, or "fill the kit" yourself after the first setup.**

The other files in this kit (`AI_WORKFLOW.md`, `AGENTS.md`, the individual message files,
`SECURITY_CHECKLIST.md`) are the detailed reference behind this block — you will rarely need
them during a session. `NOTES.md` is the file the AI keeps updated for you.
