# Product session setup

Status: initial standard · Updated: 2026-10-29 · Scope: product-development projects only.

Use this guide for a fresh product or to bring an existing project into the shared way of working. A session means a persistent project chat with a defined role. It is separate from a temporary subagent and has no automatic background execution merely because it exists.

Every role follows the [15 shared session principles](../standards/session-principles.md). They also apply when the project does not qualify for this team structure.

## 1. Qualify the project

First ask the owner: **“Is this a product-development project?”** An explicit answer already given in the current setup request counts; do not ask twice.

For this workflow, product development means building or maintaining a software product, application, or product website with ongoing implementation work. A research task, branding project, documentation library, or one-off administrative job does not automatically qualify.

- **Yes:** establish the six roles below.
- **No:** skip this structure and select the [Design, Website, or General preset](project-session-setup.md).
- **Unclear:** clarify before creating sessions or routines.

Writing or reading this guide does not itself authorize creating chats, messaging them, or enabling schedules. Apply it when the owner asks to set up the team. Confirm missing project settings; reuse authorization already given.

## 2. The six roles

Use the cheapest capable model and appropriate effort for the task, following the shared principles. Routine mechanical work can use Luna 6 where available and authorized, while the role retains accountability.

Model choices below are initial family assignments governed by the [automatic model upgrade policy](../standards/model-presets.md). Upgrade to verified available successors in the same family without repeated confirmation, preserving role responsibilities. Verify actual model identifiers on the destination host. If a successor is unavailable, keep the working model and record the blocker; a different family requires an agreed substitution.

| Session | Preferred model | Canonical role | Default activation |
| --- | --- | --- | --- |
| 🧠 Brain | Astra 6 | [Brain](../roles/brain.md) | On demand |
| 💡 Planner | Sol 6.1 | [Planner](../roles/planner.md) | On request or routed planning work |
| 🛠️ Builder | Sol 6.1 | [Builder](../roles/builder.md) | One authorized assignment at a time |
| 🧹 Sweeper | DeepSeek Flash | [Sweeper](../roles/sweeper.md) | Twice weekly |
| 😎 Reviewer | Sol 6.1 | [Reviewer](../roles/reviewer.md) | When a PR is ready or its head changes |
| 👁️ Manager | Luna 6 | [Manager](../roles/manager.md) | On handoff; scheduled intake recovery |

Read the linked role file as the session's full role instructions. Role files are canonical; do not maintain separate role prompt copies in this guide.

### Suggested routine configuration

- Sweeper: **Wednesday and Sunday at 04:30, Australia/Sydney**. This is a portable default derived from the Factory pattern, using Sydney wall-clock time including daylight saving. Verify scheduler behavior and host availability; record the actual schedule. A written schedule is not an installed routine.
- Manager intake recovery: **daily at 08:00 Australia/Sydney**, plus immediate authorized handoffs. Adjust to the product's needs. Use one scheduler host; remain quiet on unchanged checks.
- Brain, Planner, Builder, and Reviewer are on demand by default.

## 3. Routing and handoffs

Normal feature flow:

`Owner → Planner → Manager/Linear → Builder → Reviewer → Manager/Linear → authorized merge/release executor`

Use `Planner → Brain → Planner` only when strategic help is needed. Sweep flow is `Sweeper → Manager/Linear → Planner if unclear, otherwise Builder → Reviewer`.

Manager is the coordination hub. Direct Builder ↔ Reviewer repair loops are useful when explicitly authorized; Manager still receives status evidence. Do not require routine work to visit all six roles.

Use this handoff shape, omitting fields that genuinely do not apply:

```text
Assignment ID / Linear issue:
From role → destination role:
Requested outcome and authorized scope:
Relevant context and decision links:
Acceptance criteria and dependencies:
Branch / worktree / PR / exact head SHA:
Evidence, checks, and limitations:
Existing holds and actions requiring separate authority:
Next action / completion reply destination:
```

A handoff is complete when the receiving role accepts it or the sender records a delivery blocker. A quiet chat is not proof of acceptance. Use one completion or blocker report per assignment and avoid repeated acknowledgements.

Suggested Linear state mapping: Backlog → Ready → In Progress → In Review → Done, with Blocked represented by the project's supported state or label. Map to existing team states rather than creating unnecessary ones. Record the project's Done definition; merged and deployed may be different milestones.

