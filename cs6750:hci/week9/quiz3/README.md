# HCI Study Notes — Chapter 5: Designing HCI Experiments

---

## 5.1 Methodology

- **Methodology** — the way an experiment is designed and carried out; includes participants, materials, tasks, order of tasks, procedure, variables, and data analysis.
- **Signal** — the variable of interest being measured (e.g., input device, interaction technique).
- **Noise** — all random influences (environment, participant mood, etc.).
- Goal of experiment design: **enhance signal, reduce noise**.
- **Factorial experiment** — experiment where participants are exposed to levels of factors (test conditions) while behavior is observed and measured.
- Key resources: APA Publication Manual, ACM CHI proceedings, David Martin's *Doing Psychology Experiments*.
- A well-structured paper follows: **Method → Participants → [rest of methodology]**.

---

## 5.2 Ethics Approval

- Required before any HCI experiment involving humans.
- Governing bodies: **IRB** (Institutional Review Board), **HRPC** (Human Participant Review Committee), **ERC** (Ethics Review Committee).
- Participants must be informed of:
    - Nature of the research
    - Research methodology
    - Any risks or benefits
    - Right to withdraw at any time without penalty
    - Right to anonymity and confidentiality
- Special attention for **vulnerable populations**: pregnant women, children, elderly.

---

## 5.3 Experiment Design Overview

- Involves defining variables, tasks, procedure, and number of participants.
- Key starting question: **"What are the experimental variables?"**
- Forces transition from broad/untestable questions → narrow/testable questions.
- A testable research question expresses the relationship between an **independent variable** and a **dependent variable**.

---

## 5.4 Independent Variables

- **Independent variable (IV)** — a circumstance or characteristic that is *manipulated or systematically controlled* to elicit a change in human response. Also called a **factor**.
- The variable is "independent" because participants cannot influence it.
- Expressed at **levels** (also called **test conditions**) — at least two levels required.
- Examples of IVs:
    - Device (mouse, trackball, stylus)
    - Feedback modality (auditory, visual, tactile)
    - Display size (large, small)
    - Age, gender, handedness (human characteristics — cannot be "manipulated" the same way)
    - Background noise, room lighting (environmental)

### Tips for IVs:
1. Always name both the IV **and** its levels explicitly.
2. Use consistent terminology throughout the paper.

### Effects with Multiple IVs:

| Independent Variables | Main Effects | 2-way | 3-way | 4-way | 5-way | Total |
|-----------------------|-------------|-------|-------|-------|-------|-------|
| 1 | 1 | — | — | — | — | 1 |
| 2 | 2 | 1 | — | — | — | 3 |
| 3 | 3 | 3 | 1 | — | — | 7 |
| 4 | 4 | 6 | 3 | 1 | — | 14 |
| 5 | 5 | 10 | 6 | 3 | 1 | 25 |

- **Main effect** — effect of a single IV on the dependent variable.
- **Interaction effect** — combined effect of two or more IVs.
- Three-way and higher interactions are extremely difficult to interpret — **best avoided**.
- Recommended: **limit IVs to 1–2, 3 at most**.

---

## 5.5 Dependent Variables

- **Dependent variable (DV)** — a *measured* human behavior; depends on what the participant does.
- Most common in HCI:
    - **Task completion time** (speed)
    - **Error rate / accuracy** (percentage correct or incorrect)
- Other DVs: throughput, gaze shifts, mouse-to-keyboard transitions, backspace presses, target re-entries.
- Any observable, measurable aspect of human behavior can be a DV — you can "roll your own."
- Must be **clearly defined** to ensure replicability.
- Name the DV separately from its units (e.g., DV = *text entry speed*, units = *words per minute*).
- Examples of creative DVs:
    - **Negative facial expressions** (frowns, confusion, head shakes) — used in mobile phone gaming study.
    - **Read text events (RTE)** — gaze shifts from keyboard to typed text.
    - **Re-focus events (RFE)** — times a participant refocuses on a key.

---

## 5.6 Other Variables

### 5.6.1 Control Variables
- **Control variable** — a circumstance that *might* influence a DV but is held *fixed* during the experiment.
- Examples: room lighting, temperature, display size, chair height, mouse cursor speed.
- More control → **higher internal validity**, but **lower external validity** (less generalizable).

