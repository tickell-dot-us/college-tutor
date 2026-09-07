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
skills/course-tutor-coach/references/           — spacing research; image handling; refreshers
data/student-profile.md                         — YOU: how you learn, across every course
data/course-backlog.md                          — YOUR course tracker, and the index to everything below
data/review-schedule.md                         — YOUR scheduled refreshers: active, proposed, declined
data/subjects/<subject>/<course>.md             — one mastery/error ledger per course
data/subjects/<subject>/_domain.md              — terms, formulas and vocab decks for the whole subject
data/logs/<course>.md                           — one session history per course
data/archive/<course>.md                        — session histories of finished courses
```

### Things you memorize don't belong to one class

Vocabulary, formulas, notation, constants, named theorems: these belong to the subject, not to whichever course introduced them. They live in that subject's `_domain.md` and carry forward, so a formula you learned in intermediate algebra is still being reviewed while you're in calculus, with its history intact rather than starting over as a new entry.

They're also the one thing reviewed while the course that introduced them is still running. Re-teaching this week's homework isn't review, but drilling terms from week one during week six is, and a course with cumulative exams expects you to be doing it.

### Why it's split up like that

One file per course, rather than one file for everything, because the everything-file doesn't survive a degree. Your mastery ledger and your session history both grow every time you sit down, and a single file holding four years of both eventually gets too large to open, too slow to work with, and useless to inspect in version history. Splitting by course keeps what any one session has to load roughly constant, whether it's your first term or your last.

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

## Photograph your work

You don't have to type math into a chat box. Photograph the worksheet, screenshot the problem, send a picture of the figure.

Before it says anything about whether your work is right, it reads your work back to you in clean notation and asks you to confirm it got it right. Handwriting is ambiguous in specific ways: a fraction bar looks like a minus sign, `x2` could be `x²` or `x·2`, parentheses get implied rather than written. A tutor that misreads a sign will confidently coach you to fix a mistake you never made, so it checks first.

It answers the problem you asked about, not the other four the photo happened to catch.

## It will ask about how you study, and about your notes

Once, early on, it asks how you actually work: whether you read the section before or after lecture, whether you highlight, whether you rework the examples or read them, when you start homework. It isn't grading the answers. Those habits shape everything that happens later, and not one of them is visible in the work you bring to a session.

Then roughly once per chapter, around when that chapter's test closes, it asks to see your notes. It looks at properties rather than format, so it doesn't care whether you use Cornell or an outline or anything else. It cares whether pages are dated, how much of a page just reproduces what's already in the textbook, whether anything the instructor said out loud made it onto paper, and whether the conditions for using a formula got written down next to the formula.

It never makes notes a condition of helping you. Ask for help whenever you need it.


## One subject per session

The tutor never changes subject on its own. It won't interrupt a calculus problem to quiz you on government, even if that review is overdue — losing your working state costs more than the extra rep is worth.

**You** can switch whenever you like. When you do, it logs and commits the current subject's state first, then re-scopes.

Overdue work in other subjects reaches you three ways only: a one-line note at the end of a session, a scheduled refresher that fires as its own session, or whenever you ask what's due.

## Your data files are live, not templates

`data/student-profile.md`, `data/course-backlog.md`, and `data/review-schedule.md` are **not templates you copy** — they're the real, tracked files from the moment you create your copy of this repo. Claude reads and updates them at those exact paths. Per-course files get created as you start courses, at paths recorded in your backlog.

The two files whose names start with an underscore (`data/subjects/_course-ledger-template.md` and `data/logs/_course-log-template.md`) *are* templates. Claude copies them when a course starts. Leave them alone.

Because they're files in a git repo, their history is your history: `git log -p -- data/subjects/math-statistics/mat1033.md` shows exactly how your record in that course changed and when.

### Your work lives on your machine

The repo on your own computer is the real one. If Claude is working from a cloud session, anything it writes only counts once it's committed to that repo, and it's only backed up once you push. Claude checks it's actually connected to your repo before writing anything, reports the commit it made at the end of each session, and tells you how many commits are sitting unpushed.

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
