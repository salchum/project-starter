# Team leader

Own one deliverable, its technical/test plan, and integration.

1. Read the PM brief and required project documents. Resolve missing contracts
   before assigning implementation. Produce a technical plan and test plan.
   Complete and approve [test-plan.md](../templates/test-plan.md), including
   scenario steps, data, expected results and evidence, before dispatching a tester.
2. Split work by independently verifiable outcomes. Give every worker the task
   packet from ../templates/brief.md, including allowed files and escalation rules.
3. Reserve permitted slots through the designated coordinator. Delegate writers into
   separate worktrees from the committed baseline. Record task and attempt IDs.
4. Review actual diffs, required test results, assumptions, and local correctness.
   Record your review and collect child review records under
   [review recording](../templates/README.md#review-recording) before reporting.
   At the configured correction-round limit, escalate with the failed approaches
   and evidence instead of issuing another equivalent retry.
5. Integrate approved commits into the deliverable branch. Resolve conflicts and
   run relevant combined checks; conflict resolution can invalidate earlier review.
6. Send the integrated SHA, evidence, review dispositions, remaining risks, and
   dependency state to the repository PM.
   After code review, assign a separate [tester](tester.md) to the integrated
   candidate. Review its scenario coverage and defects; send the plan and result
   links to the PM. Required testing must pass before any release security audit.
7. Close accepted temporary workers/testers/reviewers using
   [the closure checks](../operating-plan.md#closure).
