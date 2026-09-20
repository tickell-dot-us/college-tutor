# Course Ledger Template

**This is a template, not live data.** Copy it to `data/subjects/<subject-slug>/<course-slug>.md` when a course starts, then delete this header block from the copy. Subject slugs are the lowercased, hyphenated form of the subject registry rows in `tutor/protocol.md` (Math & Statistics becomes `math-statistics`).

One ledger per course. The ledger holds the table and nothing else: narrative belongs in `data/logs/<course-slug>.md`.

---

# <COURSE CODE> — <Course Name>

Topic ledger. Narrative history for this course lives in `data/logs/<course-slug>.md`.

Mastery scale: **New** (not yet assessed) · **Shaky** (b/d errors present, under 3 clean reps) · **Solid** (3+ consecutive correct spaced reviews) · **Maintenance** (Solid, in the long-interval hold pattern)

Error buckets: **(a)** prerequisite gap · **(b)** current-concept misunderstanding · **(c)** execution slip *(mode-specific, see the mode file)* · **(d)** novel case

Don't upgrade a mastery rating from a single correct answer; require it to hold across a session or a spaced recheck first.

**The Notes cell has a hard budget of 200 characters.** It holds a short characterization plus a pointer to the dated entry carrying the detail, like `sign-flip slip under division; see log 2026-09-03`. Full narrative goes in the log, never here.

**The budget is enforced when you write, not repaired later.** If an update would push a cell past 200 characters, the detail goes into today's log entry and the cell is rewritten as characterization plus pointer, in that same write. A cell that is allowed to grow and be cleaned up later never gets cleaned up fast enough: see the compaction protocol in `tutor/protocol.md`.

To check this file at any time, print its longest cell: `awk -F'|' '/^\|/ {s=$(NF-1); gsub(/^[ \t]+|[ \t]+$/,"",s); if (length(s)>m) m=length(s)} END {print m}' <this file>`.

A row waiting on something the student owes carries `HELD: <what is awaited>` here, inside the same budget.

| Topic (fine-grained) | Mastery | Last reviewed | Next due | Errors (a/b/c/d) | Resources tried | Notes |
|---|---|---|---|---|---|---|
| | | | | | | |
