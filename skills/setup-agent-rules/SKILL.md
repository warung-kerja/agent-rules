---
name: setup-agent-rules
description: Install or refresh the Warung agent-rules library in a project, including its preset, central role files, project profile, session register, and instruction entrypoint. Use when the user asks to adopt these shared rules or update an existing adoption.
---

# Set up agent rules

Use `https://github.com/warung-kerja/agent-rules` as the canonical rules source. This skill orchestrates adoption; role descriptions, model choices, and setup policy remain in that library. Do not copy those definitions into this skill or assume this installed skill's directory contains the library.

## Identify the project and mode

- Use the requested project directory, otherwise the current workspace. Read its applicable instructions and inspect Git status, existing adoption records, role bindings, and active holds before editing. If the target is ambiguous, clarify it before mutation.
- Use **install** when no adoption exists; use **refresh** when the project already has shared rules. Reuse its existing layout and configuration. An incomplete adoption is a repair, not a reason to create a second setup.
- Preserve the existing preset unless the user requests a change. For a new project use the user's stated type; consult `workflows/project-session-setup.md` and ask only if the type is unclear. A website or documentation library does not automatically need the product team.
- Installing project files is authorized by a setup request. Creating chats, sending cross-chat messages, configuring schedules, changing production, or merging an adoption PR requires the corresponding user authorization. Complete the file setup even if runtime configuration is unavailable; report those statuses separately.

## Obtain and select a revision

Prefer a verified local checkout of the canonical repository, otherwise obtain a separate checkout or exact-revision files through available Git/GitHub tools. Verify the remote identity. Do not reset, stash, overwrite, or switch an existing dirty checkout to read a revision; read committed content using Git or an isolated checkout. Do not use uncommitted library changes as a published standard.

Use an explicit requested revision or the project's already-selected adoption target. If neither is given, an explicit install/refresh request selects the latest merged `origin/main` commit after fetching the canonical remote. Resolve it once to a full SHA, report that choice, inspect the changes, and pin all reads and snapshots to that SHA. This deliberate refresh is not permission to track a moving branch during subsequent assignments. Preserve an explicit project pin unless changing it is authorized.

If the source is unavailable, keep the last verified adopted snapshot; report the blocker rather than claiming it is current. For a new installation with no verified source, stop dependent setup without inventing rules. Follow the library's credential lookup rule before asking for credentials; the public source normally needs no new secret.

At the selected revision read:

- `README.md`
- `standards/session-principles.md`, `standards/core-rules.md`, and `standards/model-presets.md`
- `workflows/project-session-setup.md` and `workflows/adopt-and-update.md`
- The selected preset guide and the canonical `roles/*.md` files it links
- `templates/project-profile.md`, `templates/session-register.md`, and `templates/agents-snippet.md`
- For refresh, relevant `CHANGELOG.md` entries and `templates/session-refresh-prompt.md`

These are paths relative to the verified rules source, not this skill folder. Follow the selected revision's workflow and the project's instructions; identify conflicts rather than silently discarding local exceptions. Model-policy reconciliation remains distinct from rules adoption and must use verified availability and supported controls.

## Install project files

Use the project's established adoption layout. For a new setup, default to `docs/agent-team/` (or an equivalent documented folder for non-code projects):

1. Fill the project profile from verified facts: preset, full source SHA, adopted paths, access method, local exceptions, acceptance definition, and authority. Leave genuinely unknown runtime bindings explicitly unresolved; do not invent them or block useful file setup on optional integrations.
2. Create the session register with only the selected preset's roles. Mark sessions, tools, and routines unconfigured unless verified. Keep private host paths, identifiers, and credentials outside public committed material.
3. Default to a portable snapshot in `docs/agent-team/shared-rules/` unless the project already has reliable pinned-checkout access. Copy the selected standards, workflows, role files, and supporting documents needed by their relative links from the exact SHA, preserving the source directory structure. Include link dependencies without enabling their presets. Record source URL, full SHA, and copied paths; snapshots are derived copies, not a second place to edit role definitions.
4. Merge a concise shared-rules section into the applicable `AGENTS.md` or supported runtime entrypoint, using the template. Preserve unrelated instructions. Explicitly direct agents to the project profile, register, shared principles, and canonical role file for their assigned role/preset. A Markdown link alone is not an instruction loader. Do not invent a role for an unassigned session.
5. Follow the project's adoption/review process. Prepare an adoption PR where required and supported. Keep a proposed revision distinct from an active adopted revision until that process completes. Do not require another permission question for already-authorized local file edits.

## Refresh without duplicating setup

Compare the old and proposed revisions and summarize meaningful changes, conflicts, and newly required authority. Use one designated writer for shared adoption files; provide a handoff if another session owns them, through existing authorized routes only.

Update existing snapshots, pointers, profile, and entrypoint together. Compare locally modified snapshot files against the old source before replacing them; preserve intentional exceptions in the profile or report conflicts. Remove obsolete snapshot files only when recorded as managed and no longer needed; never delete unrelated project files. Repeating the same refresh should leave correct files unchanged.

After adoption, refresh this session at a safe assignment boundary. For other sessions, use `templates/session-refresh-prompt.md` with the resolved revision, via supported and authorized mechanisms. If cross-chat messaging is not authorized or available, give the owner a ready-to-send prompt. Record acknowledgement per session; do not mark other sessions refreshed merely because shared files changed. Retain active assignments, holds, identities, and model pins.

## Verify and report

Check the actual resulting files: resolved source SHA, snapshot content against that revision, required local links, preset/role coverage, preserved project exceptions, meaningful unresolved placeholders, and Git diff whitespace where applicable. Distinguish intentional unknown bindings from unfinished install instructions. Documentation installation does not require application tests or a trial build, render, generation job, or deployment.

Report the project, preset, revision, files changed, validation evidence, and separate statuses for project-file adoption and runtime/session refresh. List only actionable blockers or pending adoption steps. Do not claim an automatic update service, schedule, permission grant, or runtime change was installed without verifying it.
