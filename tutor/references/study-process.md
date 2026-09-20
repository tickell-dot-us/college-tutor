# Study process and note-taking

Note-taking and study sequencing sit upstream of everything this skill normally sees. A defect there surfaces weeks later as an error in the ledger, and nothing connects the two unless something does it deliberately. That connection is the point of this file.

Specific practices below draw on Saltzman and Coffin, *How to Survive Your College Math Class (and Take Home Something of Value)*, Department of Mathematical Sciences, Clemson University, 1998. Section numbers refer to that document. Its examples are mathematical; the process disciplines are not, and apply across subjects.

## The intake

Once per student, and again in a light form when a course starts in a subject with no history yet. Ask directly. None of this is inferable from the work the student brings.

**These are slots that fill over time, not an interview.** Ask the set once, early. After that, record any answer the moment it surfaces in ordinary conversation, which is where most of them actually surface: a student mentions in passing that they watch the lecture before opening the book, and that is the answer to question 1, given for free. Write it down then. A slot still empty at a unit boundary gets one offer to fill it, per the unit-boundary check in `tutor/protocol.md`. What does not work is waiting for a sit-down. An intake modeled as a single event is an intake that does not happen, and the observed case is a Study process section holding nothing but its comment scaffolding eleven days on, with one answer already volunteered and never recorded.

1. Do you read the section before lecture, after lecture, or not at all?
2. Do you bring the book to class?
3. When you read, one pass or several?
4. Do you highlight?
5. Do you rework examples on paper, or read through them?
6. Do you look at your notes again before the next class?
7. Do you start homework when it's assigned or when it's due?

Ask first, advise second. The answers go in `data/student-profile.md` under Study process, recorded as what the student said, never as what they should be doing.

Each question has a defensible better answer, and the tutor should be able to give the reasoning when asked rather than asserting a rule:

- **Preview before class** (§2.2). A few minutes skimming the section beforehand. The purpose isn't absorption, it's knowing what's already in the book, which is what makes it possible to stop copying it during lecture.
- **Bring the book, open to the relevant page** (§2.2). If the instructor works an example that's already in the text, a second handwritten copy buys nothing.
- **Read at least twice** (§2.1.1). First pass for main ideas. Second at a desk with paper: stop at each technical term and recall the definition, translate equations into words, fill in derivation steps the author skipped. Third pass to review.
- **Highlighting is close to worthless in a math text and can be actively harmful** (§2.1.2). Theorems and definitions are already set off typographically, so highlighting them adds nothing, and it substitutes recognition for understanding: passing over a highlighted line and acknowledging that it matters feels like review without being review.
- **Work problems without the book's hints** (§2.3). Using a similar worked example as a template is a crutch; mastery is being able to work the problem alone.
- **Notice what the instructor emphasized** (§2.4). Most instructors test what they stressed in class, so relative emphasis is information worth recording.
- **Ask early** (§2.3). Waiting for confusion to resolve itself rarely works in a subject where each week depends on the last.

## Before a new section: the prospective brief

The notes review below is retrospective. On its own it only tells a student what went wrong after it has gone wrong. When they are about to start a new section — `data/course-backlog.md`'s module schedule says when — or when they ask how to take notes for what is coming, give a short brief rather than general advice.

Keep it to a handful of lines. A brief that runs long does not get read before class.

- **Date and section number at the top of the page.** The cheapest item here and the one most often skipped. Every ledger row that points at a dated log entry depends on it; a page with no date cannot be pointed at.
- **Say what not to write.** Definitions, boxed rules and numbered procedures already in the text or on the slides do not need a second handwritten copy. Note where they live instead, and write out a step only when its order is the thing likely to be misremembered. The attention saved goes to listening.
- **Say what to listen for.** Spoken reasoning that never reaches the board, why one approach was chosen over another, and whatever the instructor visibly emphasizes. That material exists nowhere else once the lecture ends.
- **Give the conditions of application for this specific section.** Not the formulas, which the book already has, but the decision rules: given this shape of problem, which tool. This is the property most often missing from real notes, and it is what a test actually asks.
- **Tie it to their own record.** Pull the two or three recurring patterns from the course ledger and the subject's `_domain.md` that this material is most likely to trip, and say what to guard against. A brief that could have been written for anyone is generic advice with a date on it. The value here is that you know what this student actually gets wrong.
- **Recommend a layout only if a review has earned it.** A format is a means to a property (see `tutor/references/note-taking-methods.md`). Suggest one when a review has found the matching property missing more than once, not as a default.

If the student wants a reusable fillable note sheet built from this, that artifact belongs in the instance repo alongside their other study aids, never in the skill layer.

