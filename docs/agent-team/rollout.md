# Enable the optional team workflow

## Configure

Finish the project's normal bootstrap first. For an existing project, preserve
its requirements and deployment rules rather than replacing root files wholesale.
Choose whether a team is needed; keep the module inactive when it is not.

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
do not configure the host. Use prompts/bootstrap-pm.md for readiness inspection
before delegation.

Adopting or switching a profile reconfigures no running thread. To move an
existing PM to another provider or profile, keep the same PM thread: after the
human approves the policy change, configure that thread while it has no active
run, read back its provider, model, and options, then resume from the recorded
handover. The switch never creates a second permanent PM for the repository.

Every child receives a complete packet, including policy and source SHAs, allowed
scope, required checks, approvals, and report location. Match the parent's actual
baseline before launching a writer. Child preflight verifies its own initial SHA.

## Supervised pilot

Start with one leader and one worker on a harmless bounded deliverable. Test
nested delegation, returned settings, worktree isolation, uncommitted-change
exclusion, result delivery, integration, and independent review against a named
revision. Correct findings before extending the workflow.

Record task IDs and Git evidence so another session can reconstruct progress.
Test pause/cancellation and actual restart recovery separately in a controlled
environment. Simulated failures test instructions, not host guarantees. Do not
reboot shared machines, kill unrelated tasks, or spend quota to induce failures.

Declare success only for demonstrated behavior. Keep unsupported concurrency,
deadline, spending, and recovery controls under supervision; implement additional
enforcement before claiming unattended reliability.

## Adopt and maintain

Use the pilot evidence to decide the next scope and permitted concurrency.
Commit project-specific adaptations locally, then publish only when authorized.
Keep operational task records in the project, not in this reusable starter.

When importing this module into an existing repo, review AGENTS and HANDOVER
ownership changes as targeted patches. Upgrading project-starter does not update
repositories already created from it.
