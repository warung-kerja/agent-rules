# Simple, complete implementation

Updated: 2026-11-22.

Apply this standard when planning, writing, fixing, or reviewing software in any preset, including prototypes, websites, scripts, and tools. It does not impose development checks on non-code work or require a product team. Follow the project's adopted revision, acceptance criteria, constraints, and authorized scope.

## Understand the change

Read the relevant implementation and trace the affected flow before choosing a solution. Find callers, shared helpers, interfaces, tests, fixtures, configuration, and exports that must change together. For a bug, identify the root cause and affected callers rather than patching one symptom. Check consequences for existing users, stored data, and compatibility.

## Choose the simplest maintainable solution

Use the first suitable option that meets the full requirement:

1. Reuse the project's existing component, helper, service, or established pattern.
2. Use a standard-library or platform feature when it fits the project's conventions.
3. Use an appropriate installed dependency.
4. Add the smallest clear implementation or a justified new dependency.

Before adding a dependency, consider capability, correctness, security, accessibility, compatibility, and ongoing maintenance. A mature library can be simpler to maintain than custom code; a package for a trivial helper often is not. Explain material dependency choices briefly.

Avoid unrequested features, speculative abstractions, wrappers, configuration, and flexibility for hypothetical future needs. Preserve the project's architecture and interfaces. Remove obsolete code caused by this change when safe; capture unrelated improvements separately. Prefer readable code over clever compression. Judge simplicity by maintenance and completeness, not line count or the shortest diff.

## Finish and verify the whole change

Update every affected caller, fixture, configuration, export, and relevant document needed for the agreed outcome. Preserve validation at trust boundaries, security, accessibility, error handling, recovery from failed writes, and protection against data loss. Small code is not permission to reduce the requested behavior or quality.

Use the existing test framework and run required project checks. Add or update focused behavioral tests when new logic or a bug fix introduces meaningful regression risk, especially parsers, money, permissions, data writes, and recovery paths. Tests should fail for a plausible defect; a token assertion is not sufficient evidence. Trivial presentation or documentation edits do not require new tests by default. Broaden checks only for project requirements, failures, or concrete unresolved risks. Verify the intended user outcome proportionately and state what remains unverified.

Record a deliberate limitation with its impact and the condition that would justify revisiting it, in the appropriate code comment, decision record, or task. Use the project's existing convention; no special comment prefix or debt tool is required.

## Review and report

Inspect connected code as well as the diff. Prioritize correctness, security, data integrity, expected load, and meaningful verification before opportunities to simplify. Support findings with a concrete failure case or demonstrated unnecessary complexity. Keep existing independent-review and exact-revision verdict requirements; this standard adds no extra mandatory review gate.

Report the outcome, relevant verification, and material limitations or risks concisely. Do not add repetitive disclaimers when nothing meaningful remains unchecked. Continue authorized work without repeated preference questions; raise consequential tradeoffs or scope gaps when needed.

## Origin and optional tooling

Before choosing a PStack playbook for software work, read [optional PStack playbooks](pstack.md) at the adopted revision.

Inspired by Dietrich Gebert's [Ponytail skill](https://github.com/DietrichGebert/ponytail/blob/main/skills/ponytail/SKILL.md) and [review skill](https://github.com/DietrichGebert/ponytail/blob/main/skills/ponytail-review/SKILL.md), reviewed on 2026-11-22 (plugin manifest version 5.3.3, MIT). This is independently written Warung guidance; the adopted agent-rules commit is its source of truth. It does not track upstream changes automatically.

Ponytail's plugin, commands, mode switches, lifecycle hooks, and local metrics are optional. Do not install, enable, or trust them as part of rules setup. They are not required to apply this standard. If separately requested, check compatibility and conflicts with the project's rules and verify actual runtime behavior. Neither installation nor instruction loading proves compliance or measured savings.
