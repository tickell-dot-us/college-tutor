# Course Log Template

**This is a template, not live data.** Copy it to `data/logs/<course-slug>.md` when a course starts, then delete this header block from the copy.

One log per course, append-only, most recent entry first. This is where narrative lives: what happened in a session, what the student said, how a miss actually went. The ledger at `data/subjects/<subject-slug>/<course-slug>.md` points here by date.

---

# <COURSE CODE> — Session Log

Append-only, most recent first. Ledger: `data/subjects/<subject-slug>/<course-slug>.md`.

**Entry discipline.** One entry per session, headed by its date. Keep an entry to roughly a paragraph or two: what was worked, what was missed and how it was classified, what changed in the ledger as a result. An entry is a record of a session, not a transcript of it. If an entry is running long, the excess usually belongs in the ledger as a mastery change or in `data/student-profile.md` as a standing pattern.

Never read this whole file in a session. Read the most recent few entries, or search it by date when a ledger row points at one.

**Structural output does not belong here.** Narrative displaced from ledger cells by a compaction pass goes to `data/logs/<course-slug>-relocated.md`, not into this file. This log answers what happened recently, and a housekeeping block of tens of kilobytes sitting at the top of it defeats that. Where a log already contains inline structural entries, they do not count toward the most recent few: skip past them to the most recent entry that records an actual session, and head each one with a skip-past note.

<!-- Add new entries at the top of this section, oldest at the bottom.

**YYYY-MM-DD — short title.** What was worked, what was missed, how it was
classified, what changed in the ledger.
-->
