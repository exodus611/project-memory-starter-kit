# One-Block Project Setup

Open your project in an AI coding agent and paste the entire block below. It is the only public setup command: the agent chooses the correct mode, installs or repairs the basic system when needed, and otherwise starts the next project session. You do not copy workflows or configure paths yourself.

```text
PROJECT MEMORY BASIC BLOCK v1.1 — PUBLIC COMPANION

Run the Project Memory Quick Start for the currently open project. This is one continuous workflow: detect capabilities, inspect the project, install or repair the basic system if needed, then begin the project session. Do not ask me to choose technical functions or repeat installation steps. Do not modify any other repository.

CAPABILITY — select and announce the strongest truthful mode:
A. FULL AGENT: you can read/write project files and run commands.
B. READ-ONLY REPOSITORY: you can inspect a connected repository but cannot write or run commands.
C. UPLOADED PROJECT: you can inspect uploaded files and create downloads but have no live repository.
D. CHAT ONLY: you cannot inspect project files.
Never downgrade silently. GitHub read access is not write, terminal, commit, or push access. In B, prepare a complete patch or ready-to-save files and say they are not installed or tested. In C, return a ready-to-apply package and say GitHub Actions did not run. In D, stop after offering three simple routes: open this same block in a coding agent, connect a readable repository, or upload the project ZIP.

CONTROL — keep the user experience simple:
- Begin read-only. Inspect the tree, git status, recent history when available, README/build documentation, package/build files, existing agent instructions, NOTES.md/STATE.md or equivalents, workflows, release configuration, and ignore rules.
- Decide automatically whether the project is UNINSTALLED, PARTIAL/NEEDS REPAIR, or READY. Do not make me choose.
- Answer from repository evidence. Ask only consequential questions whose answers cannot be found. Group every unresolved question into one short message, not a sequence.
- If installation or repair is needed, show one concise plan and request one approval for all file changes and local tests. Do not edit before approval.
- Preserve existing content and uncommitted work. Merge minimally. Do not publish, release, change repository settings, commit, or push without separate final approval.
- Never place credentials, tokens, private keys, personal data, or confidential content in memory, reports, commits, fixtures, or chat output.

PUBLIC SOURCES AND IMMUTABLE TOOL PINS:
- Quick Start: https://raw.githubusercontent.com/exodus611/project-memory-starter-kit/main/START_HERE.md
- statefile workflow template: https://raw.githubusercontent.com/exodus611/project-memory-starter-kit/main/automation/statefile.yml
- releasecheck workflow template: https://raw.githubusercontent.com/exodus611/project-memory-starter-kit/main/automation/releasecheck.yml
- optional manifest example: https://raw.githubusercontent.com/exodus611/project-memory-starter-kit/main/automation/releasecheck.example.json
- statefile v0.2.3 commit: 8e9dc90f98ee181b885fec72ce7f771b66d60057
- releasecheck v0.1.1 commit: b565180b141658b5370225f10e3775b50c36059e
Use full commit SHAs in GitHub Actions, with the friendly version in a comment. Checks run only in this project or its GitHub Actions environment. Add no hosted memory service, author upload, telemetry, or external database.

INSTALL OR REPAIR — after approval, execute without repeated interruptions:
1. Select the established memory file if one exists; otherwise create NOTES.md. Preserve useful content. Ensure it has concise headings for goal/definition of done, current verified state and known problems, repository map, decisions and failed approaches, and next three tasks. For important state claims, point to evidence such as a path, test, command result, or commit. Label unknowns.
2. Put the basic session rule in the repository's recognized instruction files, including AGENTS.md, CLAUDE.md, GEMINI.md, agent.md, instructions.md, PROTOCOL.md, docs/PROTOCOL.md, .cursorrules, .cursor/rules, or .github/copilot-instructions.md; create a short AGENTS.md if none exists. The rule must say: read the memory file before substantial work; verify important claims from project evidence; propose the next task and wait for confirmation; before ending, update the memory file with changed state, evidence, decisions/failures and next tasks; exclude secrets; show the diff; obtain approval before commit/push. Preserve substantive compatible rules and do not create a large public protocol.
3. Install .github/workflows/statefile.yml using the immutable statefile SHA. Configure both paths: filters and state-file: for the actual memory filename. Choose max-age-days from the evidenced work cadence; when unknown, use 14 and record that it is adjustable. Keep strict: 'true' enabled from installation and run the strict check before calling the project READY. On a legacy instruction file, a red first check is an expected repair signal: preserve the rule's intent but replace flagged pressure language or obsolete verification rituals with direct wording, then rerun. Removing noise is not permission to remove substantive rules. If a warning cannot be resolved safely, keep the gate red, classify the project PARTIAL/NEEDS REPAIR, and ask for the smallest decision needed; never disable strict merely to obtain green CI.
4. Install .github/workflows/releasecheck.yml only when repository evidence establishes a real release process, exact artifact folder, and any required build command. Never scan the repository root by guess. Use the immutable releasecheck SHA. The first CI trigger must be workflow_dispatch only. Offer a version-tag trigger only after one successful manual GitHub Actions run.
5. Create releasecheck.json only when evidence supports meaningful artifact requirements; otherwise run without a manifest instead of inventing requirements.
6. Keep workflow permissions at least privilege, normally contents: read.
7. Record a dated installation/repair decision in the memory file: Basic Block version 1.1, selected capability mode, memory filename, max-age policy, strict status, tool names plus versions and SHAs, release folder if known, and whether real GitHub Actions runs are confirmed or still pending.
8. Validate edited YAML/JSON and run relevant existing project tests. Run statefile against the selected memory file. If a real artifact folder exists, build it with the project's established command and run releasecheck against that folder. Use temporary directories for downloaded tools and fixtures; remove them and restore generated artifacts afterward unless intentionally tracked.
9. Test a safe failure path where practical using an obviously fake credential-shaped value only in a temporary untracked fixture. Confirm statefile fails and redacts the value. Never put the fixture in project files.
10. Review git status and the complete diff. Confirm unrelated files did not change. Report verbatim: selected mode; status before/after; memory filename; workflow paths filters; state-file value; max-age-days; strict status; release folder/build command or why pending; pinned SHAs; commands/checks and results; whether GitHub Actions were actually observed.
11. Ask for separate approval before commit and push. If approved, commit only reviewed files and push only to the approved repository/branch, then report the commit and remote checks.

SESSION — use this whenever the project is READY, and immediately after an approved setup when practical:
1. Read the memory and recognized repository instructions, then inspect relevant files and recent history available in this mode. Treat memory as a map, not proof.
2. Report briefly: supported current state, evidence inspected, contradictions or uncertainty, and the next task with observable completion checks. If I included a task with this block, evaluate that task instead. Wait for confirmation before substantial work.
3. After confirmation, stay within the authorized task and permissions. Verify important claims against files, outputs, tests, or history.
4. Before ending, draft the memory update with changed state, evidence, decisions or failed approaches, and next three tasks. Run relevant checks, perform a secret-aware diff review, show files changed and remaining uncertainty, and propose a commit message.
5. Wait for approval before commit/push unless explicit write-back authority for this exact task was already granted.

HONEST LIMITS — state these in the installation report, not on every normal turn: statefile checks existence, freshness, structure, recognized instruction patterns, and obvious secret shapes; releasecheck checks only the configured deliverable folder. Neither proves factual truth, catches every confidential item, replaces human review, or cleans old Git history.
```

## What the user does

1. Open the project in an AI coding agent.
2. Paste the block once.
3. Answer only questions the repository cannot answer.
4. Approve installation/repair, then separately approve commit/push.

On later sessions, paste the same block again. It detects that the project is ready, skips installation, reports the current state, and asks what to do next.

## Platform results

| Environment | Result from the same block |
|---|---|
| Coding agent with repository write access and a terminal | Installs or repairs, tests, shows the diff, then runs the basic session loop |
| Chat with read-only GitHub access | Prepares repository-specific files or a patch but cannot apply or test them |
| Chat with an uploaded project ZIP | Returns a ready-to-apply package; the user still places it in the repository |
| Plain chat without project files | Explains the one connection/upload step required; it does not pretend to install |

The complete Reader Kit in Appendix C adds the full checkpoint, handoff, connected-agent, permissions, and security protocol without changing this one-block user experience.
