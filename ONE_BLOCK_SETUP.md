# One-Block Basic Project Memory

Open your project in an AI assistant and paste the entire block below. It creates or repairs a simple project memory and then begins the session. It does not install the advanced automated checks or the complete Reader Kit.

```text
Project Memory Basic Block v1.2 — Public Companion

Run the basic Project Memory method for the currently open project. Detect your capabilities, inspect first, create or repair the basic memory if needed, and then begin the project session. Do not ask me to choose technical modes or repeat setup steps. Do not modify any other repository. If I add a plain-language project brief or current task immediately after this block, treat it as owner input: use it to initialize a new or empty project, and verify it against repository evidence in an existing project. If I add nothing, infer what you can from project evidence and group only consequential unknowns into one message.

CAPABILITY — announce the strongest truthful mode:
A. FULL AGENT: you can read and write project files and run commands.
B. READ-ONLY REPOSITORY: you can inspect a connected repository but cannot write files.
C. UPLOADED PROJECT: you can inspect uploaded files and create downloads but have no live repository.
D. CHAT ONLY: you cannot inspect project files.
Never confuse GitHub read access with permission to edit, commit, or push. In B, prepare exact replacement files or a patch and say they were not installed. In C, return ready-to-save files. In D, stop after offering three simple routes: open this block in a coding agent, connect a readable repository, or upload the project ZIP.

CONTROL:
- Begin read-only. Inspect the project tree, existing NOTES.md or STATE.md, README, relevant files, available history, current instructions, and git status when accessible.
- Decide automatically whether basic project memory is UNINSTALLED, NEEDS REPAIR, or READY.
- Answer questions from project evidence whenever possible. Group every consequential question the project cannot answer into one short message.
- Before creating or changing files, show one concise plan and ask for one approval. Preserve existing content and uncommitted work.
- Do not commit, push, publish, deploy, change repository settings, or perform destructive work without separate approval.
- Never place credentials, tokens, private keys, personal data, or confidential content in project memory, commits, or chat output.

INSTALL OR REPAIR — after approval:
1. Preserve an established NOTES.md, STATE.md, or equivalent memory file; otherwise create NOTES.md. Keep it concise and include headings for the goal and definition of done, current verified state and known problems, repository map, dated decisions and failed approaches, and next three tasks. Point important state claims to inspectable evidence such as a file, test, output, command result, or commit. Label uncertainty instead of guessing.
2. Preserve an existing repository instruction file such as AGENTS.md, CLAUDE.md, or GEMINI.md; if none exists, create a short AGENTS.md. It should say: read the memory file before substantial work; inspect relevant evidence; propose the next task and wait for confirmation; before ending, update the memory with changed state, decisions or failures, evidence, and next tasks; exclude secrets; show the diff; request approval before commit or push. Do not paste this entire block into the instruction file.
3. Record a dated decision in the memory file: Basic Block version 1.2, selected capability mode, chosen memory filename, and whether repository write access was available.
4. Review the changed files for accidental secrets, placeholders, unsupported claims, and unrelated edits. Run relevant existing project tests when available. Show git status and the complete diff or exact replacement files.
5. Report what was created or repaired and what remains uncertain. Ask for separate approval before commit and push. If approved, commit only the reviewed files and push only to the approved repository and branch.

SESSION — when basic memory is READY:
1. Read the memory and repository instructions, then inspect the relevant files and available history. Treat the memory as a map, not proof.
2. Report briefly: supported current state, evidence inspected, contradictions or uncertainty, and the proposed next task with observable completion checks. If I supplied a task with this block, evaluate that task instead. Wait for confirmation before substantial work.
3. After confirmation, stay inside the authorized task and verify important claims against project evidence.
4. Before ending, draft the memory update with changed state, evidence, decisions or failed approaches, and next three tasks. Run relevant checks, review the diff for secrets and unrelated changes, list files changed and remaining uncertainty, and propose a commit message.
5. Wait for approval before commit or push unless explicit write-back authority for this exact task was already granted.

This Basic Block intentionally omits mid-session checkpoints, automated memory freshness checks, release-artifact checks, multi-agent handoff, advanced permission rules, and the complete security protocol. Those are part of the complete Reader Kit.
```

## What the user does

1. Open the project in an AI assistant.
2. Paste the block once. In the same message, directly below it, add one to three ordinary sentences describing a new project's purpose or today's task. This is optional when an existing repository already makes the goal clear.
3. Answer only questions the project cannot answer.
4. Approve file changes, then separately approve commit or push.

The Basic Block is useful on its own for an ordinary project. The complete Reader Kit in *Never Start from Scratch* adds the Universal Master Block, mid-session checkpoints, `statefile`, `releasecheck`, connected-agent guidance, permission boundaries, reliable handoffs, and the complete security review.
