# Domain Ledger Template

**This is a template, not live data.** Copy it to `data/subjects/<subject-slug>/_domain.md` the first time a domain-level item is worth recording in that subject, then delete this header block from the copy.

One domain ledger per subject, holding what outlives any single course in that subject.

---

# <Subject> — Domain Ledger

Knowledge in this subject that belongs to the field rather than to a course. Course-specific competencies live in that course's ledger alongside this file; narrative lives in the course logs.

**What belongs here.** The test is not whether an item is important or whether it will come up again. It is whether the item survives its course as a thing with its own identity. A term, a definition, a formula, a notation convention, a named theorem, a physical constant, a conjugation table: each existed before the syllabus and outlives it. A competency shaped by how a course sequenced material ("solving compound inequalities," "graphing linear functions") belongs to the course ledger, and a syllabus section always does.

A quick way to settle edge cases: if the student transferred schools mid-degree, which rows would still describe something real?

**Domain items are decay-eligible immediately,** including while the course that introduced them is still active. This is the one place the "never review the active course" rule does not apply, and the reason is that memorized facts decay on a different clock than applied skills. Drilling weeks 1 through 5 vocabulary during week 6 is what spaced repetition is for; it is not a substitute for doing the current homework, and it does not become one.

**One line per row.** Same discipline as a course ledger: a short characterization plus a pointer to the dated log entry carrying the detail, in whichever course's log it happened. Narrative never goes in a cell.

Mastery scale and error buckets are the same as everywhere else. See `SKILL.md`.

## Items

Individual terms, formulas, notation, theorems, constants, rules. Also where a drill deck's persistent stragglers get promoted to rows of their own.

Kind is one of: term · formula · notation · theorem · constant · rule

| Item | Kind | First met in | Mastery | Last reviewed | Next due | Errors (a/b/c/d) | Notes |
|---|---|---|---|---|---|---|---|
| | | | | | | | |

## Decks

Aggregate rows for high-volume memorization, per `references/modes/drill.md`: never log 60 items individually. A deck gets one row; items missed across two or more sessions get promoted to the Items table above and worked there.

| Deck | Size | Last drilled | Aggregate score | Next due | Persistent stragglers |
|---|---|---|---|---|---|
| | | | | | |

## Recurring patterns

Subject-scoped patterns that are not individual knowledge items: error habits, procedural confusions, and note-taking defects specific to this field. Cross-subject patterns belong in `data/student-profile.md` instead, and anything tied to a single topic belongs in that topic's ledger row.

One line each, same discipline as everywhere else: a short characterization plus a pointer to the dated log entry where it was seen. When a pattern is superseded, rewrite its line rather than adding a second one beneath it.

<!-- - [first seen YYYY-MM-DD] short characterization of the pattern; see log YYYY-MM-DD -->
