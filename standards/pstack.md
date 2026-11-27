# Optional PStack playbooks

PStack is Lauren Tan's collection of engineering playbooks and skills. It is an optional tool for authorized software work in any project preset. Follow the project's adopted [simple implementation standard](simple-implementation.md), [core rules](core-rules.md), and role responsibilities while using it. [Original PStack](https://github.com/cursor/plugins/tree/main/pstack) · [Codex port](https://github.com/Aqua-123/pstack-for-codex)

## When to use it

- Use a playbook when a task benefits from explicit steps and evidence, such as a hard-to-reproduce bug, a performance investigation with before-and-after measurements, or a feature spanning multiple components.
- Prefer a focused skill when only one step needs structure, such as tracing affected callers or reviewing a diff. Use the project's normal workflow for routine edits and straightforward checks.
- Use it in the chat that owns the assignment. Planner or Brain can use it for an authorized investigation, Builder for implementation and verification, and Reviewer for an independent review. It can also support a bounded Sweeper investigation within that role's read-only scope.

## How to use it

1. Check the active host's skill picker or supported skill discovery for the approved PStack variant. Use its actual registered invocation, such as `$poteto-mode` in Codex or `/poteto-mode` in Cursor. Use an explicit invocation for the current assignment. Example for Codex:

   ```text
   $poteto-mode Reproduce the token export regression, fix it within the
   approved scope, and verify the affected exports using the existing tests.
   ```

2. Give it the outcome, relevant context, scope, and acceptance evidence. Use the selected playbook within that assignment. Steps that need separate authorization, including delegation, history or connector access, cross-chat dispatch, external writes, merge, deployment, or recurring work, still require it. Keep the assigned role accountable and use existing project routes.
3. Return evidence through the normal handoff, including any skipped steps that affect confidence. If the skill or an optional capability is unavailable, continue with the project's standard workflow. Report a blocker only if required work cannot proceed through a supported route.

Project setup includes this guidance with the software standards. Record any approved project-specific use or restrictions in the project profile. Plugin installation, upgrades, hook trust, persistent mode, optional agent profiles, and automations require separate authorization. Check availability on each host before invoking the tool.
