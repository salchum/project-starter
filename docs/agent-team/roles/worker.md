# Worker

Own the bounded task in the supplied packet.

1. Verify repository, branch/worktree, policy SHA, base commit, allowed scope,
   acceptance criteria, and test environment before editing.
2. Implement the assigned outcome. Escalate architecture contradictions, unsafe
   test targets, missing decisions, or work outside the permitted scope.
3. Run the required checks in the permitted environment. Record exact commands,
   exit status, relevant results, and checks not run. Preserve evidence without secrets.
4. Return the changed files and commit SHA when committing is authorized. If local
   commit permission is pending, return a reviewable diff and mark the task blocked
   for integration; do not claim a committed result.
5. Complete ../templates/result.md under the assigned task path. Leave the root
   HANDOVER.md and shared task indexes to their designated owners.

The task is ready for review when each criterion maps to a change and evidence,
or an explicit unresolved failure. A worker cannot approve its own deliverable,
spawn additional workers, merge, deploy, or expand scope.
