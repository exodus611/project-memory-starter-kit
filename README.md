# Project Memory Starter Kit

A copy-ready starter kit for the repository-first project handoff method from *The Project Has a Memory*.

**Start with `START_HERE.md`.** It is one block: you fill in three sections once, paste one message each session, and the AI runs the whole protocol (open → checkpoint → close) by itself. You mainly say "yes", "no", and "commit".

## What is included

- `START_HERE.md` — **the one block.** Read this first; it is all most people ever use.
- `NOTES.md` — the project map and current handoff template (the file the AI keeps updated for you);
- `AI_WORKFLOW.md` — the full operating protocol behind the block (reference);
- `AGENTS.md` — instructions for an AI coding agent / project worker (reference);
- `OPENING_MESSAGE.md`, `WORKING_MESSAGE.md`, `CHECKPOINT_MESSAGE.md`, `CLOSING_ROUTINE.md` — the individual phase prompts that `START_HERE.md` collapses into one block (reference);
- `SECURITY_CHECKLIST.md` — the pre-commit security checklist.

The full project record belongs in the repository. `NOTES.md` is the map and handoff inside it, not a replacement for the code, documents, outputs, configuration, workflows, research, or history.

## Who writes what

You fill in only three sections by hand, once, at setup — **Goal and definition of done**, **Current state**, and **Repository map** — in your own words. From the first session on, the AI drafts every update (decisions, failures, state, next tasks, closing reports) when you ask it to checkpoint or close. You review, correct, and commit. You don't rebuild the note by hand session after session.

## Quick path

1. Create a repository for one project. Make it private unless you have a deliberate reason to publish it.
2. Copy `NOTES.md` into the repository. Fill in **Goal**, **Current state**, and **Repository map** before the first commit.
3. Each session: paste the block from `START_HERE.md` together with your `NOTES.md` (or the repository link). The AI reports state, checkpoints on its own, and drafts the closing update.
4. You verify what the AI drafts and approve the commit. Read `SECURITY_CHECKLIST.md` before committing anything new.

## What "automatic" means here

The starter kit provides a repeatable, AI-assisted protocol. The AI can draft updates when the human asks for a checkpoint or closing report. A connected agent can prepare repository edits if it has approved access. The human still reviews the understanding and diff by default.

A normal GitHub repository cannot detect that an arbitrary chat session has ended. Fully automatic updates require a specific integration or agent workflow that sends a checkpoint event. The kit does not pretend that platform memory, a chat window, or a repository connection will update `NOTES.md` by itself.

The repository is the project record. `NOTES.md` is the map and handoff inside it. The AI drafts and executes; you verify the understanding, the work, and the committed changes before relying on them.

_Last reviewed: September 21, 2026. Platform interfaces, instruction-file support, permissions, and plan limits change; check the current documentation for the service you use._
