# [Project name]

## Who writes what — read this first

You fill in only **three sections by hand, once, at setup**: `Goal and definition of done`, `Current state`, and `Repository map`. Write them in your own words.

From the first AI session on, **the AI drafts every update** — decisions, failures, state changes, known problems, next tasks, and closing reports — when you ask it to checkpoint or close (`CHECKPOINT_MESSAGE.md`, `CLOSING_ROUTINE.md`). Your job each time is short: read the draft, correct anything wrong, and commit. You are not expected to maintain or re-systematize these sections by hand.

## Goal and definition of done
[What does this project accomplish? What does finished look like? Write one to three specific sentences.]

## Current state — last verified [YYYY-MM-DD]
[What exists right now. What has been tested. What is broken, incomplete, or still unverified.]

## Repository map
[Where the worker should look next: code, documents, outputs, configuration, workflows, research, decisions, and any archive. This map is a route into the repository, not a replacement for those materials.]

## Operating protocol
[If present, read `AI_WORKFLOW.md` for the checkpoint, closing, and transfer rules. Use `OPENING_MESSAGE.md` to start, `WORKING_MESSAGE.md` during confirmed work, `CHECKPOINT_MESSAGE.md` for material updates, and `CLOSING_ROUTINE.md` before ending. If `AGENTS.md` is installed in the project root, follow it as the AI worker instruction file. These files describe how to work; this note describes what this project is.]

## Decisions made
[Add decisions with the reason. Keep old decisions; mark a later decision as superseding one instead of deleting history.]
- [YYYY-MM-DD] [Decision]. Reason: [why].

## Failed approaches — do not repeat
[Record what was tried, what happened, and why not to retry.]
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
[Keep only the last three to five short entries here. Promote durable decisions and failures into the sections above.]
- [YYYY-MM-DD] [What changed. What was verified. What remains.] 
