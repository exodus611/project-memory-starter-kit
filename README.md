# Project Memory Starter Kit

A copy-ready starter kit for the repository-first project handoff method from *The Project Has a Memory*.

## What is included

- `NOTES.md` — the project map and current handoff template;
- `OPENING_MESSAGE.md` — the start-of-session prompt;
- `WORKING_MESSAGE.md` — the prompt for the confirmed task and active work;
- `CHECKPOINT_MESSAGE.md` — the prompt for a material update or context transfer;
- `CLOSING_ROUTINE.md` — the end-of-session checklist and summary prompt;
- `AI_WORKFLOW.md` — the full operating protocol: when to read, checkpoint, update, commit, and transfer;
- `AGENTS.md` — concise instructions that can be copied into a project repository for an AI coding agent or adapted to a platform’s instruction file;
- `SECURITY_CHECKLIST.md` — the pre-commit security checklist.

The full project record belongs in the repository. `NOTES.md` is the map and handoff inside it, not a replacement for the code, documents, outputs, configuration, workflows, research, or history.

## Setup

1. Create a repository for one project. Make it private unless you have a deliberate reason to publish it.
2. Copy `NOTES.md` into the repository and keep the project’s code, documents, outputs, configuration, workflows, and history there as appropriate.
3. Copy `AGENTS.md` to the project root if your AI tool recognizes `AGENTS.md`; otherwise adapt its rules to the tool’s supported instruction or project-context file. Do not assume every platform loads it automatically.
4. Fill in **Goal and definition of done**, **Current state**, and **Repository map** before the first commit.
5. Use `OPENING_MESSAGE.md` at the start of every AI session: note first, then relevant files and history.
6. After the task is confirmed, use `WORKING_MESSAGE.md` to set the work boundary and acceptance checks.
7. Use `CHECKPOINT_MESSAGE.md` after decisions, failures, material changes, priority changes, or before context transfer. Follow `AI_WORKFLOW.md` for the full rules.
8. Use `CLOSING_ROUTINE.md` before the session ends; update the handoff and any changed project artifacts.
9. Read `SECURITY_CHECKLIST.md` before committing anything new.

## Who writes what

You fill in only three sections by hand, once, at setup — **Goal and definition of done**, **Current state**, and **Repository map** — in your own words. From the first session on, the AI drafts every update (decisions, failures, state, next tasks, closing reports) when you ask it to checkpoint or close. You review, correct, and commit. You don't rebuild the note by hand session after session.

## What “automatic” means here

The starter kit provides a repeatable, AI-assisted protocol. The AI can draft updates when the human asks for a checkpoint or closing report. A connected agent can prepare repository edits if it has approved access. The human still reviews the understanding and diff by default.

A normal GitHub repository cannot detect that an arbitrary chat session has ended. Fully automatic updates require a specific integration or agent workflow that sends a checkpoint event. The kit does not pretend that platform memory, a chat window, or a repository connection will update `NOTES.md` by itself.

The repository is the project record. `NOTES.md` is the map and handoff inside it. The AI drafts and executes; you verify the understanding, the work, and the committed changes before relying on them.

_Last reviewed: September 21, 2026. Platform interfaces, instruction-file support, permissions, and plan limits change; check the current documentation for the service you use._
