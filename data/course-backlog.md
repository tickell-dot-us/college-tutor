# Course Backlog

Live, versioned file for the course-tutor-coach skill. Tracks courses taken / in progress / planned so review sessions know what's eligible for decay, and so prerequisite-mapping can flag high-value catches.

**This file is also the index.** Every course's ledger and log live at paths named in its row, so finding a course's data never requires guessing or searching the tree. A course with no ledger yet is a course no work has happened in.

**The Subject column is load-bearing.** It routes each course to a subject directory under `data/subjects/` and to a default practice mode, and it's what lets a refresher stay scoped to one subject. Every row needs one — pick from: Math & Statistics, Physics, Discrete Math & Proofs, Computer Science, Social Science & History, Writing & Composition, Foreign Language (add a new one in `tutor/protocol.md`'s subject registry if none fit).

Paths follow one convention, so they're predictable: subject slug is the lowercased hyphenated subject name (Math & Statistics becomes `math-statistics`), course slug is the lowercased course code (MATH101 becomes `math101`).

- Ledger: `data/subjects/<subject-slug>/<course-slug>.md`
- Log: `data/logs/<course-slug>.md`, moving to `data/archive/<course-slug>.md` once the course is completed

One file per subject sits alongside those and isn't indexed here, because it isn't tied to any course: `data/subjects/<subject-slug>/_domain.md` holds the terms, formulas, notation, and drill decks belonging to the field itself. It outlives every row in this file.

## Completed (decay-eligible)

Topic rows in a completed course's ledger stay live for the maintenance deck. Only its log moves to `data/archive/`.

| Course | Subject | Completed | Ledger | Log (archived) | Key topics |
|---|---|---|---|---|---|
| | | | | | |

## In progress (not decay-eligible — active material, not maintenance material)

| Course | Subject | Started | Ledger | Log | Key topics |
|---|---|---|---|---|---|
| | | | | | |

## Planned (used for prerequisite-weighting in review sessions)

No ledger or log until work actually starts in the course.

| Course | Subject | Target term | Prerequisite topics to prioritize |
|---|---|---|---|
| | | | |
