# Install agent skills

Goals:
- Commit the `om-*` agent skills from `open-mercato/skills` so every agent working in the repository gets the same set
- Pin the installed versions in `skills-lock.json`

Spec: none
Branch: chore/install-skills
Status: done

---

## 2026-11-09
Scope: 74 skills from `open-mercato/skills` in `.agents/skills/`, `.claude/skills/` as relative symlinks to them, and `skills-lock.json` with the source and content hash of each skill.
Decisions/gotchas: `.agents/skills/` holds the only copy; Claude Code reads `.claude/skills/`, so those entries are symlinks, not duplicates. Checked that the lock file lists exactly the 74 installed directories and that every symlink resolves. Update skills through the installer so the lock hashes stay in sync with the files.
Next: run `om-setup-agent-pipeline` to write `.ai/agentic.config.json` before using the pipeline skills.
