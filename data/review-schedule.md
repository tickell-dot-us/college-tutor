# Review Schedule

Live, versioned record of the scheduled refresher tasks that exist for this student.

**Why this file exists:** the scheduled tasks themselves live in the student's Claude account, not in this repo. Without a record here, a future session has no way to know a refresher already exists — or that one was already proposed and turned down — and will pitch it again. Re-pitching a declined refresher is the fastest way to make the feature feel like nagging.

Mechanics, cadence guidance, and the task prompt template: `skills/course-tutor-coach/references/scheduled-refreshers.md`.

## Active

| Subject | Task name | Cadence (local) | Cron (UTC) | Created | Notes |
|---|---|---|---|---|---|
| | | | | | |

*None yet.*

## Proposed, not yet created

| Subject | Suggested cadence | Proposed on | Blocked on |
|---|---|---|---|
| | | | |

*None yet. Nothing is proposable until a subject has decay-eligible topics in the student model, which requires actual coaching sessions to have happened.*

## Declined

| Subject | Proposed on | Declined on | Reason (if given) | Re-ask? |
|---|---|---|---|---|
| | | | | |

*Don't re-propose anything listed here unless the student raises it, or circumstances changed in a way they'd recognize as new — e.g. that subject's course finished and its material became decay-eligible for the first time.*

## Standing notes

- Cron runs in UTC; this student is America/New_York (UTC-4 summer / UTC-5 winter). Any task created during daylight time shifts an hour earlier when DST ends in November. Record both the local time intended and the UTC cron actually set, so the drift is diagnosable later.
- A firing session needs the `college-tutor` folder reachable to read the student model. If refreshers start coming back empty, check that first.
