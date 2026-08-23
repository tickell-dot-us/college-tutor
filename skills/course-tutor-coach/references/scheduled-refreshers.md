# Scheduled refreshers: mechanics

Read this before creating, changing, or removing any scheduled refresher.

A refresher is a recurring task that starts its own fresh session, reads this repo's student model, and surfaces whatever review is due in one subject. It is the out-of-band channel that makes the no-interruption rule in SKILL.md workable — other subjects don't need to interrupt a session because they have their own way of reaching the student.

## Use the right scheduling tool

Create these with the **remote scheduled-task tools** (`create_trigger`, and `list_triggers` / `update_trigger` / `delete_trigger` for maintenance).

**Do not use `CronCreate`** if it appears in the tool list. It runs an in-process scheduler that lives inside the current session, so anything scheduled with it disappears when the session ends — and it fails silently. The student would believe they had a standing weekly refresher and simply never hear from it again. This is the single most damaging mistake available in this file.

If neither tool family is present in the current environment, don't improvise. Tell the student the cadence you'd recommend and what the task should say, note that this surface can't create it, and record it under "Proposed" in `data/review-schedule.md` so it can be created from a session that can.

## Always ask first

A scheduled task is persistent configuration that outlives the session and will act without the student present. Propose it, state the cadence and time, and wait for a clear yes. Never create one as a side effect of a tutoring session.

Set `initiation` to `human_request` when they asked or approved.

## Cadence

- **One task per subject.** This is what keeps every firing subject-scoped.
- **Weekly** is the sane default for a subject in maintenance.
- **Twice weekly** for a subject with active Shaky items, where the 1- and 3-day rungs of the ladder are still in play.
- Never schedule a refresher for the course the student is currently taking — that's active material, not decay-eligible.

Don't try to encode the 1/3/7/14 ladder in the schedule itself. The task is a heartbeat; the student model decides what actually gets served on any given firing. That way a missed week self-corrects instead of desynchronizing the whole ladder.

## The UTC / DST trap

Cron expressions are evaluated in **UTC**. This student is in America/New_York, which is UTC-4 in summer and UTC-5 in winter.

So 9:00am Tuesday Eastern is `0 13 * * 2` during daylight time — and that same expression fires at **8:00am** Eastern once DST ends in early November. It drifts the other way in spring.

Convert using the offset in effect *at creation*, tell the student the task will shift by an hour at the DST boundary, and offer to adjust it then. Picking a mid-morning or mid-afternoon time rather than something adjacent to their schedule makes the drift harmless.

## Stage the review; don't conduct it

A firing session starts with no one necessarily present, and tutoring is inherently interactive. A refresher that tries to run a full Socratic session into an empty room produces nothing useful.

The task's job is to **prepare and surface**: read the model, select what's due in its subject, say how many items and what topics, and stop there ready to begin. The student engages when they see it. Write the task prompt accordingly.

## Prompt template

Each firing starts a **fresh session with no memory of this conversation**, so the prompt has to stand completely alone:

> Open the college-tutor repo and read `skills/course-tutor-coach/SKILL.md`, then `data/student-model.md` and `data/course-backlog.md`.
>
> Run a maintenance-deck check for **<SUBJECT> only**. Do not include topics from any other subject, and do not switch subjects.
>
> Select what is due per the spacing ladder, lowest mastery first, weighting topics that are prerequisites for the student's current or next course. Then post a short summary: how many items are due, which topics, and how long it should take. Stop there and wait — don't run the session unprompted.
>
> If nothing is due in <SUBJECT>, say so in one line and stop. If the repo isn't reachable, say that instead of guessing at what's due.

Name tasks `Refresher — <Subject>` so `list_triggers` stays readable and duplicates are obvious at a glance.

## The most likely real failure

**The fired session can't reach the repo.** It starts fresh, and if the `college-tutor` folder isn't connected in that session it has no student model to read. It will not error usefully — it'll just be an agent with no data.

That's why the template ends with an explicit instruction to say so rather than improvise. Warn the student about this when proposing the first refresher: the task depends on the repo being available wherever it fires, and if refreshers start coming back empty, this is the first thing to check.

## Record every outcome

Update `data/review-schedule.md` when a task is created, changed, removed — **and when the student declines one.** The tasks live outside the repo, so this file is the only memory that a proposal was already made. Without it you'll re-pitch a refresher they turned down two weeks ago, which is the fastest way to make the whole feature feel like nagging.
