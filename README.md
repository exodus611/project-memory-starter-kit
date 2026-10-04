# Project Memory Quick Start Card

A short public companion to *Never Start from Scratch: Give Your Projects a Memory That Never Forgets* by Daniel Marlow.

Open [`START_HERE.md`](START_HERE.md) to try the basic method: create a small project map, use one opening message, and leave a reviewed handoff at the end.

For automatic setup, open your project in an AI coding agent and paste the single block in [`ONE_BLOCK_SETUP.md`](ONE_BLOCK_SETUP.md). The agent inspects the repository, asks only unresolved questions, requests one installation approval, creates and configures the project-memory checks, tests them, shows the diff, and then waits for separate commit/push approval.

The optional [`automation/`](automation/) add-on provides the underlying GitHub Actions templates for [`statefile`](https://github.com/exodus611/statefile) and [`releasecheck`](https://github.com/exodus611/releasecheck). The checks run in your own repository; there is no hosted service or upload to the author.

The same block detects whether the current product has full repository and terminal access, read-only GitHub access, uploaded files, or chat only. Full automatic installation requires a coding-agent environment that can edit files and run commands; less capable chats return the strongest truthful fallback rather than claiming work they could not perform.

**The Reader Kit guides the work. statefile checks the memory. releasecheck checks what you ship.** The complete Reader Kit is included inside the book. It contains the full `NOTES.md` template, repository instructions, opening, working, checkpoint and closing messages, connected-agent guidance, permissions model, and the complete security review.

- Read or download the Quick Start Card: https://exodus611.github.io/project-memory-starter-kit/
- Paste-once agent setup: [`ONE_BLOCK_SETUP.md`](ONE_BLOCK_SETUP.md)
- Automation details and manual fallback: [`automation/README.md`](automation/README.md)
- Book: https://www.amazon.com/dp/B0HKVZ3RSG

The Quick Start Card works on its own. Automation is optional and checks mechanical properties only. Neither tool proves factual truth, detects every kind of confidential information, replaces human diff review, or cleans old Git history. You may copy, adapt, and use these public files for your own personal and commercial projects.

*Unofficial guide. Not affiliated with or endorsed by GitHub, Inc. GitHub® is a registered trademark of GitHub, Inc.*
