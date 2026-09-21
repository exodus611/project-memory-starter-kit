# Closing routine

Use this before ending a session and whenever a material checkpoint is needed before context compaction, a model switch, or a transfer.

Before ending a session:

1. **Decisions:** What did we decide today? Add the decision and its reason.
2. **Failures:** What did we try that did not work? Record the reason not to retry.
3. **State:** What is different now? Update the current state and verification date.
4. **Next three:** Write the three concrete tasks for the next session, in priority order.
5. **Evidence:** List files changed, checks or tests run, and anything that remains uncertain.
6. **Commit:** Review the update and diff, commit it with a descriptive message, and confirm the committed record is accurate.

Optional last instruction to the AI:

```text
Before we finish, prepare a draft checkpoint with: decisions and reasons;
failures and why not to retry; state changes and verification; next three tasks;
files changed, checks run, remaining uncertainty; and a proposed commit message.
This is a draft for the repository handoff; I will verify it before committing.
```

The AI drafts. You verify. You own the committed record.
