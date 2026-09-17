# SCHEMA — Data Model

<!-- Abstract and database-agnostic: entities, relationships, data types, constraints.
     Do NOT name a specific database engine or table syntax here — map to
     concrete tables/collections/migrations in ARCHITECTURE.md or code. -->

## 1. Entities

### [PLACEHOLDER: Entity name, e.g. User]

| Field | Type | Constraints | Notes |
|---|---|---|---|
| id | identifier | required, unique | [PLACEHOLDER] |
| [PLACEHOLDER] | [string/number/boolean/date/enum] | [required/optional/unique/default:...] | [PLACEHOLDER] |

## 2. Relationships

<!-- e.g. "User has many Orders (1:N)" / "Order belongs to one User (N:1)" / "Tag <-> Post (M:N)" -->

- [PLACEHOLDER: Entity A] — [PLACEHOLDER: relationship type, e.g. 1:N] — [PLACEHOLDER: Entity B]

## 3. Constraints & Invariants

<!-- Rules the data must always satisfy, independent of business logic (that goes in RULES.md) -->

- [PLACEHOLDER: e.g. "email must be unique across Users"]

## 4. Lifecycle / State

<!-- If an entity has states (draft/published/archived etc.), describe valid transitions -->

### [PLACEHOLDER: Entity name]
- States: [PLACEHOLDER]
- Valid transitions: [PLACEHOLDER]
