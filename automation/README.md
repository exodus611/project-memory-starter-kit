# Optional Automation Add-on

The Quick Start Card is the method. This add-on supplies two mechanical checks:

- **statefile** checks that your project memory exists, is recent, has useful sections, and does not contain obvious secret patterns.
- **releasecheck** checks a chosen release folder before you send or publish it.

The checks run in **your own repository and GitHub Actions environment**. There is no hosted service, account, customer database, or upload to the author.

## Recommended timing

- Run `statefile` when project memory changes on a push or pull request, and manually when you want a health check.
- Run `releasecheck` when preparing a release: manually or on a version tag. Do not point it blindly at the whole repository.

## Recommended: paste one block into your agent

Open the repository in an AI coding agent and paste [`ONE_BLOCK_SETUP.md`](../ONE_BLOCK_SETUP.md). Do not copy workflows or configure paths yourself.

The agent is instructed to inspect first, gather any unresolved questions into one message, request one approval, install and test everything it can establish safely, show the diff, and then request separate approval before commit or push.

The two approvals are intentional safety boundaries—not repeated installation work. If the agent cannot prove the release build command or artifact folder from repository evidence, it must leave that part pending rather than install a misleading workflow.

The same block detects platform capability. A coding agent with repository write access and a terminal can complete the installation. A read-only GitHub chat can prepare exact files but cannot apply or test them; a plain chat without project access can only tell the user what connection or upload is required. The block must state that limitation instead of claiming false automation.

## Manual fallback

1. Put your durable project memory in `NOTES.md` using `START_HERE.md` as the short guide.
2. Copy `statefile.yml` to `.github/workflows/statefile.yml`.
3. Copy `releasecheck.yml` to `.github/workflows/releasecheck.yml`.
4. In `releasecheck.yml`, replace `dist` with the actual release folder. If that folder is generated rather than committed, add the project's existing build step before the folder check.
5. Optionally copy and customize `releasecheck.example.json` as `releasecheck.json`, then add `manifest: releasecheck.json` to the action step.
6. Open a pull request. Confirm the memory check passes and review the complete diff.
7. Before a real release, run the release workflow manually or push the version tag your project uses.

## Honest limits

These tools do **not** prove that project notes are factually true, detect every kind of confidential information, replace human diff review, or remove secrets from old Git history. `releasecheck` only examines the folder you configure. Treat a passing check as evidence that specific mechanical tests passed—not as blanket approval.

**The Reader Kit guides the work. statefile checks the memory. releasecheck checks what you ship.** The complete behavioral protocol is in Appendix C of *Never Start from Scratch*; it is not reproduced here.
