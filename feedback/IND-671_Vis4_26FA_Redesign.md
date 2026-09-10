# IND-671 Vis 4 — 26FA Redesign
## Driven by the 25FA end-of-term whiteboard session

Third iteration of the course. 24FA → 25FA cut the database/API/Advanced Git material
after student feedback. 25FA → 26FA moves hardware earlier and rebalances toward HMI.

---

## 1. What the whiteboard said

Ordered by how many separate ways each point appeared on the board.

### Hardware lands too late — the dominant finding
Appeared five ways: ⚠️ flags either side of Week 8, "TOO LATE IN COURSE" written above
it, "(NEEDS 1 MORE WEEK)" in its own header, "ARDUINO PRIOR??" with an arrow at the
week 4/5 boundary, and "HOW TO SHIFT W11–13 EARLIER" beside Week 12.

Student notes: *"Could come sooner in the course to iterate more often."*

### No electronics baseline was assumed
- *"Felt stuck with no any background of electronic stuff"*
- *"Can include an intro to basic principles of electronic physics"*
- *"Felt like very elementary which is good starting point but could help to have maybe
  one more week of learning circuits"*
- Board list of what they wanted: soldering, voltage (EE), best practice, voltmeter,
  Fritzing
- Side panel: **"W8 — HW LACKED THE LEARN → APPLY PROCESS, NEED HOMEWORK WITH EXAMPLE"**

### Procurement was a binding constraint
- **"HW PURCHASE LEED TIME!!"**
- *"Needed more time to prepare hardware (prints, shipping...)"*
- *"Better to have a list for buying stuff. E.g. everyone start to plan things to buy in
  the earlier weeks"*

### Week 6 under-resourced
- *"Too short time for a whole app, if we want to make everything a working component"*
- *"The project can start earlier — like building components & layout along with the
  homework"*

### React Native — cut it
Class consensus: drop from the core course. Belongs in an advanced elective or as
optional reading for anyone who wants it.

### User testing was the most-loved element
- *"Love it, need to do it more"*
- *"Very useful to get initial insight from users"*
- *"So many people have different ways of thinking and understanding — their difference
  is very valuable"*
- **"DO THIS MORE IN GRADID"**

### Week 12 — highest praise and sharpest regret
Positive: *"Appreciated how many physical resources and hardware parts Jules provided"*,
*"Able to challenge myself to create a wireless product"*, *"Really helped to have
in-class soldering + hardware integration support."*

Negative: *"Focused too much on the engineering rather than HMI (my problem)"* and
*"If I realized and understood earlier, I could have done better job, a bit
disappointing."*

Both negatives are the "too late" complaint, felt personally.

### Open questions raised by students
- Should milestone assignments be standardised, or leverage M1–M3/M4 studio projects?
- SW vs HW felt isolated when described in Week 1

---

## 2. Decisions taken

| Decision | Rationale |
|---|---|
| **Drop Redux** from the core course | Already overflowed Week 4 into Week 5 in practice; state management is heavy for a two-screen control UI. Retained as optional "read more" for students interested in cleaner data management |
| **Drop React Native** | Class consensus. Moves to optional/advanced |
| **Midterm moves to Week 5** | Keeps Weeks 2–4 as one continuous software run, and clears an unbroken hardware block after it |
| **New Week 6: electronics fundamentals** | Directly answers the largest gap on the board |
| **Hardware block Weeks 6–8, uninterrupted** | Starts two weeks earlier than 25FA, and is three worked sessions rather than two reading-only ones |
| **Procurement decoupled from teaching** | Lead time was the binding constraint. Week 4 preview covers what to buy and why; the electronics week no longer has to carry that load |
| **Project prep distributed, not a week** | Students proposed this themselves: build components alongside homework from Week 2 |
| **Software and hardware testing kept separate** | Different artefacts, different questions. Software testing runs Weeks 2–5 and feeds the midterm; hardware gets its own three-round sequence |
| **One grading scheme** | Final sheet becomes the instrument; syllabus describes weighting |
| **Split parts ordering** | Common kit Week 1; project-specific parts Week 4 |
| **GitHub library rework** | Deferred to a separate task after the course is settled |

