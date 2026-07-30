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

### RF variant

A ninth tab, **ML & Controls — RF Track**, carries the same depth and the same Fall 2027 finish (load 61 vs 59)
but spends the free elective slots on wireless: **ECE 123** Antenna Systems Engineering (Spring 27, needs only
ECE 107), **ECE 161A** Digital Signal Processing, **ECE 158A** Data Networks I, and **ECE 115** Fast Prototyping.
The only structural change is moving ECE 17 into Fall 2026 to free the Spring slot.

ECE 166 Microwave Systems is deliberately absent — it requires ECE 102 → ECE 100, which puts it in Fall 2028.

## Fixed constraints built into every plan

- **PHIL 184** in summer session 2, 2026 — completes the Philosophy area study
- **ECE 65 retake** in Fall 2026 — gates ECE 100, 102, 103 and 115
- **COMM 10** in Fall 2026 — also clears the DEI requirement
- Social science area study finished with two upper-division COMM electives (COMM 20 already done)
- American History & Institutions already satisfied by high school record — no course spent on it

## Data sources

Course offerings come from the **ECE Tentative Course List 2026-27** and prerequisites from the **ECE Course
Prerequisites** page, both supplied directly. Each course row shows its real Fall/Winter/Spring availability; a
hollow outline marks a non-ECE course whose availability is assumed rather than read. A build-time validator
(`scripts/validate.mjs` equivalent, run in Chromium) asserts that every plan has 21 courses, that each declared
load matches its computed load, that each requirement checklist sums to 18, and that no course is ever scheduled
in a quarter it isn't offered.

Anything placed in Fall 2027 or later assumes next year's pattern matches this year's. Summer 2027 is TBD for
every ECE course, so only COMM, Rady and physics courses are scheduled there.

## Known limitation

Difficulty ratings (1–5) are structural judgments — lab + lecture, heavy math, cleanroom or capstone project,
lecture-only GE — **not** grade statistics. The [SunSET](https://github.com/SheepTester/ucsd-sunset) dataset lives
in a Google Sheet the build environment cannot reach (`docs.google.com` is blocked by egress policy), so no real
grade distributions are folded in yet.

Not an official record. Confirm with ECE Undergraduate Student Affairs and Warren Academic Advising.