## The notes review

**Cadence: once per chapter or unit, at the boundary where its test closes.** That seam carries result propagation, model reconciliation, the compaction pass and a health check as well, all of them as one block rather than as separate errands: see `## The unit-boundary check` in `tutor/protocol.md`. Where a course has no chapter tests, use whatever boundary it has.

**Never a gate on help.** A student stuck late at night who is told to produce notes first learns that asking costs something. Ask for notes on the schedule; help whenever asked, without conditions.

A student who never shares notes and asks for help constantly is showing a real pattern, and it's worth naming once, plainly, and then leaving alone. The response is not to withhold help. It's that the coaching spine already refuses to hand over answers, and that refusal is what keeps the student doing the work.

### What the review checks

Properties, not format. The tutor never observes whether a format is being followed, only what ended up on the page, and it should never grade one. Check these:

1. **Dated and in sequence.** Undated pages can't be joined to the ledger's dated log entries, and a Notes cell pointing at "the 3.4 notes" resolves to nothing.
2. **How much is recoverable from the textbook?** (§2.2) A page that reproduces boxed definitions cost attention during lecture and returns nothing on review.
3. **Is what the instructor said but never wrote down captured?** (§2.2) Spoken asides, alternate approaches, and material not in the text are what notes uniquely hold.
4. **Are conditions of application recorded, or only forms?** Holding three equation forms with no rule for choosing among them is the common failure, and it's exactly what a test asks about. Polya's first step is identifying which underlying problem you're looking at (§4.1).
5. **Can each equation be read back as an English sentence?** (§3.1, §4.2.2)
6. **Are verbal shorthands precise, particularly about sign and quantifiers?** A summary line that drops a negative is worse than no summary line, because it will be trusted.
7. **Is highlighting doing work the page layout already did?** (§2.1.2)

Report findings rather than grading. Two or three specific observations land; a rubric score doesn't.

### Name what already works

A review that only produces defects teaches the student to stop sharing. Generative behaviors show up in almost everyone's notes occasionally: an annotation explaining why a step happened, a rule restated in their own words, related forms collected in one place for comparison. Say when you see them.

This matters for how the whole thing is framed. Most students are not missing a method. They already produce good notes intermittently, and transcription is the default that crowds it out. The goal is raising the rate of something they do, not installing a system they don't have.

## The loop

This is the part a study-skills handout can't do, and the reason this belongs in the tutor rather than in a pamphlet.

After a test, take the missed items and trace each one back: was what was needed present in the notes for that section? Record the result as evidence. "Your notes for this section hold all three forms and no rule for choosing among them, and two of the four items you missed were choose-the-form items" is a different kind of statement from "take better notes," and it's the kind that changes behavior.

The error taxonomy already carries signal about upstream process. Bucket (d), hasn't seen this shape before, is close to a direct measure of arriving at a lecture cold. If (d) errors cluster in the days right after each new section opens, that's evidence about previewing drawn from the student's own history rather than from general advice.

The prediction runs the other direction too. A shorthand that drops a sign, sitting in the notes for a topic where the ledger already records a sign-handling weakness, is a fault waiting to happen. Flag it when you see it rather than waiting for it to fire.

## Where findings go

- Cross-subject note habits: `data/student-profile.md`, under Standing patterns.
- Subject-specific note defects: that subject's `_domain.md`, under Recurring patterns.
- Intake answers: `data/student-profile.md`, under Study process.
- The narrative of a review: the course log, as an ordinary dated entry.

## Guarding against substitution

An always-available tutor lowers the cost of failing to capture something in the first place, which quietly erodes the reason to take notes at all. The counter is small and fits the existing protocol: before explaining a concept the student has notes on, ask them to check their notes first. That keeps notes load-bearing without gating help, and it's what the coaching spine already prescribes, which is to locate before lecturing.

## What this is not

- Not a format prescription, though not format-indifferent either. A format is a mechanism for producing a property: the two-column math layout forces reasoning to sit beside each step, and Cornell's cue column forces question-generation after class. So evaluate properties, and recommend a format only once a review has found the matching property missing more than once, framed as a means to that property rather than a system to adopt. Formats, per-subject fit, supporting practices, and the source list: `tutor/references/note-taking-methods.md`.
- Not an audit. A question about problem 7 doesn't license a review of the student's habits.
- Not a separate curriculum. It runs on the existing rhythm, at an existing boundary, reporting into existing files.

## Deferred

Per-mode guidance on what a good note *contains* (proof versus recall-explain versus code versus writing) is deliberately unspecified. Real reviews will say more about that than speculation would.
