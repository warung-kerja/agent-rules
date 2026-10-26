# Session model presets and automatic upgrades

Updated: 2026-10-26. Applies to all four project presets.

## Family defaults

| Family | Initial preset | Successor policy |
| --- | --- | --- |
| OpenAI Sol | Sol 6.1 | Latest verified available Sol successor |
| OpenAI Luna | Luna 6 | Latest verified available Luna successor |
| OpenAI Astra | Astra 6 | Latest verified available Astra successor |
| DeepSeek Flash | DeepSeek Flash | Outside this OpenAI upgrade rule; retain the configured route |

Versions in role tables are starting values, not permanent pins. This policy governs their upgrades. Keep role-to-family assignments stable: a new Sol release updates Sol sessions, not Luna or Astra sessions. The session model is distinct from image/video generation models used by tools.

## Standing upgrade rule

When a newer OpenAI model in the same family becomes available, automatically update every matching preset and existing session that follows this policy. For example, if Sol 6.2 is officially released and available on the destination account/host, upgrade Sol 6.1 presets and sessions to Sol 6.2 without asking for repeated confirmation.

This is standing authorization for same-family model maintenance in projects adopting this policy. It does not authorize unrelated work, messages, new sessions, provider changes, new purchases, or changes to project scope. Respect explicit project model pins and record them as exceptions.

## Release verification and rollout

1. Check official OpenAI model/release documentation and the models actually available to the destination account and host. A release announcement alone does not prove local availability. Verify a genuine successor within the same family; do not invent model IDs or choose a candidate by string sorting alone. Preview/experimental variants and ambiguous family replacements require a deliberate decision rather than an automatic switch.
2. Update this library's family defaults, affected role tables, starter prompts, templates, and changelog coherently. Commit, push, and open a reviewable PR. Respect the repository's existing merge authority; this policy does not bypass branch protection or merge approval.
3. Reconcile each adopting project's registered sessions, future-session defaults, and automation model settings. Preserve role, chat identity/history, assignment, tools, and supported effort. Apply changes at the next safe boundary before new work; do not interrupt running work or wake a chat with a dummy assignment merely to set its model.
4. Use a supported settings interface. If a capability only selects a model for one message/run, record that limit; do not call it a persistent session update. If no supported setter is available, record the exact manual action needed and report the blocker. Never edit internal chat databases or guess undocumented configuration.
5. Verify saved configuration on each host. Record old/new model, actual model ID, verification date, source, affected sessions/routines, exceptions, and blockers in the project's register. A repo edit is not proof of runtime rollout. One host may upgrade while another remains blocked by availability.
6. Report a concise upgrade summary only when something changed or needs attention. On compatibility failure, retain or restore the last working model where available and record why; do not silently downgrade or change families.

Keep general standards pinned to the project's adopted rules revision. Same-family model reconciliation is a specific exception: an adopting project may apply a newly verified successor without waiting for a full standards migration. Record the model-policy revision/source separately so this exception cannot silently update unrelated instructions.

## When reconciliation runs

Run the check during project setup, at session startup/resume before new assignments, on a rules refresh, or when a model-release event is received. A bounded scheduled watcher can supply unattended release detection when explicitly installed; use one scheduler owner across laptops, deduplicate releases, and stay quiet on unchanged checks.

**Implementation status:** this repository defines the automatic-upgrade policy. It does not itself contain a running release detector or a session-settings controller. This change installs no watcher and updates no existing project chats. Unattended detection and rollout require supported runtime capabilities and a separately recorded automation binding; until then, reconciliation happens at the checkpoints above.

## Source guidance

Verify actual availability using [official OpenAI model guidance](https://learn.chatgpt.com/docs/models) and the destination runtime's model controls. The initial assignments above are owner-selected presets, not a claim that a future successor is already released.
