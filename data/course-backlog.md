# Course Backlog

Live, versioned file for the course-tutor-coach skill. Tracks courses taken / in progress / planned so review sessions know what's eligible for decay, and so prerequisite-mapping can flag high-value catches.

**The Subject column is load-bearing.** It routes each course to a section of `data/student-model.md` and to a default practice mode, and it's what lets a refresher stay scoped to one subject. Every row needs one.

Seeded 2026-08-23 from prior planning research in the "Get a Degree" Claude project (`daytona-state-uf-cs-math-physics-pathway.md`, `florida-online-cs-degree-comparison.md`) — not from any tutoring session. The sequence reflects the Daytona State → UF (target) pathway as of that research; FSU and UNF remain live alternatives, which is why some rows are marked conditional.

## Completed (decay-eligible)

| Course | Subject | Completed | Key topics |
|---|---|---|---|
| | | | |

*None yet. The PERT placement test (Reading 140 / Writing 133 / Math 121) set the starting point at MAT1033, but a placement score is an aggregate, not per-topic mastery evidence — it deliberately produces no rows in the student model.*

## In progress (not decay-eligible — active material, not maintenance material)

| Course | Subject | Started | Key topics |
|---|---|---|---|
| MAT1033 — Intermediate Algebra | Math & Statistics | Fall 2026 Session A — begins 2026-08-24 (Daytona State, 7-wk compressed) | Not yet session-tracked. A topic-by-topic map exists as a separate artifact from the planning project (Miller/O'Neill/Hyde *Intermediate Algebra* 5e chapters cross-referenced to Khan Academy FL B.E.S.T. Algebra 1/2) — pull topic names from there as they come up rather than duplicating the map here. |
| POS2041 — American Federal Government | Social Science & History | Fall 2026 Session B — begins 2026-10-19 (7-wk compressed) | Not yet session-tracked. First non-STEM course in the plan and the first real exercise of recall-explain mode. Gen-ed, not part of the 14-course CS pathway. |

## Planned (used for prerequisite-weighting in review sessions)

| Course | Subject | Target term | Prerequisite topics to prioritize |
|---|---|---|---|
| MAC1105 — College Algebra | Math & Statistics | Fall 2026 Session B | MAT1033 content, once assessed |
| MAC1114 — College Trigonometry | Math & Statistics | Spring 2027 (pacing checkpoint — may split from MAC1140 rather than pair; see pathway doc) | MAC1105 |
| MAC1140 — Pre-Calculus Algebra | Math & Statistics | Spring 2027 (same checkpoint) | MAC1105 |
| MAC2311C — Calculus I & Lab | Math & Statistics | Summer 2027 | MAC1114, MAC1140 |
| MAC2312C — Calculus II & Lab | Math & Statistics | Fall 2027 | MAC2311C |
| MAC2313C — Calculus III & Lab | Math & Statistics | Spring 2028 | MAC2312C — **UF-only**; not required by FSU or UNF |
| PHY2048C — Physics with Calculus I & Lab | Physics | Fall 2027 | MAC2311C (prereq/coreq) |
| PHY2049C — Physics with Calculus II & Lab | Physics | Spring 2028 | PHY2048C, MAC2312C (prereq/coreq) |
| COP1000 — Principles of Computer Programming | Computer Science | Summer 2027 | None |
| COP2220 / COP2800 / COP2360 — C / Java / C# | Computer Science | TBD | COP1000 |
| COT3100 — Discrete Computational Analysis | Discrete Math & Proofs | Fall 2028 | MAC1105 — **UF/UNF-only**; FSU requires two separate courses (MAD2104 + MAD3105) instead |
| COP3530 — Data Structures | Computer Science | Spring 2029 | COT3100 + a language course |
| MAS3105 — Linear Algebra | Math & Statistics | Spring 2029 | MAC2312C — **UF/UNF-only**; not in FSU's published math core. DSC catalog listing vs. actual section availability was unresolved as of the source research (2026-08-22) |
| ENC course (ENC3246 / ENC2210 / ENC2256) | Writing & Composition | TBD | None — UF requires one; not yet scheduled |
| STA3032 — Engineering Statistics | Math & Statistics | TBD (post-transfer at UF) | None published |
| Foreign language, 2000 level | Foreign Language | Only if FSU becomes the target | **Conditional** — FSU requires it and can't deliver it via distance learning; UF and UNF don't require it |

---

Courses marked UF-only, UF/UNF-only, or conditional depend on which university ends up the transfer target. The full decision table is in the "Get a Degree" project's `daytona-state-uf-cs-math-physics-pathway.md`. Re-check this backlog if that decision changes — several rows drop out entirely under FSU, and one (foreign language) only appears under FSU.
