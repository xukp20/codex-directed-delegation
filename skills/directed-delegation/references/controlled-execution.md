# Controlled execution

Use for running an already chosen procedure, focused tests, a build, or bounded operational checks. The lead chooses environment, parameters, recovery policy, and consequential changes.

## Assignment additions

Provide commands or an authoritative runbook, working directory, environment, required preflight, stage order, time/cost limits when relevant, expected outputs, and retry/stop conditions. Do not place credentials in the brief.

```text
Execute [procedure] in [workspace/environment] after [preflight].
Use the selected configuration unchanged. Success requires [artifact/business condition],
not merely a zero exit status. Save bounded logs and exact command outcomes.
On [known transient condition], use [approved retry]; on other failure, preserve evidence
and report the failed stage and recovery candidate to the lead. Do not restart completed stages.
```

## Return and acceptance

Return completed stages, command outcomes, duration, artifacts, and outstanding business checks. Distinguish running, interrupted, failed, and successful work.

Use an available completion-aware waiting mechanism for long operations rather than repeated model polling. Do not leave an unowned background process or treat the monitoring process's exit as business completion. If a procedure fails repeatedly without new evidence, return control to the lead for diagnosis rather than increasing limits or changing parameters yourself.
