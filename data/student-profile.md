# Student Profile

Cross-subject observations about how this student learns. Small, always read, never course-specific.

This is the one data file loaded in every session regardless of subject, so it has to stay short. It holds patterns that travel between courses; anything that belongs to a single topic goes in that course's ledger instead, and anything that belongs to a single session goes in that course's log.

**Keep this file bounded: one line per standing pattern, 200 characters, plus a pointer.** Same discipline as a ledger row, for the same reason and more urgently, because this is the file every session in every course loads for as long as the student is in school. A short characterization and a pointer to where the pattern was named, like `reads slope and intercept off a derived equation in swapped order; see math101 log 2026-09-15`. The narrative behind a pattern goes to `data/logs/_profile-relocated.md`, which is cross-course on purpose: a standing pattern outlives the course that surfaced it, and a per-course log eventually moves into `data/archive/`.

**Soft budget for the whole file: 8 KB.** Past that, patterns need merging, not a bigger budget. When a pattern is superseded, rewrite its line rather than adding a second one beneath it. When two lines describe the same underlying habit, merge them. A profile that grows without limit defeats the point of separating it from the per-course files, and it is the one file that scales with the student rather than with the course.

---

## Standing patterns

<!-- Cross-topic, cross-subject patterns that don't fit a single ledger row —
     e.g. "strong on mechanics, weak at translating word problems into equations,"
     or "recall is fluent but mechanism questions expose gaps."
     These are the observations most worth carrying between courses.

     Notation quality belongs here too, not in a topic row: if photographed work is
     repeatedly ambiguous to transcribe, it's ambiguous to the student on the next
     line as well, and it generates real execution errors across every subject that
     uses symbols. See references/visual-input.md. -->

## Study process

<!-- Answers to the process intake in tutor/references/study-process.md,
     recorded as the student stated them, never as they should be. Update a line when the
     habit actually changes, not when the student agrees it ought to.

     Covers: reading sequence (before lecture, after, or not at all) · whether the book comes
     to class · passes per reading · highlighting · reworking examples versus reading them ·
     revisiting notes before the next class · homework timing (when assigned versus when due). -->

## Working preferences

<!-- How this student prefers to be coached, when it's stable enough to be worth
     carrying across sessions: pacing, how much scaffolding lands well, whether they
     want the concept named before or after they've worked it, session length that
     actually holds their attention. Preferences they stated, not ones inferred from
     a single session. -->

## Logistics

<!-- Timezone (confirmed, not assumed — scheduled refreshers run in UTC), and any
     standing constraint on when or how sessions happen. -->
