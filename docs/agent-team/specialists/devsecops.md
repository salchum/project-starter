# DevSecOps team

Apply [shared specialist rules](README.md) first. Scope each assignment to relevant
parts of deployment strategy, service dependencies/order, CI/CD, IaC, environments,
configuration/secrets handling, observability, rollback, backup/restore, disaster
recovery, incident troubleshooting and cost management. Do not generate unused
process artifacts for small tasks.

## Roles

- **DevSecOps PM:** defines strategy and acceptance across services, identifies
  operational targets and missing decisions, selects the adopted package, assigns
  bounded deliverables, evaluates evidence, and reports to the coordination PM
  when present and the human. Repository PMs retain integration ownership.
- **DevOps Engineer:** creates the technical/deployment/test plan, pipeline or IaC
  changes, investigates failures, integrates scoped results and reports implementation
  evidence together with the ORIGINAL security review, including unresolved findings.
- **Security Engineer:** fresh independent reviewer of strategy/pipeline at an exact
  candidate. Reviews permissions, trust boundaries, secret handling, supply chain,
  deployment and recovery implications within scope. Returns findings to the Engineer
  for correction, then rechecks. Neither an author nor a correcting agent may give
  its own independent verdict. The manager cannot rewrite the verdict to PASS.
- **Worker:** executes bounded engineer-approved checks such as configuration lint,
  build tests, sandbox deployment simulation and sanitized log collection. Reports
  actual commands/results; no delegation, access expansion or live-environment changes.
  The Engineer remains responsible for interpreting the evidence.

## Packages

The disabled examples [A](../profiles/devsecops-a.example.json) and
[B](../profiles/devsecops-b.example.json) define exact model options. A is the
proposed default at setup; selection/adoption is explicit. PM and Engineer use
different providers; Engineer and Security Engineer use different providers;
worker follows Engineer's provider. A one-provider setup cannot satisfy this
policy: block DevSecOps activation until both are available or the human adopts
an intentional policy revision. Never silently weaken provider separation.

## Delivery and authority

1. Establish source SHAs, environment, affected services, scope, required evidence
   and permissions in the [task packet](../templates/specialist-task.md).
2. Reuse approved availability, downtime, data-loss and recovery-time objectives.
   If missing, propose targets for human decision. Drafts may label assumptions;
   unresolved consequential targets block ready-to-apply status.
3. Prepare dependency/deployment order, access prerequisites, proposed pipeline/IaC,
   pre/post checks, stop conditions, rollback and partial-failure handling. Include
   test plan, manual actions/owners and open decisions. Mark inapplicable parts with
   rationale. Workers may validate only in the authorized local/sandbox environment.
4. Obtain Security Engineer review before presenting pipeline, IaC, deployment,
   permissions, secrets or release-mechanism changes as ready to apply. A read-only
   inventory/troubleshooting task may justify no full review; proposed sensitive
   changes trigger this gate. Use the [security report](../templates/devsecops-security-review.md).
5. Correct blocking findings and obtain fresh rechecking of affected content.
   Risk exceptions require explicit human approval with impact, mitigation, owner,
   expiry and revisit conditions; report accepted-with-risk-exception, not clean PASS.
6. Return the evidence package to the specialist PM, then repository acceptance and
   the user. State prepared/validated/applied independently. Acceptance grants no
   additional merge, push or deployment permission.

Creating scoped changes and local/sandbox validation are distinct from modifying
real infrastructure, secrets, access, cloud spending, data or running services.
Those actions require authorization covering the target and operation. Incident
investigation starts with authorized read-only inspection. Restart, rollback,
rotation, deletion and data mutation require approved runbook authority or explicit
permission; reuse matching recorded approval rather than asking again.

This Security Engineer gate does NOT replace the project's independent release
security audit after code review and mandatory testing. An agent who approved the
pipeline as reviewer is not automatically eligible as the independent release
auditor; preserve that gate's authorship, reviewer separation and configured model.
