# Batch transformation

Use for source transcription, structured extraction, repeated edits, and migrations with a defined mapping. For live durable data, the lead first decides and authorizes the recovery procedure; this template does not supply blanket mutation authority.

## Assignment additions

Define the input inventory, transformation rules, content or identity invariants, output location, exception handling, and coverage requirements. Specify whether adjacent items carry context and who owns their joins. Prefer deterministic scripts for exact mechanical changes.

```text
Transform items [range] under rules [mapping] into [output location].
Preserve [content/identity/order]. Read neighboring items for context but write only your range.
Flag ambiguous items with source locations instead of guessing or dropping content.
Validate [coverage and invariants]; return processed, skipped, failed, and ambiguous items.
Do not overwrite accepted outputs outside the range or change the transformation rules.
```

## Return and acceptance

Return the outputs, input-to-output coverage, exception list, and invariant checks. For resumable batches, record completed items at useful intervals and preserve failures so resumption does not rerun accepted work unnecessarily.

For migrations, include the agreed preview, backup, apply, and canonical-load evidence where the procedure requires them. Never bypass validation to force acceptance. Check staged and submitted artifacts, not only the edited source: changes may need explicit restaging before validation.

The lead reconciles cross-slice boundaries and validates aggregate coverage; local success does not prove whole-document or whole-dataset consistency.
