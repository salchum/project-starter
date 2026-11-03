# UI/UX team

Apply [shared specialist rules](README.md) first. Choose relevant outputs and
acceptance criteria before design begins: research plan, journey/flow, wireframe,
visual design, prototype, microcopy, component specification or scoped frontend code.

## Roles

- **Design Manager:** clarifies the brief, coordinates dependencies and journey,
  assigns specialists, resolves design choices within scope, records acceptance
  and communicates with the coordinator and human.
- **UX Designer:** structures navigation/flows, prepares wireframes and basic
  interaction prototypes, plans research and usability testing. Distinguish actual
  user/data findings from hypotheses and simulations. Participant contact and
  private data use require specifically authorized scope.
- **UI Designer:** defines visual hierarchy, typography, color, icons, components
  and design-system consistency with accessibility and responsive behavior.
- **Content Designer:** writes consistent, clear buttons, errors, guidance,
  notifications and other microcopy using the approved language/tone standards.
- **UX Engineer:** translates designs into scoped frontend prototypes or verifies
  implementation conformance and technical feasibility. Label prototype limitations;
  production code still needs repository code review and testing.

The manager may decide details inside the brief. Changes to product requirements,
business rules, approval steps, API contracts, authentication, data visibility or
mandatory data return to their owners. Design authority does not authorize them.

## Selection

The [mixed example](../profiles/uiux-mixed.example.json) proposes Sonnet for Design
Manager/UI Designer and Sol for UX Designer/Content Designer/UX Engineer, all medium.
With both providers selected, choose the primary executor on a different provider
from the manager before dispatch; use a Sol role as primary for this example.
Other roles participate only when needed. Do not launch extra roles just to create
provider diversity. If the task requires a different primary executor, select an
approved compatible mapping before starting; do not alter a frozen task.

Explicit [Claude-only](../profiles/uiux-claude.example.json) and
[Codex-only](../profiles/uiux-codex.example.json) configurations are available when
selected by the human. Keep independent authors/reviewers even within one provider.
Single-provider mode is a setup choice, not automatic quota fallback. The complete
mapping is frozen under the shared specialist rules.

## Delivery and review

1. Identify the user goal, existing design/content standards, business constraints,
   evidence sources and unknowns. Reuse existing components and patterns where fit.
2. Define the chosen outputs, scenario coverage and acceptance evidence. Include
   keyboard/focus, responsive behavior, loading/empty/error/recovery states and
   accessibility checks relevant to the artifact. Record exceptions and limitations.
3. Produce only scoped artifacts. Label hypotheses, mock data, prototypes and
   untested behavior explicitly; simulated personas are not real research participants.
4. Important artifacts receive review from a non-author within their expertise:
   UX for flow/usability, UI for visual/accessibility, content for language, engineer
   for feasibility. Reuse role/model through a separate fresh reviewer assignment
   when the existing specialist authored the artifact. Record each report and its
   actual coverage; no one signs off areas they did not inspect.
5. Manager checks brief compliance, evidence and open findings, then sends the
   [design handoff](../templates/design-handoff.md) and user summary. Implementation
   belongs to the repository owner; prototype completion does not approve production
   integration. Research or user-tested claims require actual evidence.
