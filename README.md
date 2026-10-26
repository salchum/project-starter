# Project Starter

A personal GitHub template repo for bootstrapping new projects with a
consistent set of docs an AI coding agent (and you) can rely on.

## Use it

Click **"Use this template"** on GitHub to create a new repo from this one.
Then open the project in Claude Code (or your agent of choice) and say
something like "let's start" — `INIT.md` walks the agent through an
interview to fill in every file for your specific project, then deletes
itself.

## What's inside

| File | Purpose |
|---|---|
| `AGENTS.md` | Canonical entry point — tells the agent what order to read everything in |
| `CLAUDE.md` | Pointer to AGENTS.md, for tools that only look for CLAUDE.md |
| `INIT.md` | One-time bootstrap interview (deleted after first use) |
| `HANDOVER.md` | Session continuity; the PM owns it during team workflows |
| `STATUS.md` | What's decided, what's open, what's blocked |
| `PRD.md` | Product requirements |
| `ARCHITECTURE.md` | Tech stack and system design |
| `SCHEMA.md` | Abstract data model (entities/relationships/constraints) |
| `DESIGN.md` | UI/UX flow and design system |
| `RULES.md` | Business rules |
| `ROADMAP.md` | Phase sequencing with effort estimates (optional — only if the project ships in phases) |

Tech stack is intentionally unspecified until a project picks one —
this template isn't tied to any language or framework.

## Optional agent teams

For projects that need coordinated agents, [docs/agent-team/README.md](docs/agent-team/README.md)
provides provider-neutral PM, team-leader, worker, and reviewer roles; task and
review templates; disabled example profiles; and a T3 adapter procedure.

The module is opt-in. Complete normal project bootstrap, then configure its
operating plan and select a supported profile before delegating. Example model
IDs must be checked against the actual host catalog. These files neither launch
agents nor enforce concurrency or spending limits by themselves.

Use a supervised pilot first. Import the module into existing projects through
targeted instruction changes, preserving their project and deployment rules.
Changes to this template do not automatically update existing repositories.
