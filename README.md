<h1 align="center">Directed Delegation for Codex</h1>

<p align="center">
  <strong>Clear assignments, traceable evidence, and decisions owned by the lead.</strong>
</p>

<p align="center">
  <a href="skills/directed-delegation/SKILL.md">
    <img alt="Codex Skill" src="https://img.shields.io/badge/Codex-Skill-2563eb?style=flat-square">
  </a>
  <img alt="Focus" src="https://img.shields.io/badge/focus-directed%20subagents-0f8f88?style=flat-square">
  <img alt="Invocation" src="https://img.shields.io/badge/use-requested%20delegation-d97706?style=flat-square">
</p>

<p align="center">
  <a href="#why">Why</a> &middot;
  <a href="#use">Use</a> &middot;
  <a href="#install">Install</a> &middot;
  <a href="#optional-luna-associate">Luna Profile</a> &middot;
  <a href="skills/directed-delegation/SKILL.md">Skill Reference</a>
</p>

`directed-delegation` helps a capable lead agent give less expensive subagents concrete, independently executable assignments. The lead retains consequential decisions and final integration; associates handle substantial reading, settled implementation, transformations, and checks against explicit criteria.

The workflow is model-independent. Astra or Sol can lead and Luna can assist, but neither model family is required.

## Why

A smaller model benefits from knowing what is settled, what evidence to inspect, what it may change, and what completion means. “Investigate everything and fix it” leaves too much judgment implicit. A bounded brief gives the associate useful autonomy without transferring architecture or recovery decisions accidentally.

This skill concentrates on writing that brief and accepting the result. Delegation selection, scheduling, and optional model configuration live in separate references. It does not add another orchestration API or require a task-management framework.

## Use

```text
Use $directed-delegation to have subagents inspect these documents. Return
source-backed comparisons; keep the final architecture decision with the lead.
```

```text
Use a Luna subagent to implement this accepted plan, and another subagent to
review the stable result against the requirements.
```

The skill may be selected when the user explicitly requests subagents, parallel agent work, or a named-model subagent. Ordinary task size or uncertainty does not activate it. Its discovery policy allows matching these explicit natural-language requests, so spelling the skill name is optional. A request to discuss or configure delegation does not launch agents.

A request to use subagents as needed lets the lead organize delegation throughout a long execution, including parallel exploration and large-scale inspection, without asking again for each in-scope assignment. Reuse an associate for related follow-ups that benefit from its context; start independently for unrelated work or independent review. Existing tool contracts and repository policies still apply.

## Assignment contract

| Part | What the associate needs |
| --- | --- |
| Outcome | A concrete deliverable and its downstream use |
| Inputs | Authoritative sources, current facts, and exact coverage |
| Work | Questions, transformation rules, or the accepted plan |
| Boundaries | Owned writes, concurrent work, and decisions reserved for the lead |
| Acceptance | Observable completion and proportionate verification |
| Return | Results, source locations, coverage, and unresolved issues |

Use only the fields that matter. A short assignment can remain a paragraph. Larger tasks can reference an existing plan without copying the whole conversation.

## Task templates

| Template | Typical work |
| --- | --- |
| [Research and synthesis](skills/directed-delegation/references/research-and-synthesis.md) | Inspect and compare many sources, preserve evidence and disagreements |
| [Evidence and triage](skills/directed-delegation/references/evidence-and-triage.md) | Trace code, reconstruct logs, test bounded hypotheses |
| [Planned implementation](skills/directed-delegation/references/planned-implementation.md) | Implement a settled behavior within an owned scope |
| [Batch transformation](skills/directed-delegation/references/batch-transformation.md) | Transcribe, convert, or migrate items under explicit rules |
| [Criteria-based review](skills/directed-delegation/references/criteria-based-review.md) | Audit a stable candidate against requirements and primary evidence |
| [Controlled execution](skills/directed-delegation/references/controlled-execution.md) | Run a chosen procedure with defined outcomes and stop conditions |

Read [selection and timing](skills/directed-delegation/references/selection-and-timing.md) when deciding what to delegate, how to partition it, or when dependent work can start. The main skill remains focused on how to assign and verify work.

## Install

From a local checkout of this repository:

```bash
cd /path/to/codex-directed-delegation
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
ln -s "$PWD/skills/directed-delegation" \
  "${CODEX_HOME:-$HOME/.codex}/skills/directed-delegation"
```

Inspect an existing destination before replacing it. Reload Codex if discovery does not refresh. Installing the skill does not change models, agent profiles, permissions, or service tiers.

## Optional Luna associate

The bundled [profile](skills/directed-delegation/assets/luna-associate.toml) is named `luna_associate`: its task may be research, implementation, execution, or review.

| Setting | Example value |
| --- | --- |
| Model | `gpt-5.6-luna` |
| Reasoning | `max` |
| Nominal context | `1000000` tokens |
| Service tier | `default` (standard; no fast tier) |

```text
Use $directed-delegation to configure luna_associate from the bundled example.
Register it in my main Codex config. Do not change other agent defaults.
```

Follow the [configuration reference](skills/directed-delegation/references/configure-subagent.md) only when installation or customization is requested. It covers standalone role metadata, main-config registration, replacement, and verification. The nominal context setting is not a guarantee of the runtime's effective token window. Other models or settings can be requested explicitly.

## Repository layout

```text
codex-directed-delegation/
├── README.md
└── skills/directed-delegation/
    ├── SKILL.md
    ├── agents/openai.yaml
    ├── assets/luna-associate.toml
    └── references/
        ├── research-and-synthesis.md
        ├── evidence-and-triage.md
        ├── planned-implementation.md
        ├── batch-transformation.md
        ├── criteria-based-review.md
        ├── controlled-execution.md
        ├── selection-and-timing.md
        └── configure-subagent.md
```

## Validation

Run the validator bundled with the Codex `skill-creator` skill:

```bash
python /path/to/skill-creator/scripts/quick_validate.py \
  skills/directed-delegation
```

Parse the example TOML and UI YAML, check relative links, and review realistic assignments for trigger accuracy, scope, and usable evidence. Syntax validation does not establish behavioral quality or runtime model configuration.

## Boundaries

- The lead owns architecture, configuration choices, consequential recovery, and final acceptance.
- Delegation does not authorize unrelated changes, external actions, or recursive delegation.
- Assignments preserve concurrent edits; independent reviewers receive stable candidates and primary evidence.
- Do not treat a subagent's confident summary, successful process exit, or nominal model setting as stronger evidence than it is.
- No fixed agent count, mandatory worktree, full-history inheritance, or repeated review ceremony is imposed.

## Sources

The workflow follows [OpenAI's subagent guidance](https://learn.chatgpt.com/docs/agent-configuration/subagents) and [skill authoring guidance](https://learn.chatgpt.com/docs/build-skills), with assignment templates distilled from practical research, execution, and review workflows. These links are background references, not mandatory reading for every assignment.
