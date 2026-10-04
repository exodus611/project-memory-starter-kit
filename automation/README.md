# Optional Automation Add-on

The Quick Start Card is the method. This add-on supplies two mechanical checks:

- **statefile** checks that your project memory exists, is recent, has useful sections, and does not contain obvious secret patterns.
- **releasecheck** checks a chosen release folder before you send or publish it.

The checks run in **your own repository and GitHub Actions environment**. There is no hosted service, account, customer database, or upload to the author.

## Recommended timing

- Run `statefile` when project memory changes on a push or pull request, and manually when you want a health check.
- Run `releasecheck` when preparing a release: manually or on a version tag. Do not point it blindly at the whole repository.

## Install with an AI coding agent

Give your agent this request from the root of your repository:

> Inspect this repository before changing anything. Read the Project Memory Quick Start Card and the files in its `automation/` folder. Identify the existing instruction file, the intended project-memory filename, the command that builds release artifacts, and the exact folder containing them. Propose a minimal installation using `NOTES.md`, `statefile` v0.2.2, and `releasecheck` v0.1.1. Configure the workflow paths and add the existing build command when CI must create the release folder; do not guess or scan the entire repository as the release folder. Preserve existing content and permissions. Explain what will run and when, show me the complete diff, and wait for my approval before committing or pushing.

That request intentionally requires inspection, explanation, a diff, and approval. It is not permission to publish or expose secrets.

## Manual installation

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
