# Refresh an existing session

Use this after a deliberate rules update. Replace `<TARGET_REVISION>` with the reviewed, merged commit SHA selected for the project, then send the prompt to each existing session that needs refreshing. Use the same revision across the project; do not leave the placeholder unresolved or substitute a moving branch. The role descriptions remain in `roles/`, not in this prompt.

One designated project owner should prepare shared adoption changes under the [adoption workflow](../workflows/adopt-and-update.md). Other sessions load the adopted revision and provide acknowledgement evidence without concurrently editing shared configuration. Sending this prompt refreshes the receiving session only; it does not broadcast to other chats or install automatic updates.

## Copy-and-paste prompt

```text
Refresh this session to use the centralized role definitions from:
https://github.com/warung-kerja/agent-rules
Target revision: <TARGET_REVISION>

Read the project's current instructions, project profile, and session register.
Identify this session's existing role and project preset; preserve its identity,
context, active assignments, holds, project exceptions, and authorization.

Fetch or obtain a readable copy of the library and resolve the target revision
to its full commit SHA. Read README.md, standards/session-principles.md,
standards/core-rules.md, standards/model-presets.md, workflows/adopt-and-update.md,
the selected preset's setup guide, and its linked roles/<role>.md at that revision.
Compare the target with the project's currently adopted revision and identify
relevant changes or conflicts before applying them.

Follow the project's adoption process. If the target is not yet adopted, the
designated owner prepares one adoption PR or the project's documented equivalent.
Other sessions report their readiness or blockers and retain the current adopted
rules until adoption is complete. Do not independently advance a shared adoption
record or claim a proposed revision is already adopted.

At a safe assignment boundary, use the adopted canonical role file as this
session's role definition. Apply its purpose, outputs, completion rules, and only
the responsibilities relevant to this project's preset. Preserve explicit local
exceptions and report conflicts rather than silently removing them.

Replace outdated copied role instructions through supported mechanisms with a
reference that explicitly directs this session to read the canonical file at the
adopted revision. Coordinate project-profile, snapshot, entrypoint, and register
changes through the designated owner using already-authorized routes. If messaging
is unavailable or unauthorized, return the handoff in this chat for the owner.
Keep one writer for shared configuration. Record or provide acknowledgement
evidence for the full adopted SHA, role-file path, preset, and refresh status.

Do not create sessions, install routines, message other chats without existing
authorization, or expand permissions as part of this refresh. If a source is
inaccessible or a conflict remains unresolved, retain the last verified adopted
rules and report the specific blocker. Do not claim that reading a file changed
persisted runtime instructions unless that update was actually verified.

Confirm briefly:
- Your role and project preset
- The canonical role file and full revision you loaded and applied
- Any meaningful behavior changes, local exceptions, or unresolved conflicts
- Whether this session is refreshed and any shared adoption work still pending

Then continue your existing authorized assignment, or wait if none is active.
```
