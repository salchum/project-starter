# INIT — One-Time Project Bootstrap

> This file exists to turn this template into a real project. Run it once,
> then delete it. If a human tells you they're starting fresh, or this file
> is still present, follow this before anything else.

## What to do

Interview the user to fill in every `[PLACEHOLDER]` token across the
project files, in this order (each step depends on decisions from the one
before it, so don't skip ahead):

1. **PRD.md** — Ask about the product: name, one-line summary, problem
   statement, goals, non-goals, users/personas, features (with priority),
   success metrics, constraints. Don't ask everything in one giant question
   — group related fields and go a few at a time, like a grilling session:
   propose a sensible default/recommendation for each, let the user
   confirm or override.

2. **ARCHITECTURE.md** — Now that the product is known, ask about stack
   (language, framework, database, hosting), high-level structure, key
   components, integration points, environments. Recommend sensible
   defaults based on what was said in PRD.md (e.g. a mobile app implies a
   different stack than an internal dashboard).

3. **SCHEMA.md** — Derive entities and relationships from the features
   described in PRD.md. Propose a first draft yourself, then confirm with
   the user rather than asking them to invent it from scratch.

4. **DESIGN.md** — Ask about design principles, key user flows and screens
   (derived from PRD features), and design system basics (color,
   typography, spacing) if relevant to this project type. Skip this
   section's design-system tables entirely if the project has no UI
   (e.g. a CLI tool or backend service) — ask first.

5. **RULES.md** — Ask about business rules and permissions/roles implied
   by the features already discussed.

6. **STATUS.md** — Last step. Summarize what was just decided into the
   "Decided" section. Leave "Open/TODO" and "Blocked" empty unless
   something concrete came up during the interview.

## When done

- Confirm with the user that every file looks right.
- Delete this file (`INIT.md`).
- Do not proceed to writing code in the same turn — bootstrapping the docs
  is the task; implementation is a separate, later request.
