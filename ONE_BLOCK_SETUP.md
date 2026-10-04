# One-Block Agent Setup

Open the repository you want to configure in an AI coding agent. Paste the entire block below once. The agent should inspect, ask only unresolved questions, request one installation approval, do the work, test it, and then wait for separate approval before any commit or push.

```text
Set up this repository with the public Project Memory Quick Start and its optional mechanical checks. Treat the currently open repository as the only target. Do not modify any other repository.

Operating rules:
- Work from repository evidence, not guesses.
- Start read-only. Inspect the tree, git status, recent history, README/build documentation, package or build files, existing agent instructions, existing NOTES.md/STATE.md, workflows, release configuration, and ignore rules.
- Do not ask me to copy files, visit several pages, or perform installation steps that you can perform with available tools.
- Do not overwrite or discard existing project memory, instructions, workflows, or uncommitted work. Merge minimally and explain conflicts.
- Never put credentials, personal data, private keys, tokens, or confidential content into project memory, reports, commits, or chat output.
- Do not assume that the repository root is the release folder. Infer the build command and exact artifact folder from evidence. If they cannot be established, mark release automation pending instead of inventing values.
- Use only the public setup materials at:
  https://raw.githubusercontent.com/exodus611/project-memory-starter-kit/main/START_HERE.md
  https://raw.githubusercontent.com/exodus611/project-memory-starter-kit/main/automation/statefile.yml
  https://raw.githubusercontent.com/exodus611/project-memory-starter-kit/main/automation/releasecheck.yml
  https://raw.githubusercontent.com/exodus611/project-memory-starter-kit/main/automation/releasecheck.example.json
- Pin statefile to v0.2.2 and releasecheck to v0.1.1. Checks must run in this repository or its GitHub Actions environment; do not add a hosted memory service, telemetry, an external database, or uploads to the author.

Capability check — choose the strongest truthful mode automatically:
A. Full agent mode: if you can read and write repository files and run commands, perform the complete process below.
B. Read-only repository mode: if you can inspect a connected repository but cannot write or run commands, complete the inspection, ask unresolved questions once, and prepare a downloadable patch or complete ready-to-save files. State clearly that installation and tests have not been executed. Do not claim success or ask for push approval.
C. Uploaded-project mode: if you have file creation but no live repository, ask once for a ZIP or the minimum missing project files, then return a ready-to-apply setup package plus exact placement instructions. Do not claim that GitHub Actions ran.
D. Chat-only mode: if you cannot inspect project files, do not attempt generic configuration. Explain in one short message that full automation requires opening this same block in a coding agent with repository/file access, connecting a readable repository, or uploading a project ZIP. Ask the user to choose one of those three routes.
Never downgrade silently. Name the selected mode and its limitation before planning. Do not confuse GitHub read access with permission to edit, commit, push, or run a terminal.

Phase 1 — inspect and ask once:
1. Determine whether NOTES.md, STATE.md, or an equivalent memory file already exists. Prefer preserving the established filename; for a new setup use NOTES.md.
2. Determine the repository's existing agent-instruction file, if any.
3. Determine whether GitHub Actions is appropriate here.
4. Determine the real build command and release-artifact folder, if the repository has a release process.
5. Check for existing workflows or policies that the setup must not conflict with.
6. Answer from repository evidence whenever possible. Collect all genuinely unresolved questions into one short message; do not ask them one at a time.
7. Present one concise installation plan listing files to create or modify, checks to run, and anything that will remain pending. Then ask for one approval to perform the whole installation and local verification. Do not edit files before that approval.

Phase 2 — after installation approval, execute without repeatedly interrupting me:
1. Create or minimally update the project-memory file. Base it on the Quick Start headings: goal, current verified state and known problems, repository map, decisions and failed approaches, and next three tasks. Fill only facts supported by repository evidence; label unknowns honestly. Preserve useful existing content.
2. If an agent-instruction file exists, add only a short rule to read the memory file before substantial work, propose an evidence-based update before ending, exclude secrets, and show diffs before commit. Do not replace existing instructions and do not invent a large behavioral protocol.
3. Install the statefile workflow at .github/workflows/statefile.yml. Configure its path filters and state-file input for the actual memory filename. Preserve compatible existing workflow behavior.
4. Install releasecheck at .github/workflows/releasecheck.yml only when a real release process and artifact folder can be identified. Configure the exact folder and add the repository's existing build command when CI must generate it. Never default blindly to scanning the whole repository. If release information is unresolved, leave this workflow uninstalled and clearly report what fact is needed.
5. Add releasecheck.json only if repository evidence supports meaningful required artifacts or rules; otherwise use releasecheck without a manifest rather than inventing requirements.
6. Keep workflow permissions at least privilege, normally contents: read.
7. Run available local validation. At minimum validate edited YAML/JSON, run statefile against the selected memory file, and, when a real artifact folder exists, run releasecheck against that folder. Use temporary locations for downloaded test tools and remove them afterward. Remove or restore generated test artifacts afterward unless they existed before or are intentionally tracked. Do not expose matched secret values in output.
8. Exercise both success and safe failure behavior where practical. A failure test must use an obviously fake credential-shaped value in a temporary fixture, never in tracked project files, and must confirm that statefile redacts it.
9. Run the repository's relevant existing tests if the changes can affect them.
10. Review git status and the complete diff. Confirm that unrelated files were not changed.

Phase 3 — report and stop:
- Report what was installed, what was detected, every command/check run and its result, any limitation or pending item, and the complete diff or a precise diff summary with paths.
- Explain that statefile checks existence, freshness, structure, and obvious secret patterns; releasecheck checks only the configured deliverable folder. They do not prove factual truth, detect every confidential item, replace human review, or clean old Git history.
- Do not commit, push, publish, create a release, change repository settings, or change store metadata yet.
- Ask for a separate final approval before commit and push. If approved, commit only the reviewed files, push only to the approved repository/branch, then report the commit and remote checks.
```

## What “one block” means

You paste one instruction block. The agent handles inspection, setup, and testing. You still retain two deliberate control points:

1. approval before it changes files;
2. approval before it commits or pushes.

Those are safety boundaries, not manual installation work.

## Where full automation works

| Environment | Result from the same block |
|---|---|
| Coding agent with repository write access and a terminal | Full inspection, installation, local tests, diff, then approval-gated commit/push |
| Chat with a read-only GitHub connection | Repository-specific files or patch are prepared, but cannot be applied or tested automatically |
| Chat that accepts a project ZIP and can create downloads | A ready-to-apply setup package is returned; the user still applies it to the repository |
| Plain chat with no project-file access | Guidance only; truthful automatic installation is impossible |

The prompt cannot manufacture permissions that the product does not provide. For the least manual experience, use a coding-agent mode that can edit the checked-out repository and run a terminal.
