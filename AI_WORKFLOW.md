# AI workflow: when to read, write, update, and hand off

This guide explains how a human and an AI worker use the starter kit together. It is deliberately explicit: a short `NOTES.md` is a map, not the whole project, and the AI must follow the map into the repository evidence.

## The hierarchy

1. **The repository is the project record.** It may contain code, documents, outputs, configuration, workflows, research, decisions, and history.
2. **`NOTES.md` is the map and current handoff.** It summarizes the current state and points to the files that contain the detail.
3. **The AI session is a temporary worker.** Platform memory, chat history, and project workspaces may help, but they do not replace the repository.
4. **The human owns decisions and commits.** The AI may draft and execute, but the human reviews the understanding, the diff, and the handoff.

## When a session starts or resumes

The AI should do this before substantial work:

1. Read `NOTES.md`.
2. Follow its repository map into the relevant files, outputs, configuration, workflows, and recent history.
3. Check whether the note is stale, incomplete, or contradicted by the evidence.
4. Report:
   - what the repository supports about the current state;
   - what remains uncertain;
   - which files or commits were inspected;
   - the proposed next task and its acceptance check.
5. Wait for the human to confirm before starting substantial work.

Use `OPENING_MESSAGE.md` for the copy-ready prompt.

If `NOTES.md` does not answer a question, do not guess. Search the repository and history, ask the human when evidence is missing, and record the correction when the answer is known.

## Prompt by phase

- **Start:** `OPENING_MESSAGE.md` asks the AI to read the map, inspect evidence, report uncertainty, and confirm the task.
- **During confirmed work:** `WORKING_MESSAGE.md` sets the task boundary, acceptance checks, and verification rule.
- **Checkpoint:** `CHECKPOINT_MESSAGE.md` asks for a dated, evidence-based draft after a material event or before context transfer.
- **Close:** `CLOSING_ROUTINE.md` asks for the final handoff, evidence, security review, and proposed commit.

These prompts are reminders for the human and AI. They do not override repository instructions, permissions, or the human’s approval boundary.

## When the AI must prepare an update

Do not wait only for the end of a chat. Prepare a checkpoint whenever one of these events happens:

| Event | What the AI records | Where the detail belongs |
|---|---|---|
| A decision is made | Decision, reason, alternatives rejected, date | Relevant project document or decision log; summarize and link it in `NOTES.md` |
| An approach fails | What was tried, result, and why not to retry | Failure log, issue, experiment note, or commit; point to it from `NOTES.md` |
| Code, documents, outputs, configuration, or workflows change | What changed and how it was checked | The changed project files; update the current-state summary and repository map |
| A known problem appears or is fixed | Problem, evidence, workaround, and status | Relevant issue or project file; update `Known problems` in `NOTES.md` |
| The next priority changes | New priority and reason | `Next three tasks` in `NOTES.md`, plus the detailed task file if one exists |
| The context is becoming long, is being summarized, or the tool may lose access | A checkpoint of the current state, open work, and exact next step | `NOTES.md` and any changed artifacts; commit before switching when possible |
| The human asks to switch model, platform, person, or agent | A transfer-ready handoff | `NOTES.md`, repository files, branch name, and latest commit |

A checkpoint is not permission to commit automatically. The AI drafts the update, shows what changed, and follows the human’s approval boundary.

## What goes in `NOTES.md` and what does not

Put a concise, current summary in `NOTES.md`:

- current state and verification date;
- the repository map and pointers;
- decisions that affect future work;
- failed approaches worth avoiding;
- known problems and workarounds;
- the next three tasks;
- the last few session outcomes.

Keep detailed evidence in the repository where it belongs:

- code in code files;
- long research in research or document files;
- generated outputs in output folders;
- detailed decisions in decision or design documents;
- complete history in commits;
- secrets in an approved secret manager, never in the note or committed files.

The test is: would the next worker need this summary to choose or verify the next action? If yes, put the short version in `NOTES.md` and point to the detailed evidence.

## How a session closes

Before the human ends the session, the AI should ask for or draft:

1. decisions made and their reasons;
2. failed approaches and why not to retry;
3. changes to the project state and what was verified;
4. the next three tasks in priority order;
5. files changed, tests run, and remaining uncertainty;
6. a proposed commit message.

The human then:

1. reviews the draft against the conversation and repository files;
2. corrects the AI’s mistakes;
3. reviews the diff and security checklist;
4. commits the note and relevant project changes;
5. asks the AI to read the committed handoff back and report discrepancies.

Use `CLOSING_ROUTINE.md` for the short checklist and prompt.

## Transfer to another session, model, platform, or person

Transfer before the current chat becomes difficult to navigate, before context compaction, before changing tools, or whenever another person needs to continue.

The outgoing worker should leave:

- a current `NOTES.md`;
- relevant project files and outputs committed;
- the branch name and latest commit;
- the exact task to continue;
- what is done, what is not done, and what remains uncertain;
- any command, test, or review needed next.

The incoming worker should start with `NOTES.md`, inspect the listed evidence and recent history, report its understanding, and confirm the next task. Never transfer only a vague chat summary when the repository can contain the evidence.

## Levels of automation

The starter kit supports different levels. They are not the same thing:

### Manual

The human copies the opening prompt, asks for checkpoints, updates GitHub, and commits. This works with any AI tool that can receive text or files.

### AI-assisted

The AI drafts `NOTES.md` updates, decision entries, failure entries, and commit messages. The human reviews and commits them. This is the recommended default.

### Connected agent

An authorized agent can read the repository and may prepare edits or a commit. It must show the diff and wait for approval unless the human has explicitly authorized unattended write access for that workflow.

### Actual automation

GitHub Actions can run tests, builds, scheduled jobs, and validation. GitHub does not automatically know that an arbitrary chat session has ended. A real automatic update requires an explicit integration or agent workflow that emits a checkpoint event. Do not assume that platform memory or a connected repository will write `NOTES.md` by itself.

## The compact rule

**Read the map. Inspect the repository. Work. Checkpoint when something material changes. Close with a reviewed update. Commit. Transfer from the repository, not from memory.**
