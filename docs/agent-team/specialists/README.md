# Specialist teams

Read this policy when configuring, assigning, recovering or accepting DevSecOps
or UI/UX work. Then read only [DevSecOps](devsecops.md) or [UI/UX](uiux.md),
the selected profile, the [specialist packet](../templates/specialist-task.md)
and the active [host adapter](../adapters/t3.md). Existing repository instructions,
review requirements and publication gates continue to apply.

## Ownership and routing

One repository PM retains repository acceptance, integration and shared HANDOVER
ownership. DevSecOps PM and Design Manager coordinate specialist services across
repositories; they are not second repository PMs. Each deliverable has one owner,
one status writer and explicit repository/file scope. Split cross-team work into
linked briefs. The Coordination PM arbitrates dependencies and priorities; when
absent, the human designates a task coordinator among the managers.

The human may direct a specialist manager or the coordinator. Inspect conflicting
assignments and dependencies before execution, record the task and notify the
coordinator if present. Reuse approvals covering that scope; routing through a
coordinator does not require duplicate approval. Escalate unresolved priority,
contract or business decisions to the human. Report specialist results through
the manager to the coordinator when present and to the user.

Shared strategies, standards and journeys belong in the designated policy/system-
design repository. Runnable pipeline/IaC, components and tests belong in their
owning repositories. Name an owner and canonical path per artifact; link instead
of copying competing sources. Only designated owners edit shared indexes.

## Selection and task freeze

During [setup](../rollout.md), record approved providers, default packages and
permitted overrides. Reuse an explicitly adopted default for new tasks unless
the human chooses another package. Ask only for missing, ambiguous or unavailable
choices. Disabled examples are not runtime targets. Verify exact provider/model/
options, subscription access and host support before dispatch; catalog presence
is not quota or execution evidence. No paid API fallback.

Freeze the COMPLETE role mapping, including workers, in the parent task and every
child packet before work begins. No provider/model/options changes within that
specialist task. A default amendment affects future tasks only. Existing general
team tasks keep their own policy and recovery rules.

Quota or access failure blocks affected execution. Use the checkpoint, live-state,
artifact preservation and ownership checks in [provider continuation](../provider-continuation.md).
For these specialist tasks its in-task switch route is replaced by: wait, or
formally stop/supersede the old task and obtain explicit human approval for a
successor with a new complete package. Reconcile descendants/processes first;
unknown liveness blocks replacement. Link predecessor and successor, carrying
all findings, partial artifacts, approvals within their original scope and
correction counts. A new task ID cannot erase failures. No automatic switch back.

Each specialist manager has one active parent task during the pilot. Keep its
identity; change its package between tasks only outside active/queued runs and
after children, requests and ownership are reconciled. Verify configuration and
workspace readback through the adapter before resuming. New permanent top-level
threads require explicit creation authorization; policy adoption creates none.

## Capacity and closure

Specialists share the global ledger and limits with existing teams. Initial pilot:
one leader and one execution slot, sequentially, globally; no per-team allowance.
DevOps Engineer consumes leader capacity. Implementing designers, UX Engineer and
workers consume execution capacity shared with existing worker/tester/Git worker
roles. Managers are recorded coordinators; a manager implementing artifacts also
consumes an execution slot. Independent security/review assignments are recorded
and run sequentially after execution; a waiting parent retains task ownership
without pretending its child consumes no capacity. Record running versus waiting
activity and reserve through the existing ledger owner before dispatch.

Only after explicit global capacity expansion may up to two independent DevOps
workers or two UI/UX specialists run in parallel, with disjoint workspaces/targets
and resolved dependencies. Team ceilings never override stricter global limits.

Use light tasks for bounded work; activate only needed roles. Mandatory review
is not removed by choosing a light path. Escalate after two unsuccessful correction
rounds; checkpoint after 60 minutes of active work. Follow existing descendant-first
closure and settlement rules after durable reports, acceptance/supersession and
no pending work/requests. Ongoing managers remain available between assignments.
These are supervised conventions, not host-enforced locks or spending limits.

## Evidence and skills

Persist brief, decisions/reasons, useful progress, problems, attempted solutions,
standards, evidence, unresolved findings and handoff—not the entire transcript.
Every review round has a durable report under the existing [recording rules](../templates/README.md#review-recording).
Read-only reviewers return the complete report for its named owner to persist
unchanged. Manager summaries retain original verdicts and evidence references.

Report prepared, validated and applied separately, with exact candidate/environment,
commands actually run, results, untested scope and next owner. Unknown usage/cost
stays unknown. A local validation is not deployment success; a prototype is not
user-tested without real evidence. Keep secrets and private participant data out
of shared reports.

Use relevant installed skills after reading them. Skills do not expand authority
or silently replace project standards. Propose standard changes through a recorded
decision for the appropriate owner.
