# AI workspace setup

Goals:
- Add `AGENTS.md` and `CLAUDE.md` with the rules agents must follow
- Create `.ai/` with `specs/` (plus `implemented/`, `archive/`), `runs/`, `lessons.md` and `lessons/`
- Require English for everything in the repository and on GitHub, and pull requests for every change to `main`
- Add planning, verification and lesson-promotion rules adapted from Boris Cherny's Claude Code tips

Spec: none
Branch: chore/ai-workspace
Status: done

---

## 2026-11-09
Scope: AGENTS.md (language, branches, `.ai/` layout, required workflow, specs, run logs, lessons), CLAUDE.md importing it, `.ai/` tree with `.gitkeep` files, empty lesson index.
Decisions/gotchas: CLAUDE.md imports AGENTS.md via `@AGENTS.md` so the rules have one source. The repo was empty, so `main` got one empty bootstrap commit to give the PR a base; this is the only direct commit on `main`.
Next: enable branch protection on `main` in GitHub settings.

## 2026-11-09
Scope: AGENTS.md gains plan-first step for complex tasks, a Verification section (plus checklist item), Working practices (subagents, worktrees, skills) and lesson promotion; CLAUDE.md summary updated.
Decisions/gotchas: Source: ykdojo.github.io/claude-code-tips (Boris Cherny's 10 tips); tips 7, 9, 10 skipped as personal setup. The article has no explicit verification tip, so Verification draws on tips 5 and 6.
Next: merge PR #1, enable branch protection on `main`.
