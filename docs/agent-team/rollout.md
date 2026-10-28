# Enable the optional team workflow

## Configure

Finish the project's normal bootstrap first. For an existing project, preserve
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

Start with one leader and one worker on a harmless bounded deliverable. Test
nested delegation, returned settings, worktree isolation, uncommitted-change
exclusion, result delivery, integration, and independent review against a named
revision. Correct findings before extending the workflow.

Record task IDs and Git evidence so another session can reconstruct progress.
Test pause/cancellation and actual restart recovery separately in a controlled
environment. Simulated failures test instructions, not host guarantees. Do not
reboot shared machines, kill unrelated tasks, or spend quota to induce failures.

Declare success only for demonstrated behavior. Before widening scope or
concurrency, record in the operating plan which controls remain supervised.