---

## 3. Weekly plan — 26FA

Fridays, Sep 18 – Dec 18. Thanksgiving takes Nov 27, so 13 teaching sessions.

| Wk | Date | Topic | Homework (due before next class) |
|---|---|---|---|
| 1 | Sep 18 | Intro, tools setup, **project brief & common kit order** | Configure tools; order common kit; identify a prior studio project to carry forward |
| 2 | Sep 25 | HTML & CSS for interface design | Build a page; **begin project UI**; first UI test on the number counter |
| 3 | Oct 2 | JavaScript basics & interactive elements | Number Adder; continue project UI; UI test |
| 4 | Oct 9 | React components + Routes · **hardware preview (30 min)** — what the second half needs, why lead time matters | Enhanced Number Adder in React; **project parts list due**; place order; **run UI test that feeds the midterm** |
| 5 | Oct 16 | **Midterm: software project presentation** | Act on midterm feedback; parts arriving |
| 6 | Oct 23 | **Electronics fundamentals** — soldering, voltage, voltmeter, breadboard, Fritzing | Solder a working circuit; document it in Fritzing |
| 7 | Oct 30 | **Arduino + IDE + WebSocket** — worked example, hands-on | Build the worked example; extend it toward your project |
| 8 | Nov 6 | **HMI concepts + applied Arduino** | HMI document v1; bi-directional comms working end-to-end |
| 9 | Nov 13 | Low-fidelity prototype; **plan HW test round 1** | Run round 1 — broad, task-based, scored against the rubric |
| 10 | Nov 20 | Review round 1 findings; high-fidelity build / circuitry process | Build toward hero experience; **run round 2** over the break |
| 11 | ~~Nov 27~~ | **Thanksgiving — no class** | — |
| 12 | Dec 4 | Review round 2; refine the weak areas | **Run round 3**; compile rubric comparison across all three |
| 13 | Dec 11 | Final build & integration | Finish prototype; HMI document final |
| 14 | Dec 18 | **Final presentations** | Submit everything |

### What changed structurally

**Midterm moves to Week 5.** Weeks 2–4 build the software project continuously, with the
project developing as homework rather than in a dedicated prep week — which is what
students proposed. Dropping Redux and React Native makes three weeks of content fit where
five used to.

**Hardware runs as an unbroken block, Weeks 6–8.** Electronics fundamentals, then Arduino
and WebSocket, then HMI and application. Nothing interrupts it. Hardware teaching begins
Week 6 rather than Week 8, and it is three worked sessions instead of two reading-only
ones.

**Procurement is decoupled from the teaching.** The Week 4 preview exists purely so
students know what they are buying and why, three weeks before the electronics week needs
it. Common kit goes out Week 1, project parts Week 4, everything arrives before Week 6.

### Note on the compression

Weeks 2–4 is three weeks of software before the midterm, where 25FA effectively had five.
The content is smaller by exactly that much — Redux and React Native are gone. And since
project work is distributed as homework from Week 2, students get three weeks of building
rather than the single dedicated prep week they called *"too short time for a whole app."*

That said, this is the tightest part of the plan. If it slips, the midterm moves to Week 6
and electronics compresses — not the reverse. The hardware block should not be the thing
that gives.

---

## 4. Grading — one scheme

### Term grade

| Component | Weight |
|---|---|
| Weekly assignments (Weeks 1–7) | 25% |
| Final project (Weeks 8–14) | 60% |
| Participation & engagement | 15% |

### Final project — the grading sheet (100 points)

| Criterion | Points |
|---|---|
| Working prototype & technical integration | 35 |
| HMI design & documentation | 30 |
| User testing & iteration evidence | 20 |
| Presentation quality, incl. target audience clarity | 15 |

HMI and testing together (50) now outweigh engineering (35). This is the direct answer
to *"focused too much on the engineering rather than HMI."*

The seven-criteria sheet used in 25FA is retired. This one sheet is the only instrument,
and the syllabus quotes it verbatim.

---

## 5. User testing

