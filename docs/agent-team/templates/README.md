# Task records

Copy these templates into the owning repository at
docs/agent-team/tasks/<task-id>/. Choose a unique task ID before delegation.
Use brief.md, status.json, result.md, and reviews/<round>.md.

Replace every REQUIRED marker before dispatch. A brief is a complete packet:
include required policy excerpts or verified local paths, since child agents do
not inherit the parent's conversation. Avoid credentials and production data.

Status transitions:
queued → running → in_review → accepted.
Running or review may become blocked, failed, or cancelled. A correction returns
in_review → running with a new attempt/round record. At the configured unsuccessful
correction-round limit, mark blocked and escalate. Never reset counters by renaming a task.

Accepted means task criteria and required reviews passed. Track merge/deployment
separately. The single named status writer reconciles child activity before changing
state and records timestamped reasons; elapsed time alone cannot release a slot.
