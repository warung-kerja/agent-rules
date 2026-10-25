# Agent Rules

Shared guardrails, roles, and repeatable ways of working for agents across projects and computers.

This repository owns reusable standards. Each product repository owns its implementation and project-specific configuration. Linear owns tasks and execution status. Chats coordinate the work; important decisions must survive outside chat history.

## Start here

Ask: **Is this a product-development project?**

- **Yes:** follow [Product session setup](workflows/product-session-setup.md) to establish the six-session team.
- **No:** skip that team structure. Adopt only the standards relevant to the work. This rules library itself does not need six product sessions.
- **Unclear:** ask the owner before creating sessions or routines.

To use this library, ask your agent:

> Read https://github.com/warung-kerja/agent-rules and its product-session setup guide. Determine whether this is product development. If it is, inspect the existing project and sessions, propose or apply the setup within my authorization, and preserve project-specific constraints. Record the adopted rules commit. Reuse existing sessions and routines where possible.

## Library

| Folder | Purpose | Current contents |
| --- | --- | --- |
| `standards/` | Shared guardrails that apply across workflows | [Core rules](standards/core-rules.md) |
| `workflows/` | Procedures for setting up and operating projects | [Product session setup](workflows/product-session-setup.md), [adopting and updating rules](workflows/adopt-and-update.md) |
| `templates/` | Starting points copied into a consuming project | [Project profile](templates/project-profile.md), [session register](templates/session-register.md), [AGENTS snippet](templates/agents-snippet.md) |

Keep role definitions and starter prompts together in the session guide for now. Add new folders only when real content needs them. Name files with lowercase words separated by hyphens.

## How changes reach projects

Edit the shared standard here, update [CHANGELOG.md](CHANGELOG.md), and commit it. Projects adopt a specific commit through a small update PR and record exceptions locally. See [adoption and updates](workflows/adopt-and-update.md).

GitHub makes the library available across computers; it does not automatically refresh other clones, running chats, tools, permissions, or schedules. An agent must fetch and read the adopted rules. Project copies are snapshots with provenance, not competing canonical standards.

## Contributing

Keep instructions actionable and model-independent where possible. Separate required behavior from suggested defaults. Use generic examples suitable for a public repo; never commit credentials, private workspaces, customer data, machine paths, or chat transcripts. Record project-specific exceptions in that project, not as silent edits to the shared standard.
