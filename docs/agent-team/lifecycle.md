# Close temporary task threads

The assigning manager owns closure: leaders close worker/reviewer tasks they
assigned; PMs close accepted leader/reviewer tasks. A temporary coordinator is
closed by its supervising owner after its deliverable is accepted.

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

On T3, use the settlement procedure in [the adapter](adapters/t3.md#thread-settlement).
On other hosts, use the adapter's supported equivalent or report that manual
cleanup is required. Settlement is an organizational action, not proof of task
acceptance or permission to merge/deploy.

Keep ongoing PM and planning conversations active even between assignments.
Retain branches, commits, and worktrees unless their cleanup is separately
approved. A later correction gets a new task/review round with the prior context;
settled history remains part of the evidence chain.
