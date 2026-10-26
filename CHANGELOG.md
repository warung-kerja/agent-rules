# Changelog

## 2026-10-25 — Check existing credential documentation first

- Require every session to check `02_Business_Operations/docs` in the local Obsidian vault before asking the owner for API keys or tokens.
- Resolve the vault location per laptop, read only relevant service documentation, and request filesystem access when needed.
- Keep secret values out of repository files, tool output, chats, tickets, PRs, and handoffs; stored credentials do not expand task authority.

Existing adopters must refresh their core rules and session instructions. No credential documents were read or copied as part of this documentation change.

## 2026-10-25 — Principles for every session

- Added the owner's 15 principles as `standards/session-principles.md`, applicable to every role and to non-product work.
- Linked the canonical principles from the repository instructions, onboarding, common session prompt, and adoption templates.
- Clarified how cheaper models and bounded subagents support role ownership without silently changing configured models or bypassing runtime constraints.

Existing adopters must include the principles in their pinned rules/snapshots and refresh affected session instructions. This change does not install routines or update other projects automatically.

## 2026-10-25 — Initial library

- Established the shared standards, workflows, and project templates layout.
- Defined six product roles: Brain, Planner, Builder, Sweeper, Reviewer, Manager.
- Added product-development qualification, copy/paste session prompts, bounded handoffs, independent PR review, and proposed sweep/intake schedules.
- Added adoption by Git commit, project overrides, existing-session migration, and single-host scheduling across computers.

First adoption requires filling the project profile, verifying model routes and tools, and configuring authorized sessions/routines. This release installs no product sessions or automation by itself.
