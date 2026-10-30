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
| `HANDOVER.md` | Where the last session left off — overwritten every session |
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
provides opt-in, provider-neutral PM, team-leader, worker, reviewer and tester roles;
task and review templates; disabled example profiles; and a T3 adapter
procedure. The files are instructions: they launch nothing and enforce no limits
by themselves. Start with that README.
During initialization, choose no team, one provider for all roles, or multiple
providers with models/options selected per role. Reviewers save traceable results
so the PM can return a linked summary of findings, owners and user decisions.
