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
   components, integration points, and environments. Recommend sensible
   defaults based on what was said in PRD.md (e.g. a mobile app implies a
   different stack than an internal dashboard).

   Then cover testing and deployment as their own short round, always —
   don't skip it for small projects, but don't over-fill it either:
   - **Testing:** critical-path tests are mandatory — ask the user which
     flows count as critical and what "passing" means for each, so the
     test plan and expected result are explicit. Ask their preference for
     anything beyond that baseline (unit/integration/E2E scope, coverage);
     don't assume more than critical-path coverage without asking.
   - **Deployment:** default is manual push-to-deploy — ask if they want
     more than that, and only add pipeline/automation detail if they give
     a concrete reason (real users, collaborators, uptime needs).
   - **CI:** do not ask about this. Leave the CI field as
     `[PLACEHOLDER: decide once codebase exists]` — it's an explicit
     later decision, not part of bootstrap.
   - **User-facing docs:** ask where they'll live (README section, a docs
     site, an OpenAPI spec, none) — don't prescribe a format, just record
     the answer in STATUS.md's "Decided" section. Skip creating any new
     doc file for this; formats vary too much by project type to template.

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

6. **ROADMAP.md** — Ask directly whether this project ships in phases or
   all at once. If all at once, delete ROADMAP.md and skip the rest of
   this step. If phased, auto-suggest phase boundaries from PRD.md's
   feature priorities (P0 -> Phase 1, P1 -> Phase 2, ...), then have the
   user confirm/adjust the phases and supply a day-range effort estimate
   for each (e.g. "10-20 days") — don't invent estimates yourself.

7. **STATUS.md** — Last step. Summarize what was just decided into the
   "Decided" section. Leave "Open/TODO" and "Blocked" empty unless
   something concrete came up during the interview.

## When done

- Confirm with the user that every file looks right.
- Delete this file (`INIT.md`).
- Write HANDOVER.md as the closing action, same as any other session
  (see AGENTS.md's Rule section) — summarize what was just bootstrapped
  and set "Next step" to the actual next move (e.g. "start building the
  first feature").
- Do not proceed to writing code in the same turn — bootstrapping the docs
  is the task; implementation is a separate, later request.
