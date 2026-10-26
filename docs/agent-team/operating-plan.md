# Project agent-team operating plan

Status: INACTIVE TEMPLATE. Configure with the human before dispatch. Keep this
file in the project's policy repository; reference its committed SHA in tasks.

## Required project decisions

- Team scope and purpose: REQUIRED
- Participating repository identities and policy location: REQUIRED
- One accountable PM per repository; coordination PM if needed: REQUIRED
- Existing planners, task handoffs, and replacement procedure: REQUIRED
- Human approval gates for scope, architecture, risk, commits, publication,
  merges, deployment, spending, and live testing: REQUIRED
- Selected configured provider/model profiles: REQUIRED
- Maximum active leaders/workers and how all repositories share that limit: REQUIRED
- Maximum unsuccessful correction rounds and escalation owner: REQUIRED
- Active-work checkpoint/deadline and actual enforcement mechanism: REQUIRED
- Subscription/API spending policy and measurement limits: REQUIRED
- Shared contract ownership, compatible rollout, and rollback: REQUIRED (or none)
- Pause/cancel handling, remote disconnection, and restart reconciliation: REQUIRED
- Pilot scope, acceptance evidence, and remaining supervision: REQUIRED

## Workflow rules

A PM assigns a bounded deliverable with acceptance criteria. Its leader creates
technical/test plans, delegates complete task packets, reviews worker evidence,
and verifies the integrated result. The PM reviews architecture, completeness,
and relevant security implications. Sensitive changes receive an independent
reviewer who did not author the implementation.

Use isolated writer worktrees and immutable base/review SHAs. Missing decisions
or conflicting contracts return to the assigning manager. Record every attempt;
correction counters survive retries. Task acceptance is separate from merge and
deployment approval.

For multiple repositories, a parent assignment links the child task IDs and
explicit handoff acknowledgements. Cross-system acceptance waits for the required
reviewed child results. Repository-local work can remain local.

The named PM owns the root HANDOVER.md summary during team operation. Other
roles write task-specific results. A designated status writer reconciles host
activity, descendants, commits, and worktrees before reassigning work. An expired
wait or missing response is not proof that an agent stopped.

Remote disconnection neither cancels approved work nor grants new authority.
Pause stops new dispatch and checkpoints affected tasks; cancellation can leave
partial files/processes. Reconcile before resuming. Avoid duplicate workers after
an uncertain launch or restart.

Prompt rules and example profiles are cooperative policy. Document which limits
are enforced by the host, which require a separate control, and which depend on
human supervision. Record untested behavior explicitly.
