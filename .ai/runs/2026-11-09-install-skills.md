# Install agent skills

Goals:
- Commit the `om-*` agent skills from `open-mercato/skills` so every agent working in the repository gets the same set
- Pin the installed versions in `skills-lock.json`
- Configure the agent PR pipeline with `om-setup-agent-pipeline`: config, tracker and browser descriptors, GitHub labels, `SDLC.md`

Spec: none
Branch: chore/install-skills
Status: done

---

## 2026-11-09
Scope: 74 skills from `open-mercato/skills` in `.agents/skills/`, `.claude/skills/` as relative symlinks to them, and `skills-lock.json` with the source and content hash of each skill.
Decisions/gotchas: `.agents/skills/` holds the only copy; Claude Code reads `.claude/skills/`, so those entries are symlinks, not duplicates. Checked that the lock file lists exactly the 74 installed directories and that every symlink resolves. Update skills through the installer so the lock hashes stay in sync with the files.
Next: run `om-setup-agent-pipeline` to write `.ai/agentic.config.json` before using the pipeline skills.

## 2026-11-09
Scope: `om-setup-agent-pipeline` run: `.ai/agentic.config.json` (GitHub tracker, `agent-browser`, full label taxonomy, QA gate on), `.ai/trackers/github.md` and `.ai/browsers/agent-browser.md` copied from the skill, `SDLC.md` from its template, `.ai/{plans,analysis,scripts,qa}/.gitkeep`, `.gitignore` for per-run QA state. Created 32 missing labels on GitHub (`bug` and `documentation` already existed and were left as they are). Cross-skill coverage check: `SKILL_COVERAGE_OK`.
Decisions/gotchas: `paths.runs` is `.ai/plans`, not the default `.ai/runs`, so om-* plans never collide with AGENTS.md run logs (see lesson `2026-11-09-om-plans-dir`). `validation.commands` is empty because the repo has no code yet, so the gate passes trivially. AGENTS.md was left untouched, as the skill requires. CODE_REVIEW.md and BACKWARD_COMPATIBILITY.md were deferred until there is code to derive them from.
Next: fill `validation.commands` and SDLC.md's Validation gate once the stack exists; list the new `.ai/` directories in AGENTS.md's tree.

## 2026-11-10
Scope: AGENTS.md `.ai/` tree lists the pipeline files and directories (`agentic.config.json`, `trackers/`, `browsers/`, `plans/`, `analysis/`, `scripts/`, `qa/`) and points to `SDLC.md`; states that om-* plans never go to `.ai/runs/`.
Decisions/gotchas: The rule that keeps plans out of `.ai/runs/` now lives in AGENTS.md as well as in the lesson, so agents that never open the lesson still see it.
Next: merge PR #2; fill `validation.commands` once the stack exists.
