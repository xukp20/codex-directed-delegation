# Evidence and triage

Use for locating relevant code, reconstructing events, reproducing an issue, and testing bounded hypotheses. The lead decides a cross-system root cause and repair direction when evidence requires deeper judgment.

## Assignment additions

Provide the observed failure, expected behavior, time/version or run identity, relevant entry points, and permitted diagnostic operations. Mark previous diagnoses as hypotheses. Explicitly separate read-only inspection from commands that mutate state.

```text
Trace this observed failure from [entry point] through its actual callers and state.
Check hypotheses [A/B] against logs and code; record evidence against them as well.
Return the shortest supported causal chain with file/symbol or event references.
Identify the smallest reproduction or next observation that distinguishes remaining causes.
Do not patch code, restart services, or modify runtime data in this assignment.
```

## Return and acceptance

Return observations, causal candidates, contradictory evidence, and unresolved discriminating checks. Distinguish historical reports from current observations. Locate the affected path rather than listing every keyword match.

Do not infer root cause from the last error string alone. If reproduction is unavailable, state the limit; do not convert a plausible explanation into a confirmed diagnosis.
