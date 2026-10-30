# Enable the optional team workflow

## Configure

During normal bootstrap, record the team choice using the selection procedure
below. Finish bootstrap before runtime activation. For an existing project, preserve
its requirements and deployment rules rather than replacing root files wholesale;
import AGENTS and HANDOVER ownership changes as targeted patches. Upgrading
project-starter does not update repositories already created from it.

Complete operating-plan.md with the human. For multiple repositories, choose
the policy repository and resolve each checkout by Git identity. Select or
reconcile existing PM threads before creating new ones.

Copy a disabled profiles/*.example.json to a project-specific profile. Resolve
provider/model IDs and options from the actual host catalog, verify permitted
billing, and explicitly enable the configured copy. Example names and settings
are not availability or quality guarantees. Commit the policy and record its SHA.

### Provider and role selection

1. Ask the human to choose: no team (ordinary single-agent work), single-provider
   team, or multi-provider team. Record the answer in the project's STATUS.md.
   No team or an unanswered choice leaves examples disabled and skips team setup.
2. For a team, ask which installed providers/accounts the project may use and
   confirm the host and authorized billing route. Read the host's live model
   catalog and option schema. If access or a catalog is unavailable, record the
   desired choices as pending; do not invent availability or launch a probe.
3. Let the human choose the provider, exact model and explicit supported options
   for PM, team leader, worker, independent reviewer and tester. Reasoning names and
   levels are provider-specific; never silently translate unsupported settings.
   In single-provider mode every enabled role must use the selected provider
   instance. Multi-provider mode permits a separate selection for each role.
   One provider/model may serve several roles through separate assignments;
   authors still cannot act as their own independent reviewers.
   For bounded test execution, propose a lightweight supported model with low
   reasoning; let the user confirm it. Validate that the chosen model supports
   the actual test tools. Compare cost only using relevant observed/account
   evidence; API token prices do not measure subscription quota or task cost.
   Never change provider to obtain a cheaper tester in single-provider mode.
4. Ask whether workers need one model or several selectable variants. For several,
   create separate complete profile variants and agree who selects each variant
   per task and what rationale is recorded. Keep one worker selection per packet.
   Additional specialist roles, such as a security auditor, require their role,
   trigger/gate and report format to be defined in project policy before enabling;
   then let the human select their provider/model/options by the same rules.
5. Present the complete role mapping, worker-selection rule, limits, reporting
   owner and remaining approvals for confirmation. Record the confirmed choice
   in operating-plan.md and project-specific profile copies. Preserve the
   disabled example files. Keep configured copies disabled while any validation
   or approval remains unresolved. A selection is not an automatic provider
   switch, permission to create threads or permission for API fallback.
6. Validate configured profile JSON, all role mappings and options, permitted
   subscription access and host support. Single-provider mode must contain
   exactly the selected provider instance; multiple-provider mode must contain
   only approved instances. Complete the operating plan, obtain required commit
   approval, then enable the confirmed configured copies and commit the policy.
   Proceed to binding/preflight below only after bootstrap and these gates finish.

If the human already supplied these choices, reconcile and confirm the completed
mapping rather than repeating the interview. Existing projects may use this
section directly; a template update does not activate teams or change live tasks.

## Bind and preflight

Use the host adapter to bind the PM thread to the correct repository/worktree.
Apply the profile through actual host model-selection settings. JSON files alone
do not configure the host. Before delegation, send the PM the
[readiness prompt](#pm-readiness-prompt).

Adopting a profile does not reconfigure running threads on its own. Switch an
existing PM's provider or profile only after human approval, on the same PM
thread outside an active run, through the host adapter (T3: step 6 of
[PM binding](adapters/t3.md#preflight-and-pm-binding)). Read back the provider,
model, and options before the PM resumes from its recorded handover.

Every child receives a complete packet, including policy and source SHAs, allowed
scope, required checks, approvals, and report location. Match the parent's actual
baseline before launching a writer. Child preflight verifies its own initial SHA.

### PM readiness prompt

Send after the operating plan and profile are configured and committed. Replace
every REQUIRED field first.

```text
Act as repository PM for REQUIRED verified repository.
Read AGENTS.md and docs/agent-team/README.md.
Policy checkout: REQUIRED absolute path; policy SHA: REQUIRED full commit.
Human-selected profile: REQUIRED file; host model/options: REQUIRED explicit selection.

Perform readiness inspection only. Reconcile existing planners and unfinished
tasks, verify project/worktree/branch/base SHA, profile support, authentication
and permitted billing, approvals, and limit/recovery enforcement. Report any
missing prerequisite before delegation or application changes.

Record the selected PM identity only after ownership is reconciled. Preserve
project-specific publication/deployment rules. A user disconnect grants no approval.
```

## Supervised pilot

For a light-path trial, use a harmless bounded deliverable with the PM or one
executor and the review required by the brief. This does not test nested
delegation. For a standard-path pilot, use one leader and one worker. Test
nested delegation, returned settings, worktree isolation, uncommitted-change
exclusion, result delivery, integration, and independent review against a named
revision. Correct findings before extending the workflow.

Record task IDs and Git evidence so another session can reconstruct progress.
Test pause/cancellation and actual restart recovery separately in a controlled
environment. Simulated failures test instructions, not host guarantees. Do not
reboot shared machines, kill unrelated tasks, or spend quota to induce failures.

Declare success only for demonstrated behavior. Before widening scope or
concurrency, record in the operating plan which controls remain supervised.
