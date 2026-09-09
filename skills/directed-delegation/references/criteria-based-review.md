# Criteria-based review

Use for audits, source comparisons, and independent checks against explicit criteria. The lead owns final acceptance and high-ambiguity judgments.

## Assignment additions

Give the candidate version or stable artifact, requirements, source evidence, review dimensions, and desired coverage. Do not give an independent reviewer the author's verdict or expected findings. Make report writing distinct from permission to repair.

```text
Review [candidate] against [criteria] using [primary evidence].
Cover [scope]; return each material mismatch with location, violated criterion,
concrete consequence, and supporting evidence or reproduction.
Separate confirmed defects from questions; report what was not checked.
Do not change the candidate. Write only [optional report path].
```

When `right-sized-engineering` is already enabled, use [engineering guidance](engineering-guidance.md) to pass the standard without suggesting findings. Require reachable triggers and owned consequences for blocking issues; keep optional simplifications distinct.

## Return and acceptance

Return material findings and actual coverage, including a scoped “none found” when appropriate. Do not demand speculative hardening unrelated to supported behavior. Identify what evidence would settle uncertainty.

For repairs, re-review changed portions and their immediate consequences. A second agent is not independent if it merely repeats the first agent's summary. Full source coverage, critical invariants, and subtle mathematical claims need the verification appropriate to those requirements, not an unsupported blanket approval.
