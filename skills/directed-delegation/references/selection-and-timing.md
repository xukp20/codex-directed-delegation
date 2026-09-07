# Selection, timing, and reuse

Use this branch when the user asks the lead to use or organize subagents as needed throughout an execution, or when a delegation decision needs planning. Do not make it a preliminary ceremony for an already clear assignment.

## Ongoing delegation

An instruction such as “complete this work and use subagents as needed” authorizes the lead to select, dispatch, and reuse associates throughout that task. Reassess at meaningful stage changes: a long execution may expose broad exploration, large-scale inspection, analysis, or well-specified implementation suitable for one or several associates. Do not wait for the user to enumerate each subtask or ask permission again. Respect subsequent limits and the overall task scope; this does not authorize unrelated work or unrequested configuration changes.

Use multiple associates when independent inputs or questions justify parallel work, and retain tightly coupled or decision-heavy work with the lead. “As needed” does not impose a fixed agent count or require delegation at every stage.

## Allocate judgment

Delegate work with clear criteria, substantial input or repetition, bounded dependencies, and outputs the lead can check economically. Keep ambiguous goal interpretation, architecture, contract selection, runtime configuration, and consequential recovery planning with the lead. Evidence collection for those decisions can still be delegated. Neither code nor research is inherently a lead-only task.

A reviewer on a smaller model can detect specified violations and gather counterexamples. Do not treat that as sufficient adjudication of an unfamiliar proof or ambiguous architecture. Strong reasoning settings do not remove model capability differences.

Account for briefing, waiting, and verification costs. Keep short tightly coupled work local when delegation adds no useful capacity. Use scripts for deterministic enumeration or transformation; an agent is useful where inspection or interpretation remains necessary.

## Split and dispatch

- Split read-heavy work by source range, subsystem, or independent question. Assign coverage explicitly to prevent gaps and unnecessary duplication.
- Dispatch independent pieces together once their inputs and criteria are ready. While they run, do useful lead work rather than duplicate their scans.
- For dependent work, wait for the required candidate or stable input. Do not send reviewers a moving target and call the review final.
- Give neighboring slices enough read-only overlap to understand boundaries, but assign one owner for each output boundary. The lead resolves shared identifiers and global relationships.
- Parallel writers need disjoint write scopes or actual isolation. Shared indexes and aggregate files normally have one integrator. Worktrees are useful where isolation is needed, not compulsory for every reader.
- Migration and audit may run together only when the audit uses stable evidence or a snapshot; reading live changing data can produce inconsistent conclusions even without write conflicts.

Start with the smallest useful group. Batch sizes and concurrency follow available slots, dependencies, actual costs, and user requirements, not a fixed “six agents” rule. Do not recursively delegate by default.

When exact model settings matter, use a compatible configured role and verify what is actually applied. Follow the live tool's inheritance restrictions; do not silently replace a requested model, reasoning level, or service tier.


## Reuse or start independently

- Reuse the same associate for related or consecutive assignments when its existing context materially helps: inspecting a subsystem and then tracing a related failure, implementing an accepted change and correcting it, or continuing batches under the same rules. Send the new objective, changed facts, input boundaries, and acceptance criteria rather than repeating the entire briefing.
- Sequential reuse preserves useful context; it does not make old observations current. Require a targeted refresh when files, versions, or accepted decisions have changed. Complete or explicitly redirect the current assignment before giving that associate conflicting work.
- Start a separate associate for unrelated work with no useful shared source context. Provide a self-contained brief and relevant inputs rather than inheriting unrelated conversation history. Prefer independence also when stale assumptions or excessive unrelated context would outweigh reuse.
- Preserve review independence even when subjects overlap: the author may handle repairs, while a separate reviewer checks the stable candidate. Reuse that reviewer for subsequent checks of those repairs when appropriate.
- Relatedness alone does not require serialization. If related tasks can run independently and parallelism is worthwhile, use separate associates with the same bounded source basis and distinct scopes; let the lead reconcile their results.
