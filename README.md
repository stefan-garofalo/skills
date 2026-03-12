# skills

Shareable skills for domain-scoped multi-agent planning and execution.

This repo contains two skills:

- `domain-plan`
- `domain-execute`

It also includes one optional Codex role file:

- `extras/sparky.toml`

## What this workflow is

This skillset is built around one idea:

1. Take one broader story or domain task.
2. Decompose it into explicit child tasks with dependencies.
3. Persist that structure into a backlog and a `*-plan.md` artifact.
4. Execute only unblocked tasks in parallel.
5. Validate each task through explicit completion criteria.

In other words, this repo is not just "two prompts".
It is a small operating model for swarm-style execution.

## What each skill does

### `domain-plan`

Purpose:

- take a broader story/domain task
- research current codebase and dependencies
- invoke a dependency-aware planner
- normalize the result into an execution-ready `*-plan.md`
- add task metadata needed by workers
- sync child tasks into a backlog

Important outputs:

- explicit task IDs
- `depends_on`
- `location`
- `validation`
- `tdd_target`
- `review_mode`
- backlog item references

Practical meaning:
`domain-plan` turns a high-level story into a durable execution contract.

### `domain-execute`

Purpose:

- read an approved `*-plan.md`
- treat that plan as the source of truth
- sync exact worker briefs back into the backlog
- choose the execution path
- run dependency-aware waves of workers
- enforce TDD-first and validation rules
- keep plan and backlog state updated during execution

Practical meaning:
`domain-execute` turns the plan contract into governed swarm execution.

### `extras/sparky.toml`

Purpose:

- optional worker role for Spark-based execution
- used only when you want `spark` mode together with `$parallel-task-spark`

Practical meaning:
this file is not part of the generic workflow.
It is a Codex-specific runtime convenience.

## Agnostic vs Codex-specific

### Workflow concepts that are agnostic

These parts are portable to other agent systems:

- one parent story becomes multiple child tasks
- child tasks have explicit dependencies
- plan artifact is the execution contract
- backlog is the external source of truth
- execution proceeds in waves
- workers get bounded ownership
- validation is explicit, not inferred
- TDD target is defined before execution
- browser/runtime validation can be required per task

If you use another harness, these ideas still apply.

### Skill packaging that is Codex-specific

These parts assume Codex-style skills:

- `SKILL.md`
- `agents/openai.yaml`
- installation under `~/.agents/skills`
- optional role registration under `~/.codex/config.toml`
- optional `sparky.toml` role config

If you are not using Codex, treat these files as reference prompt specs and adapt them to your own agent framework.

### Runtime dependencies that are not specific to these two files

These skills rely on a larger environment:

- a dependency-aware planner skill
- a dependency-aware parallel executor skill
- a TDD-oriented execution discipline
- a browser/runtime validation capability
- a backlog tool or CLI
- git-aware repo context

In this repo, those dependencies are documented but not bundled.

## Required companion skills

These two skills are not standalone. They expect the following companion skills to exist in the host environment:

- `$swarm-planner`
- `$parallel-task`
- `$parallel-task-spark`
- `$tdd`
- `Agent Browser`

Without these, `domain-plan` and `domain-execute` are incomplete.

## Required local tools

Required or strongly expected:

- Codex skills support
- `opensrc`
- a backlog CLI or equivalent workflow
- git

Usually useful:

- GitHub CLI if you want repo-native finalize steps

Optional:

- `portless` for worktree-safe server validation

## Install in Codex

Copy or symlink the skill folders into `~/.agents/skills`:

```bash
mkdir -p ~/.agents/skills
cp -R skills/domain-plan ~/.agents/skills/
cp -R skills/domain-execute ~/.agents/skills/
```

If you want `spark` mode, also install the optional role file:

```bash
mkdir -p ~/.codex/agents
cp extras/sparky.toml ~/.codex/agents/
```

Then register it in `~/.codex/config.toml`:

```toml
[agents.sparky]
description = "Fast implementation worker for swarm execution"
config_file = "/ABSOLUTE/PATH/TO/.codex/agents/sparky.toml"
```

## Typical usage

Planning:

```text
Use $domain-plan to create an execution-ready domain plan and sync tasks to the chosen backlog.
```

Execution:

```text
Use $domain-execute to run an approved domain plan with the selected swarm executor.
```

## What you will likely customize

Most adopters will need to adapt:

- backlog-specific instructions
- finalize/push/review behavior
- worker role configuration
- browser/runtime validation expectations
- host-specific repo tooling

The core reusable pieces are:

- plan-first execution
- explicit dependency graph
- backlog as source of truth
- bounded task handoff
- validation-first completion rules

## Repository contents

```text
skills/
  domain-plan/
    SKILL.md
    agents/openai.yaml
  domain-execute/
    SKILL.md
    agents/openai.yaml
extras/
  sparky.toml
```

## Notes

- The prompt logic tries to stay host-agnostic where possible by deriving repo host context from git remotes.
- `spark` mode is optional and Codex-specific.
- The generic workflow is broader than Codex; the packaging in this repo is not.
