# Continue after provider quota exhaustion

After the team workflow is explicitly enabled, use this procedure when
subscription quota blocks an assigned role. It applies
in either provider direction and on both execution paths. This is a supervised
recovery procedure, not automatic failover or proof of runtime recovery.

The user chooses whether to wait or continue with another provider. Writing or
adopting this procedure alone does not authorize a provider switch. Existing
scope, subscription-only billing, correction limits, review requirements, and
publication gates from [the operating plan](operating-plan.md) remain in force.
Keep automatic provider fallback and automatic active-thread changes disabled.

## 1. Stop affected work and preserve evidence

The assigning manager stops new affected dispatches and marks the assignment
blocked with an observed timestamp and a sanitized error reference. If the PM
cannot run, the human or this coordinating conversation may preserve evidence
and prepare the handover; that does not create a second accountable PM.

Distinguish confirmed quota exhaustion from authentication failure, an unknown
provider error, and a full context window. Record unknown when the cause or
reset time is not exposed. A context-window issue alone does not require another
provider. Authentication failures need access repair through the authorized
subscription route; do not substitute API credentials.

Inspect live task/descendant state, processes, worktrees, and Git state. A failed
inference call does not prove that tools or children stopped. Follow
the active host's recovery procedure (on T3,
[pause and recovery](adapters/t3.md#pause-cancellation-recovery)) to
checkpoint or cancel affected execution, then verify it stopped. Unknown
liveness blocks replacement; it is not a free slot.

Preserve partial edits, untracked files, and test output. Commit only if already
authorized. Otherwise retain the worktree and record the exact diff/file
inventory, including binary or untracked artifacts needed to resume. Keep
credentials and private account details out of records. If the exhausted agent
cannot write a checkpoint, reconstruct it from inspected artifacts and label
unverified claims as unknown.

## 2. Record the checkpoint and user decision

The task's status writer records the following under
`tasks/<task-id>/provider-continuation-<attempt>.md`. This is the recovery packet;
link it from the revised [brief](templates/brief.md) and task status.

| Field | Required evidence |
| --- | --- |
| Identity | Task, old attempt, role, accountable PM/status writer, dependencies |
| Failure | Observed time, sanitized cause/evidence, known reset time or unknown |
| Source | Selected profile, provider, model/options, full governing policy SHA |
| Workspace | Repository identity, branch/worktree, base and current full HEAD |
| Partial work | Changed/untracked file inventory, retained artifacts, unfinished operations |
| Progress | Completed criteria, remaining steps, assumptions and unresolved decisions |
| Validation | Commands actually run, results, evidence paths, checks not run |
| Reviews | Authors, reviewed SHAs, findings/dispositions, correction rounds already used |
| Runtime | Task/descendant/process readbacks, pending requests, slots and their owner |
| Authority | Existing scope/commit/publication approvals and remaining gates |
| Decision | Wait or switch; user approval evidence and its exact scope |
| Target | Role(s), profile mapping, provider/model/options, task-only or PM default selection |
| Resumption | New attempt/owner, verified workspace and target readbacks, next action |

Offer the concrete target role mapping from a configured, enabled profile
already approved for this project. The [Codex](profiles/codex.example.json) and
[Claude](profiles/claude.example.json) files are disabled examples, not runnable
recovery targets. Complete [setup](rollout.md) before selecting a derived profile.
Resolve supported model/options and subscription access before execution. Unsupported or unavailable targets stay
blocked; do not silently approximate settings or choose a third provider.

Wait: retain the packet and resume only after access and live state are checked.
Switch: require explicit approval naming the affected roles and target selection.
An already recorded approval covering this exact switch need not be requested
again. Switching one child role leaves the repository default and other roles
unchanged. Record this approved role-specific exception in the revised brief;
a proposed new profile must complete normal policy adoption before runtime use.

## 3. Transfer ownership without duplicate execution

| Blocked role | Continuation |
| --- | --- |
| Worker | The manager assigns one replacement attempt with the partial-work packet and the same acceptance criteria. |
| Team leader | Hand over the technical plan, integration state, child inventory and pending reviews. Verify routing/ownership of existing children; if the host cannot transfer them, reconcile and close/supersede them before replacement dispatch. |
| Reviewer | Start a fresh review round on the exact candidate SHA with all prior findings. An interrupted review is not PASS. |
| PM | Keep the same accountable PM thread; configure it only outside an active run, then read back its binding and exact options before resuming. |

The manager records supersession and the new attempt; the authorized ledger
owner reconciles slots before dispatch. New attempts do not reset correction
counts or erase unresolved findings. Retain old records and worktrees.

The replacement writer gets an isolated workspace and verifies its actual base
and inherited partial changes against the packet before editing. A new worktree
does not inherit dirty changes. Transfer only inventoried artifacts after
confirming the old writer stopped, or reuse the retained checkout only when
the host can explicitly bind it safely. Mismatch or unsupported binding blocks
resumption. Never discard edits to obtain a clean checkout.

For PM handover, checkpoint and reconcile affected children first; record who
owns any unaffected live tasks. Verify the selected profile and policy, existing
PM identity, repository binding, pending approvals and ledger ownership. The
human or authorized coordinating conversation performs configuration while that
PM has no active run, queued turn, or unresolved pending request. Record each
request's disposition rather than treating the switch as approval. Use the
active host's configuration and readback procedure; on T3, use
[provider continuation](adapters/t3.md#provider-continuation).
If the host cannot reconfigure the existing PM identity safely, remain blocked
for a separately approved handover plan.
If configuration/readback fails, stay blocked rather than creating another PM.

## 4. Resume, review, and close

The replacement acknowledges the packet, role limits, approvals, actual Git
state, required readings and next step before proceeding. Recheck incomplete or
unreliable tests and any checks invalidated by further edits. Preserve valid
evidence with its original SHA and provenance.

Retain independent review wherever required. An agent that authored or corrected
the deliverable cannot act as its independent reviewer; changing provider or
opening another thread does not erase that authorship. If only one provider is
available, use a fresh non-author reviewer within that provider under an approved
selection. If the task requires cross-provider review, obtain an explicit change
to that requirement or wait; do not silently downgrade it.

Resume only when the recorded target, subscription access, ownership, workspace,
live state and approval checks all pass. Keep merge/push/deploy decisions separate.
Close superseded temporary attempts through [the closure checks](operating-plan.md#closure)
only after remaining work is assigned and pending work/requests are resolved.
The ongoing PM remains active. Quota returning does not trigger an automatic
switch back; any later switch follows this same decision and handover procedure.
