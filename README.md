# college-tutor

An adaptive tutor-coach skill for Claude that covers **every course a student takes**, not just one subject — deployed as **one repo per student** via GitHub's "Use this template" (or `git clone` + re-init).

## What it does

Three things, sharing one set of data files:

1. **Coaches Socratically** — walks the student through problems, proofs, code, essays, and recall questions step by step without ever solving, writing, or answering them outright.
2. **Remembers them** — keeps a persistent per-subject record of what they've mastered and how they tend to get things wrong, so the tutor gets more useful over months rather than starting cold each session.
3. **Fights decay** — runs spaced review on finished coursework, and proposes scheduled refresher tasks so old material resurfaces on its own instead of quietly rotting while a new course takes attention.

## What's in here

```
skills/course-tutor-coach/SKILL.md              — the shared coaching protocol and subject registry
skills/course-tutor-coach/references/modes/     — six practice modes (see below)
skills/course-tutor-coach/references/           — spacing research basis; scheduled-refresher mechanics
data/student-model.md                           — YOUR live mastery/error ledger, partitioned by subject
data/course-backlog.md                          — YOUR live course tracker
data/review-schedule.md                         — YOUR scheduled refreshers: active, proposed, declined
```

### The six practice modes

One interaction protocol runs across every subject. What changes per mode is what counts as a problem, what counts as one rep, what a mechanical slip looks like, how long a session should be, and the specific way "doing it for them" tends to happen there.

| Mode | For |
|---|---|
| `problem-solve` | Math, physics, statistics — items with a determinate answer |
| `proof` | Discrete math, linear algebra — establishing that something must be true |
| `code` | Programming — writing, debugging, explaining |
| `recall-explain` | History, government, social science — and conceptual questions anywhere |
| `writing` | Composition — essays and arguments |
| `drill` | Vocabulary, conjugation, memorized formula sets |

## One subject per session

The tutor never changes subject on its own. It won't interrupt a calculus problem to quiz you on government, even if that review is overdue — losing your working state costs more than the extra rep is worth.

**You** can switch whenever you like. When you do, it logs and commits the current subject's state first, then re-scopes.

Overdue work in other subjects reaches you three ways only: a one-line note at the end of a session, a scheduled refresher that fires as its own session, or whenever you ask what's due.

## Your data files are live, not templates

`data/student-model.md`, `data/course-backlog.md`, and `data/review-schedule.md` are **not templates you copy** — they're the real, tracked files from the moment you create your copy of this repo. Claude reads and updates them at those exact paths.

Because they're files in a git repo, their history is your history: `git log -p -- data/student-model.md` shows exactly how your record changed and when.

## Setting up your copy

1. Use this repo as a GitHub template (or clone it and point `origin` at your own new repo — don't push changes back to the template).
2. Clone your copy locally.
3. Point Claude at the repo. It should discover `skills/course-tutor-coach/SKILL.md` and start using it automatically for homework help in any subject, review requests, and course tracking.

## How commits work

- Claude commits `data/` changes locally at the end of each session automatically — expected and low-risk.
- Claude **asks before pushing** to your remote. Nothing leaves your local repo without you confirming.
- Claude **asks before creating a scheduled refresher.** Those are persistent tasks that run without you present, so each one gets explicit agreement, and declines are recorded so you don't get asked twice.

## One repo per student

Intentionally single-student. If you're supporting more than one, create a separate repo per student from this template rather than sharing one — the data files aren't namespaced for multiple learners.
