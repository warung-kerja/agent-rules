# Principles for every session

Updated: 2026-10-25. Applies to every role and session, including work outside product development. The six-session team remains conditional on the project being product development.

These are the shared baseline. Apply them within the owner's agreed scope, applicable runtime instructions, and project-specific constraints. Role definitions explain responsibilities; these principles govern how each role works.

1. **Keep checks focused and proportionate.** Test the changed behaviour and meaningful risks. Reuse valid evidence; repeat or broaden checks only when a change, failure or unresolved concern justifies it.
2. **Route work to the right session.** Use the existing planning, builder, review or Tickets chat that owns the work. Preserve its context and avoid duplicate assignments.
3. **Use the cheapest capable model and appropriate effort.** Default routine ticket updates, formatting and mechanical work to Luna 6 where available. Reserve stronger models and higher effort for complexity, uncertainty and consequential decisions.
4. **Delegate when it improves the outcome.** Give subagents bounded tasks with clear inputs, ownership and completion criteria. Parallelise independent work, integrate their results and close finished workers.
5. **Keep one accountable owner for each outcome.** Delegation does not transfer responsibility for completion. Each shared file or mutable record should have one writer at a time.
6. **Keep Linear aligned with reality.** Search before creating tickets. Update status at meaningful transitions, record blockers and link the PR or evidence. Define “Done” clearly for each project; distinguish implementation, review, acceptance and deployment.
7. **Commit and push at meaningful milestones.** Keep commits coherent and scoped. Preserve completed work on GitHub and open reviewable PRs without mixing unrelated changes or private data.
8. **Make the smallest complete change.** Solve the agreed problem, favour existing mechanisms and subtract unnecessary complexity. Capture worthwhile adjacent work as follow-up tickets.
9. **Verify the actual user outcome.** Passing tests support acceptance, but the main journey and important recovery paths must work. State clearly whether evidence comes from fixtures, browser checks or the live service.
10. **Use independent review where it matters.** Give substantial or risky changes a fresh review context. Review the actual current revision, close material findings and recheck affected behaviour after fixes.
11. **Protect production while developing.** Use isolated checkouts and disposable data. Treat merging, deploying and publishing as distinct actions, with the project’s relevant authorization and recovery procedure.
12. **Act independently within the agreed scope.** Resolve routine implementation choices without repeatedly asking permission. Escalate material scope changes, consequential tradeoffs, missing authority and persistent blockers.
13. **Report in clear human language.** Lead with the outcome, its practical meaning and anything requiring attention. Keep technical detail behind concise evidence links; report failures and limitations plainly.
14. **Preserve useful knowledge in the right place.** Keep tasks in Linear, implementation evidence in the repository and durable cross-project learning in the Wiki. Read relevant context first and verify historical claims against current state.
15. **Communicate meaningful changes without creating noise.** Report completion, material progress, failures and decisions needed. Avoid acknowledgement loops, repeated unchanged checks and unnecessary monitors.

## Applying the principles

- Read these principles at the project's adopted rules revision before acting. For non-product work, read them without creating the product team.
- Preferred role models are starting assignments. Use Luna 6 for suitable routine work where available and routing permits it; keep the accountable role and context intact. Apply verified same-family upgrades under the [model upgrade policy](model-presets.md) and record them; do not silently change families or override explicit pins. Record other agreed substitutions in the project profile.
- Temporary subagents support the accountable session; they do not replace the persistent role sessions. Use delegation only when permitted by the runtime and agreed scope. Do not spawn workers merely to satisfy a quota or add review overhead to a simple task.
- Use Linear, GitHub, and the Wiki where they are part of the project's setup and accessible. If a required destination is unavailable, preserve the evidence in the repository and report the blocker; do not claim the external update succeeded.
- Before asking for API keys or tokens, follow the [credential lookup rule](core-rules.md#api-key-and-token-lookup): check `02_Business_Operations/docs` in the local Obsidian vault first, without exposing credentials.
- See [core rules](core-rules.md) for coordination and authority details and [adoption and updates](../workflows/adopt-and-update.md) for propagating changes.
