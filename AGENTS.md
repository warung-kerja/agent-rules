# Working in agent-rules

This repository is the shared library of agent standards and workflows. It is not a product-development app; do not create the six-session product team for this repo by default.

- Read README.md, standards/session-principles.md, and only the relevant standards/workflows/templates. Apply the shared principles to work in this repository as well.
- Before asking for an API key or token, follow the credential lookup rule in standards/core-rules.md: check `02_Business_Operations/docs` in the local Obsidian vault first. Never expose or commit credential values.
- Keep reusable rules here and project-specific configuration in the consuming project.
- Keep the role definitions and their copy/paste prompts consistent.
- When changing expected behavior, update CHANGELOG.md and relevant adoption guidance.
- Mark suggestions as defaults; distinguish written policy from installed/verified automation.
- Do not claim that a linked file is automatically loaded by another agent runtime.
- Preserve user authorization boundaries. A role or ticket label does not grant tool access, cross-chat messaging authority, merge permission, or deployment permission.
- Keep all committed material suitable for a public GitHub repository. Do not copy private source material, credentials, host paths, or conversation IDs into this library.
- Check Markdown links, placeholders, role consistency, and git diff whitespace. Documentation-only changes do not require application tests.
