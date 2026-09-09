---
name: directed-delegation
description: "Select, brief, and verify subagents when the user requests delegation or the agent identifies concrete independent subtasks worth parallelizing. Also use when explicitly invoked. Task size or uncertainty alone is not a reason to delegate."
---

# Directed Delegation

Help a capable lead agent direct a less expensive execution agent through clear assignments. Model names are examples, not fixed roles: the lead owns consequential engineering decisions and integration within the user’s authorization; associates gather evidence, implement settled plans, and check defined criteria. Decisions explicitly reserved by the user remain with the user.

## Invocation

Use when the user requests delegated work, invokes this skill, or the lead identifies concrete independent subtasks whose parallel execution would materially help the authorized task. The lead may select the skill and organize those assignments without a separate user request, subject to current session rules and explicit user limits. Keep short, tightly coupled work local when coordination adds no useful capacity. A request to discuss or configure subagents authorizes only that discussion or configuration, not launching work. A request to use subagents as needed grants ongoing delegation discretion within the authorized task, including long-running work; do not ask again for each in-scope assignment. Use the existing subagent tools and their live contracts; do not reproduce their orchestration API here or create sidebar tasks as substitutes.

## Write the assignment

Resolve the choices that determine correctness before dispatch. If the approach is unsettled, assign evidence collection rather than asking the associate to silently choose the architecture. Give enough context to execute independently without copying unrelated history or abandoned proposals.

Include the following information when it matters; this is a compact briefing, not a mandatory form:

```text
Outcome and use: Deliver [result] so the lead can [next decision/action].
Inputs: Work in [absolute location]. Read [authoritative sources] and cover [range].
Current basis: [verified facts], [accepted decisions], [hypotheses still to test].
Assignment: [specific questions, rules, or ordered steps]. Preserve [invariants].
Boundaries: [read/write scope], [other writers], [decisions reserved for the lead].
Acceptance: [observable completion criteria and focused verification].
Exceptions: Handle [routine cases]; return [material deviations] to the lead.
Return: [artifact/result], evidence locations, coverage, unresolved items, and checks.
```

- Replace vague instructions such as “check everything” with an inventory, question set, or observable criteria. Supply a small example when a classification or transformation is otherwise ambiguous.
- Identify the authoritative plan and exact assigned portion. References can carry detail; a summary must not discard constraints the associate needs. Do not require reading an entire project when a bounded source set suffices.
- Separate observations from hypotheses. For independent review, provide the candidate, requirements, and primary evidence without the author's verdict or suggested findings.
- Give permission to resolve routine in-scope details, but reserve changed requirements, architecture, runtime configuration, and consequential recovery choices for the lead. Do not prescribe shell commands when only the outcome matters; do supply exact steps for fragile ordered operations.
- For writers, name their owned files or data slice and shared hotspots. State that they are not alone, must preserve others' edits, and must not revert concurrent work. Read-only reports may have a separate permitted output path.
- For large inputs, assign explicit coverage and manageable batches. Preserve source locations and boundary context. A large context window is capacity, not a reason to inherit all conversation history.

## Collect, correct, and accept

Require a concise conclusion with traceable evidence rather than raw logs. Distinguish checked, skipped, failed, and unknown items; “no issues found” applies only to the inspected scope. For changes, obtain the actual artifact or diff and completed verification results, including failures that affect acceptance.

Check the result against the assignment and inspect consequential claims at their source. Scale verification to risk: representative sampling can check routine extraction, but does not certify full coverage or high-consequence invariants. A successful command or another agent's approval alone does not establish task completion.

Send focused follow-ups describing the mismatch, evidence, desired correction, and unchanged boundaries. Reuse the associate for related corrections; use a separate reviewer when independence matters. If the plan is invalid, evidence conflicts, or the same failure recurs without new information, resolve the issue at the lead level instead of repeating the assignment. Ask the user only for genuinely user-owned choices that remain outside existing authorization.

The lead combines outputs, resolves cross-slice conflicts, and owns the final conclusion. Do not reread every low-risk input by default and erase the benefit of delegation. Keep substantive source evidence accessible for targeted checks.

## Task references

Read only the reference matching the assignment; combine two when the task actually has both stages.

| Assignment | Reference |
| --- | --- |
| Search, extract, compare, and summarize many sources | [Research and synthesis](references/research-and-synthesis.md) |
| Trace code, logs, and observed failures | [Evidence and triage](references/evidence-and-triage.md) |
| Implement a settled bounded plan | [Planned implementation](references/planned-implementation.md) |
| Convert or repair many items under explicit rules | [Batch transformation](references/batch-transformation.md) |
| Inspect artifacts against defined criteria | [Criteria-based review](references/criteria-based-review.md) |
| Run an approved procedure and report its outcome | [Controlled execution](references/controlled-execution.md) |

## Optional branches

- When organizing user-requested or self-selected delegation during execution, read [selection, timing, and reuse](references/selection-and-timing.md). Also use it for task splitting, dependent dispatch, or choosing whether to reuse an associate; apply it as new work arises without rereading it for every assignment.
- Only when asked to create or change a subagent profile, read [configuration](references/configure-subagent.md). It includes selectable Luna max / nominal 1m and Sol high / nominal 272k standard-tier profiles. Normal delegation does not install or change configuration.
- For design, implementation, or review with a material engineering complexity tradeoff, read [engineering guidance](references/engineering-guidance.md). It explains how to suggest the optional `right-sized-engineering` skill and carry an already authorized standard into assignments and acceptance, including Sol/Luna work. Model selection alone does not activate that companion.