Two separate tracks. Software testing runs through the first half and feeds the midterm.
Hardware testing is its own three-round sequence in the second half. They are not the
same exercise at different scales — different artefacts, different questions.

All testing happens as homework, before the class it feeds into. Class time is for
reviewing findings and deciding what to change.

### Track 1 — software UI (Weeks 2–5)

Light, frequent tests on the number counter UI as it develops, then a fuller round in
Week 4 that feeds the Week 5 midterm presentation.

Purpose is partly to build the habit before it matters. Students learn the method on a
small artefact with no hardware to confound it.

### Track 2 — hardware prototype, three rounds

The rounds narrow progressively. Each is task-based and scored against the same rubric —
the rubric is what makes the sequence mean anything, because it is the constant that lets
round 3 be compared to round 1.

**Round 1 — broad (Week 9 homework)**
Wide, shallow coverage of the whole experience. Every major task, minimal depth. The
output is a map of where the pain is, not a solution. Score everything against the rubric
to establish a baseline.

**Round 2 — narrowing (Week 10 homework, over the break)**
Retest the areas that scored well quickly, just to confirm they held. Spend the recovered
time going deeper where round 1 showed low confidence: more steps, finer tasks, more
probing on the same interaction.

**Round 3 — targeted (Week 12 homework)**
Focus on what scored badly in rounds 1 and 2. Same tasks, same rubric, so improvement is
measurable rather than asserted.

### Deliverable

The final presentation shows the rubric scores across all three rounds. Movement between
round 1 and round 3 on the areas that started weak is the evidence of iteration — this is
what "Iteration & user testing" is scoring, not the number of tests run.

### What gets measured

**Usability** — task completion, time taken, where they hesitate, severity of each issue
on a 1–4 scale.

**Emotional response** — what they say unprompted, reaction at the moment of interaction,
whether they return to it voluntarily, what they describe to someone else afterward.

25FA named these as "functionality and enjoyability" once, in the Week 12 homework, with
no method attached. This year both are instrumented and carried across all three rounds.

---

## 6. Parts & procurement

Lead time was a binding constraint. Split into two orders.

**Common kit — ordered Week 1, everyone**
Arduino UNO R4 WiFi, breadboard, jumper wires, NeoPixel matrix and ring, buttons,
potentiometer, servo, basic soldering supplies.

**Project-specific — identified Week 4, ordered Week 5**
Depends on direction. Smaller order, shorter lead time, and by then the project is known.

This also resolves the students' own question about standardised vs studio-derived
projects: the kit is standard, the project is theirs.

### House project option — rubber band winder & counter

For students without a studio project to carry forward. A device mounted on an electric
screwdriver that counts winds, optionally automates the trigger, and releases at a set
target.

Recommended as the default because it has genuine bi-directional communication built in —
the app sets target turns, the device counts and reports back, the device signals
completion. The WebSocket requirement arises from the problem rather than being bolted on.
It also has a real user in the rubber-band-powered car class, which gives the HMI
documentation a concrete audience.

### Held back: touch-monitoring wearable

Capacitive sensing between two bodies is unreliable enough that students would spend the
term fighting the sensor instead of designing the interface. It also needs two devices
plus a phone, which triples the integration surface, and it asks students to build around
physical intimacy — not something everyone will want to opt into. Viable for one
ambitious student; risky as a house project.

---

## 7. Still open

1. **Syllabus rewrite.** Sections 3, 4, and 5 above change the weekly plan, the grading,
   and the course description. The filed syllabus must match.
2. **Weeks 2–4 compression.** Three weeks of software before the midterm where 25FA had
   five. Should hold now that Redux and React Native are gone, but it is the thinnest
   part of the plan.
3. **Week 7 worked example.** The Arduino homework needs a Number-Adder-shaped worked
   example that does not yet exist. This is the "learn → apply" fix, and it is new
   authoring rather than a port.
4. **The testing rubric.** The three-round sequence depends on one rubric applied
   consistently. It does not exist yet and needs writing before Week 9.
5. **Canvas content for Weeks 6, 9, 10, 12, 13.** No 25FA pages exist for these.
5. **GitHub library rework** — deferred, but students asked for assemblies rather than
   component demos.
