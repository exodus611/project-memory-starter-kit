# Project Memory Quick Start Card

A short public companion to *Never Start from Scratch: Give Your Projects a Memory That Never Forgets* by Daniel Marlow.

Open [`START_HERE.md`](START_HERE.md) to try the basic method: create a small project map, use one opening message, and leave a reviewed handoff at the end.

Open your project in an AI coding agent and paste [`BASIC_PROJECT_BLOCK.txt`](BASIC_PROJECT_BLOCK.txt). It decides automatically whether to install, repair, or begin a normal project session. Installation uses one grouped question round, one installation approval, and one separate commit/push approval; later sessions skip setup and move directly to the next task.

The public Basic Block does not install automated checks. The [`automation/`](automation/) folder remains public so readers and advanced users can inspect the GitHub Actions templates used by the complete Universal Master Block: [`statefile`](https://github.com/exodus611/statefile) and [`releasecheck`](https://github.com/exodus611/releasecheck). When used, those checks run in the user's repository; there is no hosted service or upload to the author.

The same block detects whether the current product has full repository and terminal access, read-only GitHub access, uploaded files, or chat only. Full automatic installation requires a coding-agent environment that can edit files and run commands; less capable chats return the strongest truthful fallback rather than claiming work they could not perform.

**The Reader Kit guides the work. statefile checks the memory. releasecheck checks what you ship.** `BASIC_PROJECT_BLOCK.txt` is the canonical public Basic Block v1.2; the older `UNIVERSAL_PROJECT_BLOCK.txt` URL is retained as an identical compatibility copy, not a second edition. The canonical complete Universal Master Block v3.1 is included inside the book. It contains the full `NOTES.md` template, repository instructions, opening, working, checkpoint and closing messages, connected-agent guidance, permissions model, and the complete security review.

- Read or download the Quick Start Card: https://exodus611.github.io/project-memory-starter-kit/
- Copy the one project block: [`BASIC_PROJECT_BLOCK.txt`](BASIC_PROJECT_BLOCK.txt)
- Explanation and platform modes: [`ONE_BLOCK_SETUP.md`](ONE_BLOCK_SETUP.md)
- Automation details and manual fallback: [`automation/README.md`](automation/README.md)
- Book: https://www.amazon.com/dp/B0HKVZ3RSG

The free Basic Block is enough for an ordinary project: it creates project memory and maintains a simple start-to-close loop. It intentionally omits automated freshness and release checks. The complete Reader Kit is for long sessions, context compaction, mid-session checkpoints, `statefile`, `releasecheck`, multiple agents, evidence-based handoffs, tighter permission boundaries, recovery after failures, and the full security protocol.

Automation checks mechanical properties only. Neither tool proves factual truth, detects every kind of confidential information, replaces human diff review, or cleans old Git history. You may copy, adapt, and use these public files for your own personal and commercial projects.

*Unofficial guide. Not affiliated with or endorsed by GitHub, Inc. GitHub® is a registered trademark of GitHub, Inc.*
