# Adopt and update the shared rules

## First adoption

1. Obtain a readable checkout of `warung-kerja/agent-rules` on the machine running the project. Record its full Git commit SHA.
2. Read README.md, the session principles, core rules, model policy, and the selected setup guide. Use the [project preset selector](project-session-setup.md); ask only if the project type is unclear. The session principles apply to every preset.
3. Inspect the consuming repo's instructions, existing chats, Linear project, automations, and active work. Reuse working setup; identify conflicts before changing it.
4. Copy the project-profile and session-register templates into the project's `docs/agent-team/` or equivalent documented project folder. Select only the chosen preset's roles; product-only routine defaults do not apply to other presets. Fill them with verified local settings. Keep private host paths and chat IDs in an ignored local register if the product repo is public.
5. Incorporate the AGENTS snippet into existing project instructions without overwriting unrelated content. Record the selected rules paths, full adopted SHA, local exceptions, and how agents can read that revision.
6. If agents cannot access the library reliably, vendor the selected files into `docs/agent-team/shared-rules/`. Preserve their source paths and SHA; update them together through adoption PRs. Configure each runtime's recognized instructions entrypoint to read these files.
7. Follow the selected session guide to configure and verify the team. Record what is installed, deferred, or blocked.

A Markdown link does not load instructions automatically. For Codex, use the project's AGENTS.md as the entrypoint and explicitly direct it to the relevant files. Other agents need their own supported entrypoint. See the [official AGENTS.md guidance](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

## Updating the library

Change the canonical files here and add a dated CHANGELOG entry explaining behavior and migration impact. Review and merge the change. Use the merged commit as the revision offered to consuming projects.

A change that alters authority, routing, model defaults, schedules, or completion criteria should describe what adopters must reconfigure. Do not imply existing sessions were updated just because the Markdown changed.

## Updating a consuming project

To adopt the four-preset setup and model upgrades, include `standards/model-presets.md`, the selector, and the selected setup guide in the recorded paths/snapshots. Refresh existing prompts and runtime entrypoints. Record family, actual model, explicit pins, and upgrade status per session. Existing projects may reconcile verified same-family successors under this policy without a full rules migration; record the model-policy source separately. Other standards still follow pinned adoption. No existing chat, routine, or watcher changes merely because these files are added.

When adopting the session principles, add `standards/session-principles.md` to the selected paths and any vendored snapshot. Update the runtime entrypoint and every role's common preamble to read it, including existing sessions. Preserve the 15 principles as one canonical list rather than making separate role-specific copies. Check local model/effort and delegation policies for conflicts; record any constraints or agreed exceptions. No schedule changes are required by this addition.

1. At project onboarding or a deliberate rules-refresh task, fetch the library and compare the adopted commit with the proposed commit. Do not switch to a moving branch silently during an assignment.
2. Summarize relevant differences and conflicts. Preserve local safety constraints and active holds. If a required source is unavailable, use the recorded snapshot and disclose the limitation; do not guess the latest rules.
3. Prepare one adoption PR updating selected snapshots/pointers, the adopted SHA, and any exceptions. Behavior needing new authority remains pending until the owner grants it.
4. Refresh each affected session's instructions through its supported mechanism. Inspect routines before editing them; migrate one existing routine instead of creating duplicates. Record the result.
5. Verify routing and ownership without starting real implementation merely as a test. Manager records the adoption evidence and outstanding blockers in the product repo.

## Across computers

Clone/pull the same GitHub library and resolve the same adopted SHA on each machine. Rebind local checkout paths, project IDs, chat IDs, model routes, tools, and credentials on that machine; never assume they transfer automatically.

Choose one scheduler host for each routine. A laptop and an always-on computer must not both dispatch the same ticket or run the same sweep. Keep shared dispatch evidence in Linear or another explicitly designated durable store; chat history alone is insufficient across machines.

To roll back a rules change, restore the prior adopted SHA and corresponding snapshots, then refresh the affected sessions/routines and record any work already started under the newer policy.
