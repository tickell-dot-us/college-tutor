# Mode: drill

**Subjects:** foreign language vocabulary and conjugation; memorized formula sets; anything that is genuinely a lookup table in the head.

- **Item:** one pair — word/meaning, verb/conjugation, name/formula.
- **One rep:** correct cold recall.
- **Session size:** 30–60 items. Nothing like the other modes.

## The Socratic ladder mostly doesn't apply here

You cannot coach someone to a vocabulary word they have never seen. There's no reasoning path to a memorized arbitrary pairing, and pretending otherwise wastes their time and feels faintly ridiculous.

So in this mode the ladder collapses to: **cold prompt → if missed, supply it immediately, requeue it, move on.** Speed is the point. Dwelling on a missed item is worse than moving past it and seeing it again in ninety seconds.

This is the one place where "never give the answer" is suspended, and it's suspended because the answer carries no reasoning to be robbed of.

Where reasoning *does* exist — a conjugation that follows a rule, a formula that can be derived — coach the rule once, then drill the instances. If they miss items that follow a rule they know, that's (a): the rule isn't solid, and drilling instances won't fix it.

## Requeue within the session

A missed item comes back roughly five items later, then again near the end. This within-session requeue is separate from the 1/3/7/14 ladder, which governs across sessions. Both are running at once; don't conflate them.

## What the buckets mean here

- **(c)** — near-miss: right word wrong ending, right formula wrong constant. Worth distinguishing, because it means partial encoding rather than none.
- **(b)** — simply doesn't know it.
- **(a)** — doesn't have the underlying rule the item depends on.
- **(d)** — rarely applies here.

## Where decks live

**In the subject's domain ledger, `data/subjects/<subject-slug>/_domain.md`, never in a course ledger.** A deck belongs to the field, not to the course that happened to introduce it: a Spanish vocabulary deck is a property of Spanish, and it should follow the student from Spanish 1 into Spanish 2 with its history intact rather than being rebuilt each term.

This is also why a deck stays drillable while its course is still running. Domain items are decay-eligible immediately, which is the documented exception to the rule against reviewing active-course material — see `SKILL.md` under Course backlog.

## Keep the ledger readable

**Don't log 60 items individually.** A drill session would bury everything else in the domain ledger and make it useless to read.

Log instead: the deck name, size, date, aggregate score, and the specific persistent stragglers — items missed across two or more sessions. Those stragglers are the only ones that deserve their own row, and they're the only ones that need targeted work. Promote them to the Items table of the same domain ledger and work them there.
