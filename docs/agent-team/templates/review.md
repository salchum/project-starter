# REQUIRED task ID — review round REQUIRED

- Reviewer identity / role / independence: REQUIRED
- Actual provider / model / explicit options / readback source: REQUIRED (or unknown)
- Completion timestamp / report path: REQUIRED
- Exact reviewed SHA / base SHA: REQUIRED
- Original brief and applicable criteria: REQUIRED
- Previous findings, responses, unresolved objections: REQUIRED
- Evidence inspected / checks actually run: REQUIRED
- Checks not run / coverage limitations: REQUIRED (or none)
- Findings: REQUIRED (or explicitly none)
- Verdict: REQUIRED (pass / changes-required / blocked)
- Remaining risk requiring human decision: REQUIRED (or none)
- Next owner / next action / decision requested from PM or user: REQUIRED (or none)

For every finding: stable finding ID, severity, location, triggering condition,
impact, supporting evidence, required correction, action owner and disposition.
Use an explicit unassigned owner when allocation is pending; the PM resolves it.
Recheck corrected findings against
the new SHA. A pass applies only to the stated scope and revision.
