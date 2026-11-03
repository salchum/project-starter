# REQUIRED DevSecOps security review — round REQUIRED

Apply [review recording](README.md#review-recording) and the
[DevSecOps gate](../specialists/devsecops.md#delivery-and-authority).

- Task / reviewer identity and model-options / non-author declaration: REQUIRED
- Policy SHA / candidate full SHA / target environment and reviewed files: REQUIRED
- Scope: strategy, pipeline/IaC, permissions, secrets, supply chain, rollback: REQUIRED (justify exclusions)
- Evidence inspected / checks actually run / checks not run and limitations: REQUIRED
- Findings: ID, severity, evidence/location, impact, required correction, owner, disposition: REQUIRED or none
- Previous finding IDs and recheck evidence: REQUIRED or initial round
- Verdict: PASS / changes-required / blocked / accepted-with-risk-exception: REQUIRED
- Exception authority / impact / mitigation / owner / expiry / revisit conditions: REQUIRED or none
- Remaining gates, including separate release audit and deployment authorization: REQUIRED
- Report persistence owner / timestamp / next action: REQUIRED

An interrupted attempt is incomplete, never PASS. Return the original report
unchanged through the Engineer to the manager. Findings cannot be erased by a new task.