## 4. Set up a new or existing project

1. **Qualify.** Apply the product-development gate above.
2. **Inspect.** Read repo instructions and project docs; identify existing role chats, Linear configuration, routines, active assignments, holds, and model/tool availability.
3. **Record configuration.** Follow [adoption and updates](adopt-and-update.md). Fill [project profile](../templates/project-profile.md) and [session register](../templates/session-register.md). Record the adopted rules SHA, local overrides, dispatch eligibility, messaging routes (including completion replies), and merge/release authority.
4. **Reuse roles.** Map existing chats to these responsibilities. An existing Tickets chat may already cover Manager's triage function; a Brainstorm chat may serve Planner or Brain depending on its actual remit. Keep names if useful. Do not create duplicate chats or cancel existing routines without authorization. Preserve in-progress work and holds.
5. **Create missing sessions when authorized.** Use the six preferred titles/models, the preamble below, and the matching canonical role file. Bind them to the correct product and checkout. Record actual IDs/host/model routes in local configuration. Roles that do not edit code can use the product checkout read-only by convention; code-writing work needs ownership isolation.
6. **Authorize routes once.** Confirm the owner's team messaging/dispatch scope if it is not already given. Configure only those routes. If tools cannot message other chats, use a written handoff for the owner; do not claim routing is operational.
7. **Configure routines when authorized.** Inspect existing routines, choose one scheduler host per routine, and install/update the Sweeper and Manager schedules. Include project filters, deduplication, scope, pause/hold rules, and quiet-on-no-change behavior. Keep Brain, Planner, Builder, and Reviewer on demand unless a separate need is agreed.
8. **Verify.** Confirm each session read the adopted revision and accepted its role; check actual model and tool access. Validate a handoff with a harmless setup acknowledgement, not a real build. Inspect saved routine targets, timezone, and enabled status. Verify Manager can read the correct Linear project. Record blockers honestly.
9. **Finish with a setup report.** List reused/created sessions, models, adopted SHA, Linear mapping, allowed routes, installed routines, exceptions, and anything not operational. Do not call setup complete while required bindings remain TBD.

For an existing project, do not retroactively reroute live assignments just to match the new diagram. Finish or explicitly hand off that work, then adopt the standard for subsequent assignments. Factory-specific production rules must remain local to Factory.

## 5. Session startup prompt

Replace placeholders using the completed project profile. Supply this preamble as the new session's initial prompt and resolve `<ROLE_FILE>` to the matching linked `roles/*.md` file at the adopted revision. The role file itself supplies the role instructions; do not keep a rewritten copy in the session guide.

### Common preamble — include in every role

```text
You are <ROLE> for <PROJECT>, a product-development project.
Read the repository instructions, docs/agent-team/project-profile.md, the verified
session register, standards/session-principles.md, and the adopted shared core
rules, model upgrade policy, product-session guide, and <ROLE_FILE>.
Apply all 15 principles and the role file’s Product development section.
Reconcile verified same-family successors before new assignments, preserving
explicit pins and using supported settings controls; report blocked upgrades.
Use exactly the rules revision recorded in the profile; report inaccessible files.
Follow project-specific constraints, active holds, and current owner authorization.
Use the registered team destinations. Cross-chat messaging and Linear writes are
allowed only within the owner's recorded authorization. Do not create duplicate
sessions, routines, assignments, or a competing backlog.
Keep durable decisions and evidence in the project repo; Linear owns task status.
Report role readiness, actual model, tool/routing limitations, then await work.
```

## 6. Basis and deliberate choices

This guide draws on the Gambar Factory project's existing Planner, Builder, Sweeper, Reviewer, and Manager chats and its [repository instructions](https://github.com/warung-kerja/gambar-factory/blob/main/AGENTS.md), inspected on 2026-10-25. The preferred six-role roster and model assignments come from the owner's request for this library.

Factory has additional specialist chats and task-specific authorizations. Its observed Sweeper can perform implementation under its own instructions; **this standard routes implementation to Builder**, matching the owner's requested main-builder role. Existing Factory behavior is reference evidence, not an automatic migration or authority grant.

The scheduled times, finding limit, one-Builder concurrency, and Manager ownership of routine board writes are initial defaults. Projects may override them explicitly in their profile. This document does not change Factory, create sessions, or activate routines.
