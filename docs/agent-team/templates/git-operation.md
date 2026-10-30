# REQUIRED task — Git operation packet

- Accountable PM / status and result writer / result path: REQUIRED
- Policy SHA / selected profile / git-worker provider, model and explicit options: REQUIRED
- Repository remote identity / branch / verified worktree binding: REQUIRED
- Expected local HEAD / expected destination local or remote SHA (or absent): REQUIRED
- Ordered permitted operations (commit / fast-forward / push only): REQUIRED
- Commit file allowlist and approved diff/artifact fingerprints / message: REQUIRED or not applicable
- Exact source SHA / destination branch-ref / remote: REQUIRED as applicable
- Purpose (save work / publish for review / integrate accepted result / release): REQUIRED
- Approval evidence and scope / remaining approval gates: REQUIRED
- Review, test and audit evidence references / applicability: REQUIRED
- Push-triggered workflow/deployment effects and authorization: REQUIRED or none
- Required check commands / permitted environment / acceptance criteria: REQUIRED
- Exclusive checkout/ref ownership and prior writer stopped / slot reservation: REQUIRED
- Dependencies / stop conditions / next owner on failure: REQUIRED

## Result

- Timestamp / actual model-options readback: REQUIRED
- Operations attempted / command exit status / checks and evidence: REQUIRED
- Before and after local SHA / resulting tree / remote-ref readback: REQUIRED as applicable
- Files included / remaining dirty files / scope verification: REQUIRED
- Outcome (completed / blocked / failed / uncertain): REQUIRED
- Blocker / next owner / action required from PM or user: REQUIRED or none

The PM verifies this record and includes its outcome in the user summary.
Completion proves only the named Git operation, not deployment success.
