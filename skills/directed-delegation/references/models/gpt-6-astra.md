# GPT-6 Astra

Consider this preset for work whose value depends on resolving substantial uncertainty: establishing a foundational design, interpreting interacting constraints, comparing consequential alternatives, or independently evaluating an important result. These uses apply across domains and are not exclusive roles.

## Settings

The [profile](../../assets/models/gpt-6-astra.toml) defaults to `low` reasoning and standard service tier. It does not override context size; inspect the resolved session value before relying on a particular input capacity.

Use `low` when evidence, candidate, and criteria are already clear and the task primarily requires checking consistency, completeness, or support. Consider an explicit `medium` setting for foundational design, unresolved structural choices, or difficult tradeoffs. Choose by judgment required, not merely by whether the task is called design or review. Explicit user settings always prevail.

## Assignment guidance

Supply the decisive facts, constraints, alternatives where known, and specific questions to resolve. Ask for a recommendation with evidence and remaining uncertainty. Keep the assignment focused on consequential judgment; delegate large inventories or repetitive verification separately when useful.

For economical automatic selection, prefer concentrated design or evaluation assignments over routine iteration. A stable candidate and primary evidence make independent evaluation useful. Ongoing implementation or repeated intermediate checks can use another suitable model unless the user requests otherwise or observed difficulty justifies this one.

Basis: user-selected preset guidance, reviewed 2026-09-10; not a claim about measured capability or pricing. Apply the shared [precedence and verification rules](index.md).
