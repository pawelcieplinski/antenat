# AGENTS.md

Instructions for AI agents working in this repository. The rules under "Required workflow" apply to every task.

## Language

Write everything that lands in the repository or on GitHub in English: code, comments, documentation, specs, run logs, lessons, commit messages, branch names, pull requests, review comments and issues. Chat with the user stays in the user's language.

## Branches

Every change reaches `main` through a pull request. Commit and push only to a task branch:

- Create the branch from an up-to-date `main` before the first commit: `git switch -c <type>/<slug>`, where `<type>` is `feat`, `fix`, `docs`, `refactor` or `chore`, and `<slug>` matches the task's run log.
- If you find yourself on `main` with uncommitted changes, move them to a task branch before committing.
- Open a pull request to `main` when the task is ready for review.

## The `.ai/` directory

```
.ai/
├── specs/               # active SDD specs: YYYY-MM-DD-slug.md
│   ├── implemented/     # delivered specs
│   └── archive/         # abandoned or superseded specs
├── runs/                # task run logs: one file per task, YYYY-MM-DD-slug.md
├── lessons.md           # lesson index, one line per lesson
└── lessons/             # lesson bodies: YYYY-MM-DD-slug.md
```

`YYYY-MM-DD` is the date the file is created, `slug` is a short kebab-case description (e.g. `2026-11-09-pdf-export.md`).

## Required workflow

### At task start

1. Read `.ai/lessons.md` and open the lessons that bear on the task.
2. Check whether the task already has a run log: `grep -l "Status: in-progress" .ai/runs/*.md`. If it does (resuming, a new session, taking over from someone else), read it in full and continue in the same file, on the same branch.
3. Look for the task's spec in `.ai/specs/`. If one exists, work from it.
4. Switch to the task branch, or create it (see "Branches").

### Before every commit

- [ ] You are on a task branch, not `main`.
- [ ] The task's run log exists. On the task's first commit, create `.ai/runs/YYYY-MM-DD-slug.md` from the template below, dated the day the task started.
- [ ] A new entry (2–5 lines) describing this commit is appended at the end of the run log.
- [ ] The run log header is current: goals, spec link, status.
- [ ] The run log is staged in the same commit as the changes it describes (`git add .ai/runs/...`).
- [ ] If the commit fixes a non-obvious bug, uncovers a gotcha, or follows a correction from the user, the same commit adds a lesson.

## Specs (`.ai/specs/`)

Specs for spec-driven development. Lifecycle:

- A new spec goes to `.ai/specs/YYYY-MM-DD-slug.md`.
- Once delivered, move it to `implemented/`; if abandoned or superseded, to `archive/`. Move it with `git mv` and keep the file name.
- After moving a spec, update the link in the header of every run log that points to it.

## Run logs (`.ai/runs/`)

One file per task, appended to on every commit.

- The file name stays fixed for the whole task: the date is the day the task started. Later sessions and later days append to the same file.
- The header at the top is live: keep its goals, spec link and status current. Set `Status: done` only in the commit that completes the task.
- Entries below the header are frozen: each commit appends a new entry at the end and leaves earlier entries as they are.
- Write the entry before committing, as you go. Every commit has its own entry.

Template:

```markdown
# <Task title>

Goals:
- <goal 1>
- <goal 2>

Spec: [YYYY-MM-DD-slug](../specs/YYYY-MM-DD-slug.md)
Branch: <type>/<slug>
Status: in-progress

---

## YYYY-MM-DD
Scope: <what this commit covers>
Decisions/gotchas: <what was decided, what to watch out for>
Next: <what is left>
```

When the task has no spec, write `Spec: none`.

## Lessons (`.ai/lessons.md`, `.ai/lessons/`)

The project's long-term memory, shared by people and all agents. Record project findings here rather than in an agent's private memory, which nobody else can see.

Write a lesson when:
- you fix a bug whose cause was non-obvious,
- you hit a gotcha that the code and configuration do not reveal,
- the user corrects your approach or confirms a non-obvious decision,
- you find an improvement to the process, the tooling or these instructions.

How to write one:
1. Check `.ai/lessons.md` for a similar lesson. If there is one, update its file instead of creating a new one; delete a lesson that turned out to be wrong, together with its index line.
2. Create `.ai/lessons/YYYY-MM-DD-slug.md` with three sections: **Context** (what happened), **Lesson** (the rule to follow), **How to apply** (when and where).
3. Append a line to `.ai/lessons.md`: `- [Title](lessons/YYYY-MM-DD-slug.md) — the rule in one sentence`.
