# Security checklist

Before every commit, ask:

- Does any file contain a password, API key, token, private SSH key, credential, payment detail, or personal identification information?
- Is the repository visibility correct for the material inside it?
- Would I be comfortable if this file became public tomorrow?
- Does an AI tool, integration, or deploy key have more access than this task requires?
- If write access is enabled, do I review the proposed diff before it is committed?

## Rules

- Keep the project map and logic summary in `NOTES.md`; keep the full authorized project record in the repository, and keep secrets in an approved secret manager or GitHub Secrets.
- Keep a deploy key read-only unless the workflow genuinely needs to write; if write access is enabled, review every proposed diff before committing.
- Never paste a private key or token into a chat or repository.
- If a secret is committed, revoke or rotate it immediately. Removing the line does not remove it from history.
- Do not put confidential client data in `NOTES.md` merely because the repository is private.
