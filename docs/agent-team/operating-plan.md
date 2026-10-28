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
and relevant security implications. Changes in the sensitive categories listed
in [the PM role](roles/pm.md) step 5 receive an independent reviewer who did not
author the implementation.

Use isolated writer worktrees and immutable base/review SHAs. Missing decisions
or conflicting contracts return to the assigning manager. Record every attempt;
correction counters survive retries. Task acceptance is separate from merge and
deployment approval.

For multiple repositories, a parent assignment links the child task IDs and
explicit handoff acknowledgements. Cross-system acceptance waits for the required
reviewed child results. Repository-local work can remain local.

A designated status writer reconciles host activity, descendants, commits, and
worktrees before reassigning work. An expired wait or missing response is not
proof that an agent stopped.

Remote disconnection neither cancels approved work nor grants new authority.
Pause stops new dispatch and checkpoints affected tasks; a coordinated pause
reaches every PM and its descendants. Cancellation can leave partial
files/processes. For a scope change, invalidate only affected packets and
approvals, then issue revised packets.

On restart, reconcile recorded attempts with live processes and retained
worktrees before resuming. Unknown liveness means blocked pending inspection,
not a free slot; an abandoned assignment needs a new explicit owner. Avoid
duplicate workers after an uncertain launch or restart.

Prompt rules and example profiles are cooperative policy. Document which limits
are enforced by the host, which require a separate control, and which depend on
human supervision. Record untested behavior explicitly.

## Closure

The assigning manager closes temporary task threads: leaders close the worker
and reviewer tasks they assigned; PMs close accepted leader and reviewer tasks.
A temporary coordinator is closed after its deliverable is accepted by its
supervising owner, or by the human or coordinating conversation when no agent
supervises it.

Before closure:
1. Persist the result, relevant implementation/review SHAs, and review disposition
   in the owning repository's task records.
2. Confirm acceptance, or explicitly record cancellation/supersession and assign
   any remaining follow-up to an owner. Unresolved review work stays active.
3. Reconcile host task state and descendants. Require no active/queued work,
   pending child runs, unresolved questions, or pending approvals. A completed
   assistant turn alone does not satisfy this check.
4. Close eligible descendants before their temporary parent using the host
   adapter, then verify and record the resulting state.

On T3, use [the settlement procedure](adapters/t3.md#thread-settlement). On other
hosts, use the adapter's supported equivalent or report that manual cleanup is
required. Settlement is an organizational action, not proof of task acceptance
or permission to merge/deploy.

Keep ongoing PM and planning conversations active between assignments; a PM's
completed run is no reason to settle it. Retain branches, commits, and worktrees
unless their cleanup is separately approved. A later correction gets a new
task/review round with the prior context; settled history remains part of the
evidence chain.
