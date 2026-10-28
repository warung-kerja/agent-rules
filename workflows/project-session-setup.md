# Choose and set up a project session preset

Updated: 2026-10-29.

All sessions follow the [shared principles](../standards/session-principles.md), [core rules](../standards/core-rules.md), and [model upgrade policy](../standards/model-presets.md).

## Choose one preset

Use the owner's stated project type. If it is unclear, ask which setup fits before creating sessions.

| Project type | Session guide | Team size |
| --- | --- | --- |
| Product development | [Product](product-session-setup.md) | 6 |
| Branding or design | [Design](design-session-setup.md) | 5 |
| Prototype or website | [Prototype / website](website-session-setup.md) | 4 |
| Generic / all purpose | [General](general-session-setup.md) | 2 |

A website does not automatically require the six-role product team. Use the Prototype / Website preset for that work unless the owner chooses Product Development for its ongoing product lifecycle. Do not combine presets automatically. This rules library does not need any preset installed merely because it documents them.

## Shared setup procedure

1. Read the selected guide and its linked canonical role files, then inspect existing project instructions, sessions, tools, and active work. Preserve context and reuse matching sessions.
2. Follow [adoption and updates](adopt-and-update.md). Copy the project-profile and session-register templates into `docs/agent-team/` or the project's equivalent documented location. Keep only the selected preset's roles. Non-code projects can use their project folder rather than a software repository.
3. Record the selected type, adopted rules SHA, model policy, actual host model availability, authorized delegation/messaging routes, tool access, file ownership, outputs, and acceptance criteria. Use Linear where configured; do not fabricate a board or make tool access a completed assumption.
4. When authorized to establish the team, create missing role chats using the common preamble below with the matching canonical role file path. Resolve family models using the model policy, verify their actual bindings, and preserve project-specific pins. Record missing tools/models as blockers.
5. Verify that each role accepted its remit and read the adopted rules. Check harmless routing acknowledgement only within authorized routes. Record the final session bindings and any deferred configuration. Do not run image generation, renders, builds, or deployments merely to prove a chat exists.

The three non-product presets are on demand by default. No Manager polling, Sweeper, Reviewer, or other recurring routine is implied. Substantial or risky work still needs independent review under the shared principles; use an authorized fresh review context without adding permanent roles by default.

## Common preamble for Design, Website, and General roles

Replace placeholders. Resolve `<ROLE_FILE>` to the canonical `roles/*.md` file linked by the selected guide, using the adopted checkout or snapshot. Read the role file directly; do not maintain another role-description copy here:

```text
You are <ROLE> for <PROJECT>, using the <PRESET> session setup.
Read the project instructions, project profile, session register, and adopted
shared session principles, core rules, model policy, selected setup guide, and
<ROLE_FILE> at the recorded adopted revision. Apply the role file’s selected-preset
section and shared sections that name that preset. Report inaccessible sources.
Follow the registered model family and reconcile verified same-family successors
before new assignments, respecting explicit pins and supported settings controls.
Preserve the role, context, active work, and agreed scope when delegating.
Use only authorized team routes and tools; do not create duplicate sessions.
Record durable outputs in the project and task status in Linear where configured.
Report actual model/tool availability and readiness, then await work.
```
