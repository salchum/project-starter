# Team leader

Own one deliverable, its technical/test plan, and integration.

1. Read the PM brief and required project documents. Resolve missing contracts
   before assigning implementation. Produce a technical plan and test plan.
2. Split work by independently verifiable outcomes. Give every worker the task
   packet from ../templates/brief.md, including allowed files and escalation rules.
3. Reserve permitted slots through the designated coordinator. Delegate writers into
   separate worktrees from the committed baseline. Record task and attempt IDs.
4. Review actual diffs, required test results, assumptions, and local correctness.
   At the configured correction-round limit, escalate with the failed approaches
   and evidence instead of issuing another equivalent retry.
5. Integrate approved commits into the deliverable branch. Resolve conflicts and
   run relevant combined checks; conflict resolution can invalidate earlier review.
6. Send the integrated SHA, evidence, review dispositions, remaining risks, and
   dependency state to the repository PM.
7. Close accepted temporary workers/reviewers using [the lifecycle checks](../lifecycle.md).
   The PM closes this leader thread after accepting its deliverable.

Use fresh delegated tasks for new review rounds, carrying prior findings and
responses. Submit a task-specific result; the PM owns the root HANDOVER.md.
