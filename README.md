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

## Library

| Folder | Purpose | Current contents |
| --- | --- | --- |
| `standards/` | Shared guardrails that apply across workflows | [Session principles](standards/session-principles.md), [core rules](standards/core-rules.md), [model presets](standards/model-presets.md) |
| `workflows/` | Procedures for setting up and operating projects | [Project preset selection](workflows/project-session-setup.md), setup guides above, [adopting and updating rules](workflows/adopt-and-update.md) |
| `templates/` | Starting points copied into a consuming project | [Project profile](templates/project-profile.md), [session register](templates/session-register.md), [AGENTS snippet](templates/agents-snippet.md) |

Keep role definitions and starter prompts together in the session guide for now. Add new folders only when real content needs them. Name files with lowercase words separated by hyphens.

## How changes reach projects

Edit the shared standard here, update [CHANGELOG.md](CHANGELOG.md), and commit it. Projects adopt a specific commit through a small update PR and record exceptions locally. See [adoption and updates](workflows/adopt-and-update.md).

GitHub makes the library available across computers; it does not automatically refresh other clones, running chats, tools, permissions, or schedules. An agent must fetch and read the adopted rules. Project copies are snapshots with provenance, not competing canonical standards.

## Contributing

Keep instructions actionable and model-independent where possible. Separate required behavior from suggested defaults. Use generic examples suitable for a public repo; never commit credentials, private workspaces, customer data, machine paths, or chat transcripts. Record project-specific exceptions in that project, not as silent edits to the shared standard.
