# Project Notes — Project Memory Starter Kit

## Goal and definition of done
Publish a beginner-friendly public companion that clearly separates: the 267-word manual card, the useful automatic Basic Block, and the complete Reader Kit in the book. Done means the canonical and compatibility Basic files match, the ZIP contains only `START_HERE.md`, links and English text validate, GitHub Pages is green, and product claims remain accurate.

## Current state — last verified 2026-10-04

- Public Basic Block v1.2 is live from commit `c1b6b6e99c6446a406a4712263348a3b1adc89c8`; it is 698 words and intentionally does not install `statefile`, `releasecheck`, or mid-session checkpoints.
- `BASIC_PROJECT_BLOCK.txt` is canonical and `UNIVERSAL_PROJECT_BLOCK.txt` is a byte-identical compatibility copy.
- `project-memory-starter-kit.zip` contains only the 267-word `START_HERE.md` manual card.
- GitHub Pages run `37220039069` completed successfully for commit `c1b6b6e`.
- The `automation/` templates remain public for inspection and for use by the complete Universal Master Block; the Basic Block does not install them.

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
- Repository-internal project-memory controls are installed at commit `ff26c49e463d37311d08afd3747837df52274c16`. Strict project-memory run `37229521744` and Pages run `37229520432` completed successfully. The manual-only release preflight passes locally and still needs one deliberate GitHub dispatch.

## Next three tasks

1. Run the manual release preflight once on GitHub and record the result before adding any automatic trigger.
2. Keep the public product ladder accurate and avoid changing Basic or the complete Reader Kit without a material reason.
3. Update this memory whenever a public artifact, positioning claim, or workflow changes.

## External services and dependencies

- GitHub Pages hosts the public companion.
- `statefile` v0.2.3 is pinned at `8e9dc90f98ee181b885fec72ce7f771b66d60057`.
- `releasecheck` v0.1.1 is pinned at `b565180b141658b5370225f10e3775b50c36059e`.

## Recent sessions

- 2026-10-04 — Installed durable memory, concise repository instructions, strict SHA-pinned `statefile`, and a manual-only pinned `releasecheck`. Local artifact checks and release preflight pass; the first strict project-memory run and Pages deployment completed successfully on commit `ff26c49`.
