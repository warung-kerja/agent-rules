# Core rules

Updated: 2026-10-25.

Read and follow the [principles for every session](session-principles.md). They are the shared baseline for every role, including non-product work. This document adds operational detail; it does not replace those principles.

## Sources of truth

- **agent-rules:** shared standards, role definitions, and reusable processes.
- **Product repository:** code, project profile, architecture decisions, operating instructions, and verification evidence.
- **Linear:** scope, priorities, ownership, dependencies, acceptance criteria, and execution status.
- **GitHub:** branches, PRs, review findings, and merge evidence.
- **Chats:** coordination and discussion. Move durable outcomes into the appropriate source above.

Verify live state before acting. A historical handoff, stale ticket, or previous review is evidence, not proof of the current checkout, PR head, deployment, or permissions.

## Scope and authority

Follow applicable runtime instructions, the owner's current authorization, and project-specific constraints. These shared standards establish the baseline; they cannot override higher-priority instructions or grant tools and permissions. Record local exceptions with a reason and owner.

A new ticket is intake, not automatic execution permission. The project must define what may be dispatched and implemented without further approval. Continue work already authorized; ask only when required information or authority is genuinely missing. Prepare a concrete, reviewable result before requesting a final approval.

Planning, implementation, review, merge, deployment, and publication are distinct actions. Technical readiness alone does not authorize the next action. Do not bypass an approval rejection by changing tools, agents, or transport.

## Ownership and coordination

Use one primary owner per assignment and one writer per shared artifact. Builder owns implementation; Manager owns routine Linear maintenance. Other roles send evidence and proposed updates to Manager. If Manager is unavailable, retain the handoff in the product repo and report the blockage; avoid a second competing task board.

Use isolated branches/worktrees when work could collide. Do not overwrite another session's changes. Limit Builder to one active assignment by default; queue additional work. Parallel builders require explicit ownership and an integration plan.

Cross-chat messages require owner authorization for the specific project team and routes. Do not infer that authorization from this library. Send self-contained assignments and meaningful state changes; avoid acknowledgement loops. Record dispatch before sending, verify acceptance afterward, and reconcile uncertain delivery before retrying.

## Build and review

Prefer small, focused PRs. Verify changed behavior proportionately, including required project checks. Broaden or repeat checks when a new change, failure, or concrete unresolved concern justifies it. State what passed, what failed, and what remains unverified.

Reviewer independently inspects the current PR head and base, relevant diff, regression risks, and verification. A review verdict names the exact head SHA. A changed head needs a fresh verdict. Reviewer sends fixes back to Builder rather than rewriting the code being reviewed.

Do not call work Done solely because code exists or a PR is open. Each project defines whether Done means merged or deployed/accepted. Record implementation, merge, and deployment separately when they differ.

## Cost and continuity

Use the cheapest capable model and appropriate effort. Default suitable routine ticket updates, formatting, and mechanical work to Luna 6 where available. Preserve the accountable role and its context; preferred session models do not require every task to use that model. Model changes follow the [automatic same-family upgrade policy](model-presets.md). Delegation and model changes must respect the runtime, project configuration, explicit pins, and agreed scope.

Delegate bounded tasks when it improves the outcome. Parallelise independent work with clear inputs, ownership, and completion criteria. Integrate results and close finished workers; the parent session remains accountable.

Use Brain for consequential architecture, hard unresolved tradeoffs, and substantial brainstorming. Routine planning stays with Planner. Manager coordinates; Sweeper discovers; Builder implements; Reviewer reviews.

Record durable decisions with context, rationale, and consequences in the product repo. Respect pause/cancel and existing holds across sessions and machines. Never turn an old backlog or roadmap into new authority.

## Public-library hygiene

Store reusable, sanitized instructions here. Keep secrets in the project's approved secret mechanism. Do not commit private task content, customer material, internal identifiers, or machine-specific settings merely to make a template realistic.
