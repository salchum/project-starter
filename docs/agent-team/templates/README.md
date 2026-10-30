# Task records

Copy these templates into the owning repository at
docs/agent-team/tasks/<task-id>/. Choose a unique task ID before delegation.
Use brief.md, status.json, result.md, and reviews/<round>.md.

Replace every REQUIRED marker before dispatch. A brief is a complete packet:
include required policy excerpts or verified local paths, since child agents do
not inherit the parent's conversation. Avoid credentials and production data.

## Review recording

Every code reviewer, reviewing team leader, PM performing acceptance review, and
security auditor (when configured) records each round, including PASS with no
findings, changes-required, and blocked outcomes. Use [review.md](review.md) for
code/leader/PM review and the configured audit template for security audit.
Testers follow the same persistence and reporting rules using
[test-result.md](test-result.md) against the leader-approved
[test-plan.md](test-plan.md); the PM includes their evidence and defects.
Allocate a distinct path per role, reviewer and round under the task directory;
retain previous rounds and link carried-forward finding IDs.

The brief names the report path and persistence owner before dispatch. A reviewer
permitted to write records saves only its scoped report. A read-only reviewer
returns the complete record for the designated integration/status owner to
persist without changing its verdict, identity or evidence. Neither route
requires unauthorized commits or changes to the implementation checkout.
The owner verifies that the file exists and matches the returned report, then
passes its path and reviewed SHA to the PM. Chat-only PASS is not a durable record.

If a reviewer is interrupted before reporting, the manager records an incomplete
attempt with the known evidence and next owner; it is not an auditor/reviewer
verdict. Missing reports, stale SHAs or unresolved required reviews block task
acceptance and readiness. Apply the existing closure rules before settlement.

The PM verifies all required report paths, candidate SHAs, coverage and finding
dispositions, records its own scoped acceptance review, then saves and presents
[pm-summary.md](pm-summary.md) as a task-specific summary for the user. Include
open findings, owners, recommended actions and decisions requiring the user.
Link duplicate findings to all source records; retain conflicting verdicts until
resolved. Only the designated owners update shared indexes and handovers.

## Status transitions
queued → running → in_review → accepted.
Running or review may become blocked, failed, or cancelled. A correction returns
in_review → running with a new attempt/round record. At the configured unsuccessful
correction-round limit, mark blocked and escalate. Never reset counters by renaming a task.

Accepted means task criteria and required reviews passed. Track merge/deployment
separately. The single named status writer reconciles child activity before changing
state and records timestamped reasons; elapsed time alone cannot release a slot.
