# ARCHITECTURE — System Design

<!-- Tech stack is generic here on purpose — fill it in when the project's stack is chosen. -->

## 1. Stack

- **Language/Runtime:** [PLACEHOLDER]
- **Framework:** [PLACEHOLDER]
- **Database:** [PLACEHOLDER] <!-- see SCHEMA.md for the abstract data model -->
- **Hosting/Deploy:** [PLACEHOLDER]
- **Key libraries/services:** [PLACEHOLDER]

## 2. High-Level Structure

<!-- Diagram or bullet list of major components and how they talk to each other -->

[PLACEHOLDER: e.g. client -> API -> service layer -> database]

## 3. Components

### [PLACEHOLDER: Component name]
- **Responsibility:** [PLACEHOLDER]
- **Depends on:** [PLACEHOLDER]
- **Exposes:** [PLACEHOLDER: API/interface it provides to others]

## 4. Boundaries & Integration Points

<!-- External services, third-party APIs, auth providers -->

- [PLACEHOLDER: external system] — [PLACEHOLDER: what it's used for]

## 5. Environments

| Environment | Purpose | URL/Notes |
|---|---|---|
| local | development | [PLACEHOLDER] |
| staging | [PLACEHOLDER] | [PLACEHOLDER] |
| production | [PLACEHOLDER] | [PLACEHOLDER] |

## 6. Testing Strategy

<!-- Baseline (non-negotiable): critical paths are always tested, so both
     the test plan and the expected result are explicit. Beyond that
     baseline, scope/tooling/coverage are the user's call — ask, don't
     assume. Don't over-specify for a project that doesn't need it. -->

- **Critical paths (mandatory):** [PLACEHOLDER: the flows that must have tests, and what "passing" means for each]
- **Unit tests:** [PLACEHOLDER: scope, tooling]
- **Integration/E2E tests:** [PLACEHOLDER: scope, tooling]
- **Coverage expectations beyond critical paths:** [PLACEHOLDER]
- **CI:** [PLACEHOLDER: decide once codebase exists]

## 7. Deployment Strategy

<!-- Baseline (default, override if the user wants more): manual push-to-deploy
     is fine until there's a concrete reason for a pipeline (real users,
     collaborators, uptime requirements). Ask, don't assume more than that. -->

- **Trigger:** [PLACEHOLDER: default "manual" — override only with a stated reason]
- **Pipeline:** [PLACEHOLDER: build/test/deploy steps, if any]
- **Rollback:** [PLACEHOLDER: how to undo a bad deploy]
- **Secrets/config:** [PLACEHOLDER: how env vars/secrets are managed per environment]

## 8. Key Architectural Decisions

<!-- Decisions that would be expensive to reverse. Include the "why", not just the "what". -->

- **[PLACEHOLDER: decision]** — [PLACEHOLDER: reasoning, alternatives considered]
