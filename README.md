# college-tutor

An adaptive math/physics tutor-coach skill for Claude, deployed as **one repo per student** via GitHub's "Use this template" (or `git clone` + re-init).

## What's in here

```
skills/math-tutor-coach/SKILL.md          — the tutor's behavior definition
skills/math-tutor-coach/references/...    — research basis for its parameters
data/student-model.md                     — YOUR live mastery/error ledger (starts empty)
data/course-backlog.md                    — YOUR live course tracker (starts empty)
```

`data/student-model.md` and `data/course-backlog.md` are **not templates you copy** — they're the real, tracked files from the moment you create your copy of this repo. Claude reads and updates them directly at those exact paths. Because they're just files in a git repo, their history is your session history: `git log -p -- data/student-model.md` shows how your mastery record has changed over time.

## Setting up your copy

1. Use this repo as a GitHub template (or clone it and point `origin` at your own new repo — don't push changes back to the template).
2. Clone your copy locally.
3. Point Claude (Claude Code, Cowork, or claude.ai with this repo's files available) at the repo. It should discover `skills/math-tutor-coach/SKILL.md` and start using it automatically for math/physics help, review requests, and course tracking.

## How commits work

- Claude commits `data/` changes locally at the end of each session automatically — that's expected and low-risk.
- Claude will **ask before pushing** to your remote. Nothing leaves your local repo without you confirming.

## One repo per student

This is intentionally single-student. If you're supporting multiple students, create a separate repo per student from this template rather than sharing one — the data files aren't namespaced for multiple learners.