### 5.6.2 Random Variables
- **Random variable** — a circumstance allowed to vary freely/randomly.
- Examples: participant height, weight, personality, gender.
- More random variables → **higher external validity**, but **lower internal validity** (more noise).

| Variable | Advantage | Disadvantage |
|----------|-----------|--------------|
| **Random** | Improves external validity | Compromises internal validity |
| **Control** | Improves internal validity | Compromises external validity |

### 5.6.3 Confounding Variables
- **Confounding variable** — any circumstance that changes *systematically* with an IV.
- Makes it impossible to determine whether the observed effect is due to the IV or the confound.
- Example: In a camera distance experiment, using different cameras for near vs. far conditions — the *camera* is a confound.
- Example: Presenting all participants with condition A, then B, then C — *practice* is a confound.
- Solutions: counterbalancing, renaming the IV to acknowledge the confound, or using a between-subjects design.

---

## 5.7 Task and Procedure

- A good task must satisfy two objectives:
    1. **Represent** — representative of real-world usage (improves external validity).
    2. **Discriminate** — can differentiate between test conditions (improves internal validity).
- Trade-off: More representative tasks → more secondary tasks → more variability → lower internal validity.
- **Performance-based task** — measures speed/accuracy (most common).
- **Knowledge-based task** — participant gains knowledge, cannot repeat same task (problematic for within-subjects designs).
- The **procedure** includes: task, instructions, demonstration, practice, and any questionnaires.

---

## 5.8 Participants

- Results apply to a population only if participants are drawn from that population.
- **Convenience sampling** — most common in HCI; compromises external validity.
- Increasing **n** (number of participants) → higher chance of statistical significance.
- Danger of too many participants: statistically significant result that has **no practical significance**.
- Danger of too few participants: **failing to detect a real effect**.
- Rule of thumb: use the same number of participants as similar published research (~12 is common).
- **Usability testing**: ~**5 participants** expose ~80% of usability problems.
- Use the term **"participants"** (not "subjects") when referring to the experiment.
- Participants typically sign a **consent form** before testing.
- Demographic questionnaires gather: age, gender, computer usage, experience.

---

## 5.9 Questionnaire Design

- **Two purposes**: (1) gather demographic/experience data, (2) solicit opinions on interfaces.
- **Closed-ended questions** — constrain responses to a set of options; easier to analyze.
- **Open-ended questions** — free response; richer data but harder to analyze.
- **Likert scale** — commonly used for opinions (e.g., 1–7 scale from Strongly Disagree to Strongly Agree).
- **NASA-TLX (Task Load Index)** — assesses perceived workload on 6 subscales:
    - Mental demand, Physical demand, Temporal demand, Performance, Effort, Frustration.
- **ISO 9241-9** — questionnaire standard for non-keyboard input devices (12 items; comfort and fatigue).
- **Ratio-scale** responses (e.g., exact age) allow mean/SD calculations; better quality than ordinal.
- **Ordinal responses** (e.g., age ranges) — lower quality; cannot compute mean or SD.
- Ensure all Likert items are consistently oriented (preferred response should always be same direction).

---

## 5.10 Within-Subjects vs. Between-Subjects

- **Within-subjects** (repeated measures) — each participant is tested on *all* levels of a factor.
- **Between-subjects** — each participant is tested on *only one* level; separate groups per condition.

| Design | Advantage | Disadvantage |
|--------|-----------|--------------|
| **Within-subjects** | Fewer participants needed; less variability from predispositions; no need to balance groups | Risk of interference between conditions |
| **Between-subjects** | No interference between conditions | Requires more participants; more variability between groups |

- **HCI tends to favor within-subjects designs** due to the three advantages above.
- Some factors *must* be between-subjects (e.g., gender, handedness).
- Some factors *must* be within-subjects (e.g., practice/block).
- **Mixed design** — one factor within-subjects, another between-subjects.

---

## 5.11 Order Effects, Counterbalancing, and Latin Squares

- **Order effect (sequence effect)** — performance changes due to order of testing conditions.
    - **Practice/learning effect** — performance improves with each condition due to accumulated practice.
    - **Fatigue effect** — performance worsens due to mental/physical fatigue.
- **Counterbalancing** — dividing participants into groups that receive conditions in different orders, to offset order effects.
- **Latin square** — an n × n table where each symbol (condition) appears exactly once in each row and column.
    - Used to assign test condition orders to participant groups.
