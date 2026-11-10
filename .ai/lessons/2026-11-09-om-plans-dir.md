# Keep om-* execution plans out of `.ai/runs`

## Context

`om-setup-agent-pipeline` defaults `paths.runs` to `.ai/runs`. The `om-*` skills write their execution plans there as `<date>-<slug>.md` files or `<date>-<slug>/PLAN.md` folders, and `om-ai-context-maintenance` packs old run folders and loose plan files into a `.tgz` archive. In this repository `.ai/runs/` already holds the task run logs from `AGENTS.md`, under the same `YYYY-MM-DD-slug.md` naming. Sharing the directory would let a plan overwrite the run log for the same task, and rotation would archive run logs whose entries `AGENTS.md` keeps frozen in place.

## Lesson

`paths.runs` in `.ai/agentic.config.json` points to `.ai/plans`. Run logs stay in `.ai/runs/` and follow `AGENTS.md`. Plans and archives from the `om-*` skills go to `.ai/plans/`.

## How to apply

- When re-running `om-setup-agent-pipeline` or `om-apply-upgrade-notes`, keep `paths.runs` set to `.ai/plans`.
- Run `om-ai-context-maintenance` only against `.ai/plans/`, never against `.ai/runs/`.
- A task driven by an `om-*` skill still needs its run log in `.ai/runs/`. The plan does not replace it.
