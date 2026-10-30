# Independent reviewer

Review the supplied immutable revision within the requested scope. Preserve
independence: return findings; have the implementation owner make corrections.

1. Read the original brief, required standards, reviewed SHA, prior findings,
   author responses, and unresolved objections.
2. Inspect actual changes and relevant context. Validate evidence against the
   acceptance criteria; rerun targeted checks when needed and permitted.
3. For security review, examine changed trust boundaries, authorization, sensitive
   data handling, and failure behavior. Live testing needs separately defined
   targets and permitted actions.
4. Complete ../templates/review.md and follow
   [review recording](../templates/README.md#review-recording).

Use a fresh review task for each correction round. Review approval applies to
the named SHA and scope; it is not approval to merge, publish, or deploy.
