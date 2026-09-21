# Instructions for an AI project worker

You are a temporary worker in a project whose primary record is this repository.

## Before acting

1. Read `NOTES.md` first.
2. Follow its repository map into the relevant files, outputs, configuration, workflows, and recent commits.
3. Do not assume `NOTES.md` contains the whole project.
4. Report what the repository supports, what is uncertain, which evidence you inspected, and what task you propose.
5. Wait for confirmation before substantial work unless the human has clearly authorized the task.

## While working

- Verify important claims against project files, outputs, tests, or history.
- Do not guess when the note is incomplete; search the repository or ask the human.
- When a decision, failure, state change, known problem, or priority change matters to future work, prepare a checkpoint.
- Keep detailed evidence in the appropriate project file. Put a concise summary and pointer in `NOTES.md`.
- Never put passwords, tokens, private keys, or confidential data in `NOTES.md` or committed files.
- Do not make destructive changes, publish material, or use write access beyond the task that was authorized.

## Checkpoint format

When a material event occurs, draft the affected updates:

- Event and date
- What changed or was tried
- Result and evidence
- Decision or reason
- Files that contain the detail
- Effect on current state
- Next action

Show the human the draft before committing it.

## Before ending the session

Draft a closing report with:

- decisions and reasons;
- failed approaches and why not to retry;
- current state and verification performed;
- files changed and tests run;
- remaining uncertainty;
- next three tasks;
- proposed commit message.

Update `NOTES.md` and the relevant project files, review the diff and security checklist, and ask for approval before committing unless explicit write-back authority exists.

## Handoff

Before switching to another session, model, platform, or person, leave a committed handoff with the branch, latest commit, exact next task, completed work, open work, and evidence to inspect. The next worker starts with `NOTES.md` and verifies the handoff against the repository.
