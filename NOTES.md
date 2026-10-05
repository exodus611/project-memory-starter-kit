# Project Notes — Project Memory Starter Kit

## Goal and definition of done
Publish a beginner-friendly public companion that clearly separates: the 267-word manual card, the useful automatic Basic Block, and the complete Reader Kit in the book. Done means the canonical and compatibility Basic files match, the ZIP contains only `START_HERE.md`, links and English text validate, GitHub Pages is green, and product claims remain accurate.

## Current state — last verified 2026-10-04

- Public Basic Block v1.2 is live from commit `c1b6b6e99c6446a406a4712263348a3b1adc89c8`; a locally prepared clarification brings the next copy to 755 words by explaining that a new-project brief or current task belongs directly below the block in the same message. It still intentionally omits `statefile`, `releasecheck`, and mid-session checkpoints.
- `BASIC_PROJECT_BLOCK.txt` is canonical and `UNIVERSAL_PROJECT_BLOCK.txt` is a byte-identical compatibility copy.
- `project-memory-starter-kit.zip` contains only the 267-word `START_HERE.md` manual card.
- GitHub Pages run `37220039069` completed successfully for commit `c1b6b6e`.
- The `automation/` templates remain public for inspection and for use by the complete Universal Master Block; the Basic Block does not install them.
- The encrypted Reader Kit copy page is live from commit `35eb9bd1f21491e5945b1ae8ef153a349fca3293`. Project-memory run `37269435489` and Pages run `37269434480` completed successfully. Live ciphertext decrypts to the exact canonical SHA; wrong-code rejection passes; neither plaintext nor reader code is present in the public HTML. Human mobile copy/download verification is still pending.

## Repository map

- `BASIC_PROJECT_BLOCK.txt` — canonical public Basic Block.
- `UNIVERSAL_PROJECT_BLOCK.txt` — compatibility URL; must remain identical to the canonical file.
- `ONE_BLOCK_SETUP.md` — source and explanation for the Basic Block.
- `START_HERE.md` — manual 267-word card and the only ZIP member.
- `index.html` — GitHub Pages landing page.
- `automation/` — advanced public workflow templates, not part of Basic installation.

## Decisions

- 2026-10-04 — Keep Basic genuinely useful for ordinary projects but reserve automated checks, checkpoints, context protection, handoff, advanced permissions, recovery, and the full security protocol for the complete Reader Kit.
- 2026-10-04 — Keep the ZIP as a one-file manual card; do not label it as the automatic Basic Block.
- 2026-10-04 — Keep public automation sources accessible, while stating clearly that Basic does not install them.

## Failed approaches — do not repeat

- Do not make Basic intentionally unusable to force conversion.
- Do not claim workflow `paths:` excludes a third-party file from `statefile` scanning; it only controls workflow triggering.
- Do not describe the one-file ZIP as the automated block.

## Known problems

- This reviewed update repairs the stale README reference from Basic v1.1 to v1.2.
- Repository-internal project-memory controls are installed. Latest strict project-memory run `37229610504` and Pages run `37229610272` completed successfully on commit `7ab02b8`.
- The complete Master Block is about 11,000 characters and spans roughly nine Kindle screens. The encrypted copy page is now live and machine-verified, but it is not yet linked from the book and still needs a human mobile copy/download test.
- The manual-only release preflight passes locally and still needs one deliberate GitHub dispatch.

## Next three tasks

1. Test the live encrypted page on a real mobile browser; confirm one-tap unlock, full copy, and TXT download.
2. Run the manual GitHub release preflight and record the result before adding any automatic trigger.
3. Only after the human mobile test passes, add the one-tap link and fallback reader code to the private Kindle manuscript and consider one final EPUB update.

## External services and dependencies

- GitHub Pages hosts the public companion.
- `statefile` v0.2.3 is pinned at `8e9dc90f98ee181b885fec72ce7f771b66d60057`.
- `releasecheck` v0.1.1 is pinned at `b565180b141658b5370225f10e3775b50c36059e`.

## Recent sessions

- 2026-10-05 — Re-encrypted the Reader Kit page from the clarified canonical Master Block so the copied/downloaded block includes the same-message project-brief guidance and matches canonical SHA `af8871d9…`. The reader code and URL remain unchanged.
- 2026-10-05 — Clarified the one-block input flow across the Basic source, landing page, README, and encrypted copy page: paste the block first, then add a plain-language new-project brief or current task directly below it in the same message. Existing repositories may omit that brief when evidence already establishes the goal.
- 2026-10-05 — Published the encrypted mobile copy page at commit `35eb9bd`. Strict project memory and Pages deployment are green. A fresh fetch of the live ciphertext decrypts to canonical SHA `af8871d9…`; wrong-code rejection passes; public HTML exposes neither plaintext nor the 100-bit reader code. The Kindle manuscript remains unchanged pending a human mobile test.
- 2026-10-04 — Installed durable memory, concise repository instructions, strict SHA-pinned `statefile`, and a manual-only pinned `releasecheck`. Local artifact checks and release preflight pass; the latest strict project-memory and Pages runs are green on commit `7ab02b8`.
