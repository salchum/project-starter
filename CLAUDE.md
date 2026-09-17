# CLAUDE.md — Project Entry Point

> This file orchestrates how an AI agent reads this project's documentation.
> Read the files below, in order, before starting any work.

## First: check for INIT.md

If `INIT.md` exists in this project, this is an un-bootstrapped template —
follow its instructions before anything else. It deletes itself once the
project is initialized.

## Read Order

1. **STATUS.md** — what's decided, what's still open, what's blocked (read this first)
2. **PRD.md** — what we're building and why (requirements, scope, users)
3. **ARCHITECTURE.md** — how the system is built (stack, components, boundaries)
4. **SCHEMA.md** — the data model (entities, relationships, constraints)
5. **DESIGN.md** — UI/UX flow and design system
6. **RULES.md** — business rules that constrain behavior (non-negotiable logic)

## Rule

Always read PRD.md, ARCHITECTURE.md, SCHEMA.md, DESIGN.md, and RULES.md
before proposing or writing code, unless the user explicitly says to skip
this step. If any file is still full of `[PLACEHOLDER]` tokens, treat that
section as undefined — ask the user or state the assumption you're making
instead of guessing silently.

## Notes for the agent

- These files are the source of truth. If code and docs disagree, flag it —
  don't silently pick one.
- Tech stack is NOT fixed by this template. ARCHITECTURE.md is filled in per
  project; do not assume any particular language or framework from this file.
- SCHEMA.md is intentionally abstract (entities/relationships/constraints),
  not tied to a specific database. Map it to concrete tables/collections in
  ARCHITECTURE.md or migrations.
