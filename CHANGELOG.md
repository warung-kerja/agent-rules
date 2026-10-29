# Changelog

## 2026-10-29 — Reusable session refresh prompt

- Added `templates/session-refresh-prompt.md` with a target-revision placeholder for future role updates, linked from the README and adoption workflow.
- Distinguishes proposed from adopted revisions, coordinates shared configuration through one owner, and records session acknowledgement without implying automatic reload or wider authority.

Replace the revision placeholder before reuse. Saving this prompt does not refresh existing sessions or change project adoption records.

## 2026-10-29 — Centralized session roles

- Added one canonical file for each of the ten roles in `roles/`, with purpose, responsibilities, boundaries, outputs, and completion rules. Shared roles preserve explicit preset differences.
- Replaced duplicated descriptions and role prompt blocks across all four setup guides with canonical role references. Setup guides retain model assignments, routing, and routine configuration.
- Made Brain’s bounded investigation delegation and assigned architectural PR assessment explicit; Reviewer retains routine independent review and formal verdicts.
- Updated startup prompts, adoption guidance, and templates to load and record role files at the adopted rules revision.

Adopters must include selected role files in pinned checkouts/snapshots and refresh session entrypoints and instructions at a safe boundary. This change does not update existing chats, install routines, or expand authority.

## 2026-10-26 — Four project presets and model upgrades

- Added Branding / Design (five roles), Prototype / Website (four), and Generic / All Purpose (two), preserving the owner's preferred starting models and responsibilities.
- Added shared setup selection, per-role starter prompts, and profile/register templates that support all four presets.
- Added standing same-family OpenAI model upgrades: for example, verified available Sol 6.2 replaces Sol 6.1 across adopting presets, sessions, and routine settings. Preserve pins and report unsupported or blocked runtime updates.
- Updated earlier fixed-model wording to follow the upgrade policy. DeepSeek and generation-provider models remain outside this OpenAI session-family rule.

Adopters must refresh their selected guide, model policy, prompts, and register. This documentation installs no project sessions or background release watcher and does not change existing runtime model settings.

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
