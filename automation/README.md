# Advanced Automation Templates

The public Basic Block does not install these files. They remain public for inspection and are used by the complete Universal Master Block in the book. The advanced layer supplies two mechanical checks:

- **statefile** checks that your project memory exists, is recent, has useful sections, and does not contain obvious secret patterns.
- **releasecheck** checks a chosen release folder before you send or publish it.

The checks run in **your own repository and GitHub Actions environment**. There is no hosted service, account, customer database, or upload to the author.

## Recommended timing

- Run `statefile` when project memory changes on a push or pull request, and manually when you want a health check.
- Run `releasecheck` manually for its first real CI run. Add a version-tag trigger only after that run is green. Do not point it blindly at the whole repository.

## How these templates are used

The complete Universal Master Block inspects the repository, determines the real memory filename, build command and release folder, then configures these templates and tests both success and safe failure behavior. It leaves release automation pending rather than guessing a folder.

The free [`BASIC_PROJECT_BLOCK.txt`](../BASIC_PROJECT_BLOCK.txt) intentionally stops before this advanced layer. Advanced users may still install the templates manually using the fallback below, but they should not copy `releasecheck.yml` blindly without identifying the real release process.

## Manual fallback

1. Put your durable project memory in `NOTES.md` using `START_HERE.md` as the short guide.
2. Copy `statefile.yml` to `.github/workflows/statefile.yml`.
3. Copy `releasecheck.yml` to `.github/workflows/releasecheck.yml`.
4. In `releasecheck.yml`, replace `dist` with the actual release folder. If that folder is generated rather than committed, add the project's existing build step before the folder check.
5. Optionally copy and customize `releasecheck.example.json` as `releasecheck.json`, then add `manifest: releasecheck.json` to the action step.
6. Open a pull request. Confirm the memory check passes and review the complete diff.
7. Run the release workflow manually and confirm one green CI result. Only then, if desired, add the version-tag trigger used by the project.

## Honest limits

These tools do **not** prove that project notes are factually true, detect every kind of confidential information, replace human diff review, or remove secrets from old Git history. `releasecheck` only examines the folder you configure. Treat a passing check as evidence that specific mechanical tests passed—not as blanket approval.

**The Reader Kit guides the work. statefile checks the memory. releasecheck checks what you ship.** The complete behavioral protocol is in Appendix C of *Never Start from Scratch*; it is not reproduced here.
