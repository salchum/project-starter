# Optional agent-team workflow

This module is opt-in. Normal project bootstrap and single-agent work continue
through the root AGENTS.md and INIT.md. Reading this folder does not enable a team.

For setup, follow [the rollout guide](rollout.md). Before dispatch, complete
[the operating plan](operating-plan.md) for the project and commit the policy.
The human decides whether a team is appropriate and approves its authority.

INIT.md offers no team, a single-provider team, or a multi-provider team.
Use [provider and role selection](rollout.md#provider-and-role-selection) to
configure the human's model choices; the shipped examples are not fixed staffing.

## Assignment entry point

1. Read the current repository's AGENTS.md and required project documents.
2. Verify the assigned role, repository, committed policy version, scope, and
   approval boundaries. A role grants responsibility, not broader permission.
3. Read only the assigned role: [PM](roles/pm.md),
   [team leader](roles/team-leader.md), [worker](roles/worker.md), or
   [reviewer](roles/reviewer.md), or [tester](roles/tester.md).
4. Use the configured, enabled profile the human explicitly selected; name it and
   the full policy SHA in every packet. Files in profiles/ are disabled examples
   with environment-specific model IDs. Check live provider availability, option
   names, authentication, and billing before activation. No silent paid fallback
   or automatic provider/profile switch.
5. Read the host adapter; [T3](adapters/t3.md) is provided as an agent-operated
   procedure. Other hosts need their own launch/status/cancel/isolation adapter.
6. Create a complete packet from [the templates](templates/README.md). Stop and
   report the missing prerequisite if any required field remains unresolved.

When subscription quota blocks a role in an enabled team, follow
[provider continuation](provider-continuation.md) for checkpointing, explicit
target selection, and verified ownership before resuming.

For a single repository, its PM is the coordinator. For multiple repositories,
the human designates a coordination PM/repository and defines contract ownership
in the operating plan. Resolve policy by verified path/remote identity and commit;
do not assume sibling directory names establish trust or ownership.

This module is instructions only: not a daemon, scheduler, lock, budget
controller, or automatic model selector. [The operating plan](operating-plan.md)
records which limits anything actually enforces.
