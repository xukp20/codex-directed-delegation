# Planned implementation

Use once the behavior and approach are settled enough for a bounded implementation. A requirement to discover an architecture belongs with the lead, with optional delegated evidence gathering.

## Assignment additions

Provide the accepted plan section, current baseline, owned files/modules, relevant APIs and invariants, concrete before/after behavior, and focused validation. Define which local implementation choices remain flexible.

```text
Implement [accepted behavior] using [chosen approach] in [owned scope].
Read [plan section] and [current contract]; preserve [specific invariants].
Other agents own [neighboring scope]. Do not revert their edits or change shared interfaces.
Run [focused checks] and report the actual diff and outcomes.
If the plan conflicts with the current API or requires a new public contract,
return the conflict and smallest options to the lead before expanding the change.
```

## Return and acceptance

Return changed files, resulting behavior, exact checks and outcomes, and deviations. No commit, push, deployment, or broad refactor is implied by a local implementation assignment.

Review the actual change against the accepted plan and relevant callers. Do not accept a patch merely because its tests mirror its implementation. After a local correction, recheck the affected behavior rather than restarting unrelated testing.
