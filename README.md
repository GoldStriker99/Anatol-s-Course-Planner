# Anatol's Course Planner

A single-page planner for finishing the UC San Diego **Electrical Engineering BS (EC27, Warren, catalog FA25)** as
fast as possible, with quarter-by-quarter schedules for all eight depth options and per-course progress tracking.

Open `index.html` in any browser. Checkmarks persist in `localStorage` and sync across every depth tab, so a course
you tick on one track shows as done on all of them.

## The core finding

All eight depths require **exactly 18 more major courses**, plus COMM 10 and two upper-division COMM electives —
**21 courses either way**. Depth choice cannot shorten the degree. What it changes is whether the courses *exist
when you need them*.

Once the real 2026-27 ECE schedule is applied, the eight tracks split hard. Two required depth courses —
**ECE 157A and ECE 161C — are not offered anywhere in 2026-27**, which blocks Communication Systems and
Signal & Image Processing outright.

| # | Depth | Load | Fixed | Free | Finishes | Risk |
|---|-------|------|-------|------|----------|------|
| 1 | Machine Learning & Controls | 59 | 11 | 7 | Fall 2027 | low |
| 2 | Computer System Design | 56 | 12 | 6 | Fall 2027 | medium |
| 3 | Power Engineering | 60 | 14 | 4 | Fall 2027 | medium |
| 4 | Electronic Circuits & Systems | 63 | 12 | 6 | Fall 2027 (needs a concurrency exception) | high |
| 5 | Photonics | 62 | 12 | 6 | Winter 2028 | medium |
| 6 | Electronic Devices & Materials | 64 | 13 | 5 | Spring 2028 | high |
| 7 | Signal & Image Processing | 58 | 11 | 7 | Spring 2028, only if ECE 161C returns | high |
| 8 | Communication Systems | 63 | 14 | 4 | Blocked — ECE 157A not offered | high |

Machine Learning & Controls wins because all ten of its required major courses run between Fall 2026 and
Spring 2027 — the major itself is finished by Spring, and everything after is electives you choose.

## Fixed constraints built into every plan

- **PHIL 184** in summer session 2, 2026 — completes the Philosophy area study
- **ECE 65 retake** in Fall 2026 — gates ECE 100, 102, 103 and 115
- **COMM 10** in Fall 2026 — also clears the DEI requirement
- Social science area study finished with two upper-division COMM electives (COMM 20 already done)
- American History & Institutions already satisfied by high school record — no course spent on it

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