- **Balanced Latin square** — each condition precedes and follows every other condition an *equal* number of times; only possible for even numbers of conditions.

### Latin Square Examples:

- 2×2: `AB / BA`
- 3×3: `ABC / BCA / CAB`
- 4×4 balanced: see Figure 5.8 in text

### Rule:
- Number of participants must be a **multiple of the number of conditions**.
- For odd numbers of conditions → use **all n! sequences** to achieve full balance.
- Alternative to counterbalancing: **randomize** condition order (best when tasks are brief with many repetitions).

---

## 5.12 Group Effects and Asymmetric Skill Transfer

- **Group effect** — statistically significant differences in DV means across counterbalanced groups.
- If counterbalancing works, group means should be approximately **equal**.
- **Asymmetric skill transfer** — different amounts of performance improvement depending on the order of testing (e.g., A→B is not the same as B→A).
- Occurs when one condition serves as better practice for another (e.g., simpler task first makes subsequent harder task easier).
- Solutions:
    - Use a **between-subjects design** (no cross-condition transfer possible).
    - Have participants practice conditions before data collection.
    - Acknowledge the asymmetry in the write-up.

---

## 5.13 Longitudinal Studies

- **Longitudinal study** — participants are tested over a prolonged period; *learning/skill acquisition* is the focus.
- **Amount of practice** becomes an IV (e.g., Session 1, Session 2, …, Session n).
- Used when a new technique requires time to learn before it can outperform a current technique.
- **Crossover point** — the point at which performance with a new technique surpasses performance with the current technique.
- **Cost-benefit trade-off**: Before crossover, the new technique has a performance cost; after crossover, it has a benefit.
- **Power law of learning** — performance curves in longitudinal studies often follow a power law.
- Example: LetterWise vs. multi-tap text entry — LetterWise eventually surpassed multi-tap by Session 20 (21.0 wpm vs. 15.5 wpm).

---

## 5.14 Running the Experiment

- Always conduct a **pilot test** before beginning (even a final one right before data collection).
- Experimenter greets participants, obtains **consent forms**, administers pre-questionnaire.
- Task is demonstrated; practice trials are given.
- Instruction to participants should be: perform tasks **quickly and accurately**.
- Instructions must be **identical** for all participants; avoid giving extra guidance that could bias behavior.
- Experimenter must remain **neutral** — not overly attentive or indifferent.
- Participants should not feel pressure to perform better on one condition over another.

---

## Key Terms Quick Reference

| Term | Definition |
|------|-----------|
| **Methodology** | How an experiment is designed and carried out |
| **Independent variable (IV)** | Manipulated circumstance/characteristic; also called a *factor* |
| **Dependent variable (DV)** | Measured human behavior (e.g., task time, error rate) |
| **Control variable** | Fixed circumstance to reduce noise |
| **Random variable** | Freely varying circumstance; increases generalizability |
| **Confounding variable** | Varies systematically with an IV; threatens validity |
| **Within-subjects** | Each participant tested on all conditions (repeated measures) |
| **Between-subjects** | Each participant tested on only one condition |
| **Mixed design** | One factor within-subjects, another between-subjects |
| **Counterbalancing** | Ordering conditions differently across groups to offset practice effects |
| **Latin square** | n×n table where each condition appears once per row and column |
| **Balanced Latin square** | Each condition precedes/follows every other condition equally |
| **Order/sequence effect** | Performance change due to position in test order |
| **Practice/learning effect** | Improved performance due to practice on earlier conditions |
| **Fatigue effect** | Degraded performance due to fatigue in later conditions |
| **Asymmetric skill transfer** | Different carry-over effects depending on order of conditions |
| **Longitudinal study** | Experiment testing participants over extended period; studies skill acquisition |
| **Crossover point** | Where new technique performance surpasses current technique |
| **NASA-TLX** | Task Load Index; 6-subscale workload questionnaire |
| **Likert scale** | Rating scale (e.g., 1–7) used in questionnaires |
| **Factorial experiment** | Experiment designed around levels of one or more factors |
| **Pilot test** | Preliminary test run to check procedure and timing |
| **Convenience sampling** | Recruiting from an accessible pool; reduces external validity |
| **Signal** | The variable of interest in experimental measurements |
| **Noise** | Random influences unrelated to the variable of interest |