# Agent Rules

Shared guardrails, roles, and repeatable ways of working for agents across projects and computers.

This repository owns reusable standards. Each product repository owns its implementation and project-specific configuration. Linear owns tasks and execution status. Chats coordinate the work; important decisions must survive outside chat history.

## Start here

Every session starts with the [15 shared principles](standards/session-principles.md), regardless of role or project type.

Choose the project type using [Project session setup](workflows/project-session-setup.md):

| Preset | Sessions |
| --- | --- |
| [Product Development](workflows/product-session-setup.md) | Brain, Planner, Builder, Sweeper, Reviewer, Manager |
| [Branding / Design](workflows/design-session-setup.md) | General, Manager, Designer, Generator, 3D Builder |
| [Prototype / Website](workflows/website-session-setup.md) | General, Manager, Designer, Builder |
| [Generic / All Purpose](workflows/general-session-setup.md) | General, Generator |

Ask only when the project type is unclear. The six-session structure applies only to Product Development. This rules library does not need a session team installed by default.

All presets follow the [automatic model upgrade policy](standards/model-presets.md): upgrade Sol, Luna, and Astra sessions to verified available successors within their own families. For example, Sol 6.1 follows Sol 6.2 when released and available. Runtime updates require a supported settings interface; no background release watcher is installed by this documentation.

To use this library, ask your agent:

> Read https://github.com/warung-kerja/agent-rules, its shared principles, and model policy. Select the appropriate project preset, using my stated project type or asking if unclear. Inspect existing sessions and apply the setup within my authorization. Preserve project-specific constraints, reuse working sessions/routines, and record the adopted rules commit and actual model bindings.

## Install or refresh with a skill

The reusable [setup-agent-rules skill](skills/setup-agent-rules/SKILL.md) handles first adoption and refreshes without duplicating the central role definitions. Copy the `skills/setup-agent-rules/` folder into your local Codex skills directory (`$CODEX_HOME/skills`, or `~/.codex/skills` when unset). Keep this repository copy canonical; refresh the installed copy after skill changes. Local installation does not install project rules or update other machines.

Once the skill is available in your session, use:

```text
Use $setup-agent-rules to install the shared rules in this project.
```

For an existing project:

```text
Use $setup-agent-rules to refresh this project's rules to the latest merged revision.
```

You can specify a preset or exact commit in either request. The skill preserves explicit project pins; otherwise a deliberate install/refresh resolves the latest merged revision once and records its full SHA. Chat creation, messaging, and schedules remain subject to the project's authorization.

## Default for software projects

Software projects use [simple, complete implementation](standards/simple-implementation.md): read connected code, reuse existing mechanisms, avoid speculative complexity, finish the entire change, and verify meaningful risks. This applies to product development, websites, prototypes, scripts, and tools across presets. Non-code work has no added development requirements.

The setup skill includes the standard in new software-project adoptions when it exists at the selected rules revision, records its applicability, and adds explicit instruction loading. Existing projects need a deliberate pinned refresh. Older selected revisions are preserved with an availability limitation. The [Ponytail](https://github.com/DietrichGebert/ponytail) plugin and its commands/hooks are optional; setup does not install or enable them.

## Library

| Folder | Purpose | Current contents |
| --- | --- | --- |
| `standards/` | Shared guardrails that apply across workflows | [Session principles](standards/session-principles.md), [core rules](standards/core-rules.md), [simple implementation](standards/simple-implementation.md), [model presets](standards/model-presets.md) |
| `workflows/` | Procedures for setting up and operating projects | [Project preset selection](workflows/project-session-setup.md), setup guides above, [adopting and updating rules](workflows/adopt-and-update.md) |
| `skills/` | Reusable adoption helper | [Set up agent rules](skills/setup-agent-rules/SKILL.md) |
| `roles/` | Canonical session responsibilities, boundaries, outputs, and completion rules | [Brain](roles/brain.md), [Planner](roles/planner.md), [Builder](roles/builder.md), [Sweeper](roles/sweeper.md), [Reviewer](roles/reviewer.md), [Manager](roles/manager.md), [General](roles/general.md), [Designer](roles/designer.md), [Generator](roles/generator.md), [3D Builder](roles/3d-builder.md) |
| `templates/` | Starting points and reusable prompts for consuming projects | [Project profile](templates/project-profile.md), [session register](templates/session-register.md), [AGENTS snippet](templates/agents-snippet.md), [session refresh prompt](templates/session-refresh-prompt.md) |

Maintain each role once in `roles/`. Setup guides select roles, models, routing, and routine defaults; startup prompts direct sessions to read the canonical role file. Shared roles use explicit preset sections so responsibilities do not leak between project types. Name files with lowercase words separated by hyphens.

## How changes reach projects

Edit the shared standard here, update [CHANGELOG.md](CHANGELOG.md), and commit it. Projects adopt a specific commit through a small update PR and record exceptions locally. See [adoption and updates](workflows/adopt-and-update.md).

GitHub makes the library available across computers; it does not automatically refresh other clones, running chats, tools, permissions, or schedules. An agent must fetch and read the adopted rules. Project copies are snapshots with provenance, not competing canonical standards.

To refresh existing sessions after an update, use the [reusable session refresh prompt](templates/session-refresh-prompt.md). Select one reviewed commit for the project and replace the revision placeholder before sending it.

## Contributing

Keep instructions actionable and model-independent where possible. Separate required behavior from suggested defaults. Use generic examples suitable for a public repo; never commit credentials, private workspaces, customer data, machine paths, or chat transcripts. Record project-specific exceptions in that project, not as silent edits to the shared standard.
