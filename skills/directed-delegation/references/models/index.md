# Optional model presets

Use these cards when choosing a model automatically or configuring a requested profile. Read only the relevant cards. The delegation workflow remains model-independent.

## Selection and precedence

Explicit user model and parameter choices take precedence over established task configuration, which takes precedence over these defaults. If the user names only a model, fill unspecified settings from the task configuration or its preset. Do not silently substitute a different model or effort when a requested setting is unavailable.

| Model card | Consider for | Assignment emphasis |
| --- | --- | --- |
| [GPT-6 Astra](gpt-6-astra.md) | Judgment-intensive analysis, ambiguous constraints, consequential alternatives, independent evaluation | Concentrate evidence, unresolved questions, and evaluation criteria |
| [GPT-5.6 Sol](gpt-5.6-sol.md) | Sustained analysis, implementation, diagnosis, coordination, and review requiring synthesis | Define outcomes and boundaries; allow routine decisions within the assignment |
| [GPT-5.6 Luna](gpt-5.6-luna.md) | Bounded research, implementation, transformation, and checks with clear standards and economical verification | Specify coverage, examples, exceptions, and manageable batches |

These are practical recommendations, not benchmark claims, exclusive capabilities, or fixed job titles. Task size alone does not determine model choice. Prefer deterministic scripts for deterministic work; use agents where interpretation remains useful. Escalate when the unresolved judgment or correction cost warrants it, rather than repeating an unsuccessful assignment unchanged.

## Defaults and maintenance

The linked TOML assets are the source of truth for installable defaults. Cards explain when an explicit adjustment is useful. They do not establish account availability or effective context limits; verify resolved settings when applying a profile.

To add a model, add one focused card here, one TOML asset under `assets/models/`, and an entry in this table. Record the basis and date of recommendations, distinguish requested settings from observed runtime behavior, and update installation links. Do not rewrite the core workflow or add a registry for a new preset.

Basis: user-selected working preferences and existing repository presets, reviewed 2026-09-10. Reassess against actual assignment results and installed runtime support when models or tools change.
