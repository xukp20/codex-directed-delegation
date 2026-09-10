# Configure an associate

Read only when the user asks to create, replace, or customize a subagent profile. Ordinary delegation does not authorize configuration changes.

## Example and registration

Choose a general associate profile; each assignment supplies its responsibility and write boundary.

| Profile | Model | Reasoning | Nominal context |
| --- | --- | --- | --- |
| [luna_associate](../assets/models/gpt-5.6-luna.toml) | `gpt-5.6-luna` | `max` | `1000000` |
| [sol_associate](../assets/models/gpt-5.6-sol.toml) | `gpt-5.6-sol` | `high` | `272000` |
| [astra_associate](../assets/models/gpt-6-astra.toml) | `gpt-6-astra` | `low` | No override; verify resolved value |

All examples use `service_tier = "default"` (standard, not fast). These are selectable presets, not requirements of the workflow or claims about every model's supported settings. Sol explicitly sets 272k so it does not inherit a larger parent context; preserve that setting unless the user requests an adjustment. See the [model cards](models/index.md) for task recommendations and parameter precedence. Astra defaults to low; medium is an explicit choice for work requiring more unresolved judgment, not a second default.

Preset assets now live under `assets/models/`; existing installed role names remain unchanged. Moving an asset does not update an independently copied installed profile. Compare the selected file with the installed copy when synchronization is requested.

Use a standalone role file containing `name`, `description`, and `developer_instructions`, plus the selected model settings. For a personal installation, copy the selected example to `$CODEX_HOME/agents/<role_name>.toml` (normally `~/.codex/agents/`). Register only the requested roles explicitly in the main config when using named role references:

```toml
[agents.luna_associate]
config_file = "agents/luna_associate.toml"

[agents.sol_associate]
config_file = "agents/sol_associate.toml"

[agents.astra_associate]
config_file = "agents/astra_associate.toml"
```

The role name and the file's `name` must agree. Current Codex also discovers standalone files in the agents directory. Explicit registration points to the same file; do not create a second profile with a different identity for it.

## Apply a requested change

1. Inspect the current config and existing target role. Preserve unrelated settings, credentials, other roles, and user edits. Check installed-version support against the [official subagent documentation](https://learn.chatgpt.com/docs/agent-configuration/subagents) and local configuration loader when necessary.
2. Honor extra user requirements for model, effort, nominal context, or tools. Keep the example small; do not copy account credentials, parent-wide defaults, or unrelated settings into the profile. Omitted permissions inherit; assignment prose alone is not a sandbox.
3. Prepare a private backup outside scanned agent directories. Add the new file and its main-config reference. Remove an old role and its file only when replacement is requested. Do not globally change `default_subagent_model` merely to register one selectable associate.
4. Parse TOML and load configuration with the installed Codex. If a spawn is part of the requested validation, use a harmless bounded task and inspect the resolved role/model/effort/context/tier where exposed. Role files may override explicit spawn model and effort, so do not use a mismatched role as a generic shell for another model.
5. Distinguish written configuration, successful config loading, and observed runtime settings. Nominal context can be reduced by the model's effective-window policy. Do not silently inflate it to hit an effective target; explain the difference. Existing sessions may retain their old role catalog; reload before claiming the new role is available there.

If capabilities or requested parameters are unavailable, report the specific limitation rather than falling back to another model or fast tier. Installing this optional profile does not automatically invoke this skill.
