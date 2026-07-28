# Anatol's Course Planner

A single-page planner for finishing the UC San Diego **Electrical Engineering BS (EC27, Warren, catalog FA25)** as
fast as possible, with quarter-by-quarter schedules for all eight depth options and per-course progress tracking.

Open `index.html` in any browser. Checkmarks persist in `localStorage` and sync across every depth tab, so a course
you tick on one track shows as done on all of them.

## The core finding

All eight depths require **exactly 18 more major courses**. Picking a depth cannot shorten the degree — it only
changes how hard those 18 courses are and how badly a missing course section can delay you. Adding three GE courses
(COMM 10, one upper-division COMM elective, and one upper-division social science that also clears AHI) gives
**21 courses left** on every track, all finishing **Fall 2027**.

Depths are ranked by total difficulty load:

| # | Depth | Load | Fixed | Free | Risk |
|---|-------|------|-------|------|------|
| 1 | Computer System Design | 55 | 12 | 6 | low |
| 2 | Machine Learning & Controls | 58 | 11 | 7 | low |
| 3 | Signal & Image Processing | 60 | 11 | 7 | medium |
| 4 | Power Engineering | 60 | 14 | 4 | medium |
| 5 | Photonics | 62 | 12 | 6 | high |
| 6 | Communication Systems | 62 | 14 | 4 | high |
| 7 | Electronic Circuits & Systems | 63 | 12 | 6 | high |
| 8 | Electronic Devices & Materials | 64 | 13 | 5 | high |

## Fixed constraints built into every plan

- **PHIL 184** in summer session 2, 2026 — completes the Philosophy area study
- **ECE 65 retake** in Fall 2026 — gates ECE 100, 102, 103 and 115
- **COMM 10** in Fall 2026 — also clears the DEI requirement
- Social science area study finished with an upper-division COMM elective plus one course that
  doubles as American History & Institutions

## Known limitation

Quarter-by-quarter **course offerings are inferred**, not read live. The build environment could not reach
`ucsd.edu`, so offering patterns come from the ECE department's published degree plans, syllabi and prerequisite
pages. Prerequisites, requirement counts and unit totals are taken from the 07/28/2026 degree audit and the UCSD
catalog and are reliable; the open variable is which quarter each course actually runs. Courses flagged `verify`
in the UI are the ones where a wrong assumption costs a quarter — check them against the
[ECE tentative course list](https://www.ece.ucsd.edu/ece-tentative-course-list) and WebReg before registering.

Difficulty ratings (1–5) are structural judgments — lab + lecture, heavy math, cleanroom or capstone project,
lecture-only GE — not scraped CAPE/SET statistics, which were also unreachable.

Not an official record. Confirm with ECE Undergraduate Student Affairs and Warren Academic Advising.
