# Engineering guidance for delegated work

Use this reference when design, implementation, or review involves a concrete complexity tradeoff. It is especially useful when directing Sol/Luna work where previous results added unnecessary defenses or widened scope; treat that as task evidence, not a universal model trait.

## Optional companion and authorization

`right-sized-engineering` defines proportionate engineering standards. Suggest it only when a concrete over- or under-engineering decision would materially change the approach. Use it after explicit invocation or user approval; delegation authorization and model choice alone do not enable it. Do not interrupt routine work to propose it.

When the user has enabled it for the current task, carry that authorization into relevant associate assignments without asking again for each agent. Resolve its installed `SKILL.md` from the current skill catalog or the user-provided location and supply the actual path. If unavailable, report that limitation and continue with the task's explicit requirements; do not claim the companion was loaded. Do not automatically install it or copy its full policy here.

## Put requirements in the brief

Use the existing assignment fields rather than adding a mandatory form:

- **Inputs:** identify the enabled skill, authoritative plan, and relevant contracts. Ask the associate to read the skill and only the references needed for its slice.
- **Boundaries:** state the current consumers, supported states, owned files, preserved protections, and decisions reserved for the lead. Specify concrete exclusions when prior evidence makes them useful.
- **Acceptance:** require supported behavior and proportionate verification; evaluate added complexity and findings against the enabled standard.

For design analysis, ask for the fewest concepts and authoritative facts that serve confirmed consumers, with evidence for proposed mechanisms. The lead resolves material architectural choices.

For implementation, anchor the change to the accepted behavior and scope. Require justification for extra mechanisms and preserve protections at real trust, concurrency, and durable-state boundaries.

For review, require reachable conditions, an owned consequence, and evidence for blocking findings. Separate confirmed defects, optional simplifications, and preferences. Do not prime an independent reviewer with expected findings or require it to find a minimum number of issues.

A compact addition after the companion has been enabled:

```text
The user enabled right-sized-engineering for this task. Read [actual SKILL.md path]
and its relevant references. Apply it within [owned scope] against [current contract].
Justify additional mechanisms using current consumers and reachable consequences.
For review findings, give the trigger, consequence, and evidence; distinguish
confirmed defects from optional changes. Preserve [specific required protections].
```

Keep the companion as the source of engineering policy. Tailor the brief to actual risks instead of repeating its rules in every role profile. On follow-up, carry forward the enabled standard and update only changed facts or constraints. The lead checks the artifact and evidence against that standard; a declaration of compliance is not acceptance evidence.
