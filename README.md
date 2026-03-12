# skills

Shareable Codex skills for domain-scoped multi-agent planning and execution.

## Included

- `skills/domain-plan`
- `skills/domain-execute`
- `extras/sparky.toml` for optional `spark` execution mode

## What these skills do

`domain-plan` turns one broader story or domain task into an execution-ready `*-plan.md` artifact and syncs its child tasks into a backlog.

`domain-execute` treats that plan as the source of truth and executes it through dependency-aware swarm workers.

These skills assume:

- backlog-driven work
- explicit task dependencies
- plan-first execution
- TDD-first worker briefs
- optional browser/runtime validation

## Required companion skills

These two skills are not standalone. They depend on:

- `$swarm-planner`
- `$parallel-task`
- `$parallel-task-spark`
- `$tdd`
- `Agent Browser`

## Required local tools

- Codex skills support
- `opensrc`
- a backlog CLI or workflow you can target
- git + GitHub CLI if you want repo-native finalize steps

Optional:

- `portless` for worktree-safe server validation

## Install

Copy or symlink the skill folders into `~/.agents/skills`:

```bash
mkdir -p ~/.agents/skills
cp -R skills/domain-plan ~/.agents/skills/
cp -R skills/domain-execute ~/.agents/skills/
```

If you want `spark` mode, also register the optional role:

```bash
mkdir -p ~/.codex/agents
cp extras/sparky.toml ~/.codex/agents/
```

Then add the role to `~/.codex/config.toml`:

```toml
[agents.sparky]
description = "Fast implementation worker for swarm execution"
config_file = "/ABSOLUTE/PATH/TO/.codex/agents/sparky.toml"
```

## Usage

Planning:

```text
Use $domain-plan to create an execution-ready domain plan and sync tasks to the chosen backlog.
```

Execution:

```text
Use $domain-execute to run an approved domain plan with the selected swarm executor.
```

## Notes

- The skills are host-agnostic at the prompt level, but they assume your environment can derive repo host context from git remotes.
- `spark` mode requires the `sparky` role and `$parallel-task-spark`.
- You will likely want to adapt backlog-specific instructions to your own toolchain.
