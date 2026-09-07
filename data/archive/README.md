# Archive

Cold storage for completed courses. Nothing here is read during a normal session.

When a course moves to Completed in `data/course-backlog.md`, its log at `data/logs/<course-slug>.md` moves here as `data/archive/<course-slug>.md`. The course's ledger stays where it is, under `data/subjects/`, because its topic rows remain decay-eligible and the maintenance deck still selects from them.

Archiving is a move, not a deletion. The log stays readable, and a ledger row pointing at a dated entry still resolves once you know to look here rather than in `data/logs/`.
