---

# 3.6

# Human-Computer Interaction: An Empirical Research Perspective
**Author:** I. Scott MacKenzie  
**Chapter 5:** Designing HCI Experiments

---

# Chapter 5 — Designing HCI Experiments

## 5.1 What Methodology?

### Key Concept: Signal vs. Noise
- Observations = **Signal** + **Noise**
- **Signal** → the variable of interest (input device, feedback mode, interaction technique)
- **Noise** → everything else (temperature, lighting, wobbly chair, participant variability)
- Goal of experiment design: **enhance signal, reduce noise**

### Methodology Defined
- Includes: participants, materials/apparatus, tasks, order of tasks, briefing procedure, variables, data collection/analysis
- Allen Newell: *"Science is method. Everything else is commentary."*
- **Factorial experiments** — participants exposed to levels of factors (test conditions) while behavior is observed and measured
- HCI methodology is largely drawn from **experimental psychology**

### Key Resources
- *APA Publication Manual* (6th ed.) — used by 1,000+ journals; covers naming variables, recruiting participants, reporting statistics
- Journals following APA: **TOCHI** (ACM), **Human-Computer Interaction** (Taylor & Francis)
- *Doing Psychology Experiments* — David Martin (6th ed.)
- ACM SIGCHI CHI proceedings — look for papers with **Method → Participants** subsection structure

---

## 5.2 Ethics Approval

> Ethics approval is required **before** any HCI experiment involving humans begins.

### Governing Bodies
- Human Participant Review Committee (HRPC)
- Institutional Review Board (IRB)
- Ethics Review Committee (ERC)

### Participants Must Be Informed Of:
- Nature of the research (hypotheses, goals)
- Research methodology
- Any risks or benefits
- Right to withdraw at any time without prejudice
- Right to anonymity and confidentiality

### Special Attention
- Vulnerable participants: pregnant women, children, elderly
- Balance: **risks to participants** vs. **benefits to society**

---

## 5.3 Experiment Design

### Starting Point
> *"What are the experimental variables?"*

- Forces transition from broad/untestable questions → narrow/testable questions
- E.g., "Is my idea good?" → "Can a task be done more quickly with my new interface?"
- Two most important variables: **independent** and **dependent**

---

## 5.4 Independent Variables

### Definition
> An **independent variable (IV)** is a circumstance or characteristic that is manipulated or systematically controlled to elicit a change in a human response.

- Also called a **factor**
- Has at least **two levels** (test conditions)
- Independent of participant behavior — participants cannot influence it

### Types of Independent Variables
| Type | Examples |
|------|----------|
| Interface/apparatus | Device (mouse, trackball, stylus), display size, feedback modality |
| Human characteristics | Age, gender, handedness, expertise, first language |
| Environmental | Background noise, room lighting, vibration level |

> Note: Human characteristics like gender are **naturally occurring** — they cannot be "manipulated" the same way interface attributes can.

### Tips for IVs
1. **Name the IV AND its levels** (e.g., IV: *feedback modality*; levels: *audio, tactile*)
2. **Use consistent terminology** throughout — switching terms (e.g., "interaction stance" → "interaction position") confuses readers

### Number of IVs — Effects Table
| IVs | Main Effects | 2-way | 3-way | 4-way | 5-way | **Total** |
|-----|-------------|-------|-------|-------|-------|-----------|
| 1   | 1           | —     | —     | —     | —     | 1         |
| 2   | 2           | 1     | —     | —     | —     | 3         |
| 3   | 3           | 3     | 1     | —     | —     | 7         |
| 4   | 4           | 6     | 3     | 1     | —     | 14        |
| 5   | 5           | 10    | 6     | 3     | 1     | 25        |

> **Rule of thumb:** Limit IVs to **1–2, maximum 3**. Three-way+ interaction effects are extremely difficult to interpret.

---

## 5.5 Dependent Variables

### Definition
> A **dependent variable (DV)** is a measured human behavior — it depends on what the participant does.

### Most Common DVs in HCI
- **Speed** → task completion time (seconds/milliseconds)
- **Accuracy** → error rate, percentage correct/incorrect
- **Throughput** → bits per second (Fitts' law paradigms)
- **Text entry speed** → words per minute

### Other DVs
- Preparation time, action time, gaze shifts, mouse-to-keyboard transitions, key presses, retries
- **Novel DVs are valid** — any observable, measurable behavior that differentiates test conditions qualifies
    - e.g., *Negative facial expressions* (Duh et al., 2008) — frowns, confusion, frustration counted from video
    - e.g., *Read Text Events (RTE)* — gaze shifts from keyboard to typed text (Majaranta et al., 2006)

### Tips for DVs
- Name the variable separately from its units (e.g., DV: *text entry speed*; unit: *words per minute*)
- Design experimental software to collect data automatically via timestamps/key presses
- **Pilot test** data collection to ensure format is correct for follow-up analysis
- Include participant codes and condition codes in filenames/data columns

---

## 5.6 Other Variables

### 5.6.1 Control Variables
- Circumstances that **might** affect the DV but are **not under investigation**
- Fixed at a nominal setting to prevent interference
- Examples: room lighting, temperature, background noise, mouse cursor speed, chair height
- **Trade-off:** More control → higher **internal validity**, lower **external validity**

### 5.6.2 Random Variables
- Circumstances allowed to **vary freely** (not controlled)
- Typically participant characteristics: height, weight, hand size, gender, IQ, social disposition
- **Trade-off:** More random → higher **external validity**, lower **internal validity**

### Random vs. Control Variables Summary
| Variable | Advantage | Disadvantage |
|----------|-----------|--------------|
| Random | ↑ External validity (generalizable) | ↑ Variability → ↓ internal validity |
| Control | ↑ Internal validity (less noise) | ↓ External validity (less generalizable) |

### 5.6.3 Confounding Variables
> A **confounding variable** changes **systematically** with an independent variable.

- Problematic: is the effect due to the IV or the confound?
- Must be **eliminated, adjusted for, or acknowledged**

#### Examples of Confounds:
- **Eye tracker experiment:** Camera distance (near vs. far) uses different cameras (A vs. B) → camera is confounded with distance
- **Fitts' law:** Using A and ID as IVs → target width W decreases as ID increases → W is a confound
- **Interaction technique order:** Testing A → B → C in fixed order → practice is a confound
- **Search engine comparison:** Google (experienced) vs. new interface (no experience) → prior experience is a confound
- **Qwerty vs. new layout:** Users familiar with Qwerty only → solution: use a **longitudinal design**

---

## 5.7 Task and Procedure

### Two Objectives of a Good Task
1. **Represent** — mirrors actual/expected usage → improves external validity
2. **Discriminate** — exposes differences between test conditions → improves internal validity

> There is a **trade-off**: more representative tasks introduce secondary behaviors that reduce internal validity.

### Task Design Considerations
- Exclude behaviors common to all conditions (e.g., if capitalization is the same across techniques, exclude it)
- **Performance/skill-based tasks** — most common; participants repeat the task
- **Knowledge-based tasks** — participant learns the answer; must change task between conditions in within-subjects designs
    - e.g., "Find birth date of Einstein" → "Find birth date of Shakespeare"

### Procedure Includes:
- Task instructions
- Demonstration / practice
- Questionnaires (pre or post)

> Instructions must be given **consistently** to all participants. Avoid additional explanations that might motivate differential behavior.

---

## 5.8 Participants

### Two Requirements to Generalize Results:
1. Participants must be from the **same population** as those results are applied to
2. A **sufficient number** must be tested (affects statistical significance)

### How Many Participants?
> Use the **same number as similar published research** (Martin, 2004)

- Too many: may achieve statistical significance for trivially small, practically meaningless differences
- Too few: may miss real effects (insufficient power)
- **A priori power analysis** is rarely done in HCI (requires knowing variance in advance)
- **Usability evaluations** (not factorial experiments): ~**5 participants** exposes ~80% of usability problems (Lewis, 1994; Nielsen, 1994)

### Recruitment
- Ideally random sampling; in practice, **convenience sampling** is typical
- Convenience sampling → narrows true population → compromises external validity
- Screening criteria should be stated in the Participants section
- **Consent forms** required: voluntary participation, no harm, right to withdraw, confidentiality

### Terminology
- Use **"participants"** when referring to the experiment specifically
- Use **"users"** for general conclusions

---

## 5.9 Questionnaire Design

### Two Purposes:
1. Gather **demographics** (age, gender) and technology experience
2. Solicit **opinions** on devices/interaction techniques

### Question Types
| Type | Description | Use |
|------|-------------|-----|
| Closed-ended | Fixed response options | Easy to tally, analyze |
| Open-ended | Free text | Richer data, harder to analyze |
| Ratio-scale | Numeric (e.g., exact age) | Enables mean, SD, correlations |
| Ordinal | Categories (e.g., age ranges) | Good for large samples; no mean/SD |

### Common Rating Instruments
- **Likert scale** — e.g., 1 (Strongly disagree) to 7 (Strongly agree)
- **NASA-TLX** — assesses perceived workload on 6 subscales: mental demand, physical demand, temporal demand, performance, effort, frustration
- **ISO 9241-9** — 12-item questionnaire for comfort/fatigue with non-keyboard input devices

> ⚠️ Ensure all items are **consistently constructed** (preferred response always at same end of scale) before computing means across items.

---

## 5.10 Within-Subjects and Between-Subjects

### Definitions
| Design | Description |
|--------|-------------|
| **Within-subjects** (repeated measures) | Each participant tested on **all** levels of a factor |
| **Between-subjects** | Each participant tested on **only one** level; separate group per level |

### Choosing the Design

**Must be between-subjects when:**
- Factor is an immutable human characteristic (gender, handedness)

**Must be within-subjects when:**
- Factor is practice/learning (skill acquired within a person)

**When there's a choice — compare trade-offs:**

| | Within-Subjects | Between-Subjects |
|-|----------------|-----------------|
| Participants needed | Fewer | More |
| Testing per participant | More | Less |
| Participant variability | Consistent across conditions | More variability between groups |
| Group balancing | Not needed (one group) | Required |
| Interference risk | Higher | None |

> HCI experiments **tend to favor within-subjects** designs due to fewer participants needed and consistent variance.

**Mixed design** — one factor within-subjects, another between-subjects  
e.g., Block (within) × Handedness (between)

---

## 5.11 Order Effects, Counterbalancing, and Latin Squares

### Order Effects
- **Practice/learning effect** — performance improves with each subsequent condition
- **Fatigue effect** — performance worsens with subsequent conditions
- Practice is a **confounding variable** in within-subjects designs

### Counterbalancing
> Dividing participants into groups and administering conditions in **different orders** to offset practice effects.

### Latin Squares
> An n×n table where each symbol appears exactly **once per row and once per column**.

**Standard Latin Squares:**
```
2×2:  A B    3×3:  A B C    4×4:  A B C D
      B A          B C A          B C D A
                   C A B          C D A B
                                  D A B C
```

**Balanced Latin Squares** (for even n — each condition precedes/follows every other equally):
```
4×4:  A B D C      6×6:  A B F C E D
      B C A D            B C A D F E
      C D B A            C D B E A F
      D A C B            D E C F B A
                         E F D A C B
                         F A E B D C
```

### Participant Requirements
- Number of participants must be **divisible by the number of levels**
- e.g., 3-level factor → use 9, 12, or 15 participants

### Counterbalancing Example (3 editing methods A, B, C; 12 participants):
- Group 1: A → B → C
- Group 2: B → C → A
- Group 3: C → A → B
- Results: Mouse method (C) = 13.0s, Arrow keys (A) = 15.2s, Search/Replace (B) = 15.5s
- Group means were very close (~0.3s difference) → counterbalancing worked

### Odd Number of Conditions
- Standard Latin square is imbalanced (B follows A twice, A follows B once)
- Solution: Use **all n! sequences**
    - 3 conditions → 3! = 6 orderings (complete balance)

### Random Assignment Alternative
- Appropriate when: task is brief, many repetitions, many conditions
- Conditions chosen at random **without replacement** per block

---

## 5.12 Group Effects and Asymmetric Skill Transfer

### Group Effect
> Significant differences across groups in mean DV scores — indicates counterbalancing **failed**.

### Asymmetric Skill Transfer
> Different amounts of skill transfer depending on the **order** of testing.
- Occurs when one condition serves as better practice for a subsequent condition than vice versa

### Classic Example (Koester & Levine, 1994):
- Compared LO (letters-only) vs. L+WP (letters + word prediction) scanning keyboards
- Group 1 (LO→L+WP): 31.4 cpm — performed better
- Group 2 (L+WP→LO): 28.8 cpm — 8% slower
- **Why?** LO was excellent practice for the more complex L+WP; L+WP first was harder → less benefit to LO second
- Lines in learning curve **crossed over** → asymmetry confirmed

### Solutions:
- Use a **between-subjects design** (eliminates cross-condition transfer entirely)
- Have participants **practice** a condition before data collection to equalize starting points

---

## 5.13 Longitudinal Studies

### Definition
> An experimental evaluation where participants practice over a **prolonged period** and improvement in performance is measured.

- Used when learning/skill acquisition is the research interest (not something to eliminate)
- **Amount of practice** becomes the IV (e.g., *Session 1, Session 2, … Session N*)

### Key Features
- Reveals **power law of learning** curves
- Goal: compare new technique against current practice over time
- May show a **crossover point** — where new technique surpasses current practice

### Crossover Point
- Before crossover → **Cost** (current practice is better)
- After crossover → **Benefit** (new technique is better)

### Example (MacKenzie et al., 2001):
- Multi-tap vs. LetterWise text entry over 20 sessions
- Session 1: both ~7.3 wpm
- Session 20: LetterWise = 21.0 wpm vs. Multi-tap = 15.5 wpm (36% faster)
- LetterWise uses 44% fewer keystrokes on average for English

### Qwerty vs. Dvorak Case Study
- Dvorak Simplified Keyboard (DSK) shown to be faster in longitudinal studies
- Yet Qwerty dominates — two reasons:
    1. **Manufacturing cost** — keyboards require ground-up reengineering
    2. **User resistance** — people are change-averse; unwilling to retrain

### Virtual/Soft Keyboards
- Created in software → **no retooling cost**
- Better opportunity for optimized designs
- Optimized layouts (common letters centered) → less movement → faster, but requires learning
- Requires longitudinal study to find crossover point

---

## 5.14 Running the Experiment

### Before Testing Begins
- **Final pilot test** with 1–2 participants to:
    - Smooth out briefing/preparation protocol
    - Verify timing fits within scheduled session (e.g., 1 hour)
    - Catch any last-minute issues

### During Testing
- Greet participant → introduce experiment → consent form
- Brief questionnaire (demographics, related experience)
- Reveal apparatus → explain and demonstrate task → practice trials
- Collect data

### Instructions to Participants
- Typically: proceed **quickly and accurately**
- Must be given **consistently** to all participants
- Avoid additional explanations that could cause differential behavior

### Experimenter's Role
- Act as **neutral** — do not convey preference for any outcome
- Avoid making participant nervous (overly attentive) or disengaged (indifferent)
- Participants should not feel pressure to produce a specific result

---

## Key Terms Summary

| Term | Definition |
|------|------------|
| Independent Variable (IV) | Manipulated factor with ≥2 levels |
| Dependent Variable (DV) | Measured human behavior/performance |
| Control Variable | Held constant to reduce noise |
| Random Variable | Allowed to vary freely; increases generalizability |
| Confounding Variable | Varies systematically with IV; threatens validity |
| Within-subjects | All participants tested on all conditions |
| Between-subjects | Separate group per condition |
| Counterbalancing | Varying condition order across groups to offset practice effects |
| Latin Square | n×n ordering table; each condition appears once per row/column |
| Balanced Latin Square | Each condition precedes/follows every other equally (even n only) |
| Order Effect | Performance change due to sequence of conditions |
| Asymmetric Skill Transfer | Unequal learning transfer depending on testing order |
| Longitudinal Study | Extended practice study measuring skill acquisition over time |
| Crossover Point | Moment new technique outperforms current practice in learning curve |
| Factorial Experiment | Experiment with IVs and measured DVs |

---

# Heuristic Evaluation of User Interfaces
**Authors:** Jakob Nielsen & Rolf Molich  
**Published:** CHI '90 Proceedings, April 1990

---

## Abstract

> Heuristic evaluation is an **informal method of usability analysis** where evaluators are presented with an interface design and asked to comment on it.

- Individual evaluators found only **20–51%** of usability problems
- Aggregating evaluations from **3–5 evaluators** produces significantly better results

---

## Introduction

### Four Ways to Evaluate a User Interface

> There are four fundamental evaluation approaches, each with different trade-offs in feasibility and thoroughness.

- **Formal** — analysis techniques; still in research, not yet practically applicable
- **Automatic** — computerized; only feasible for primitive checks
- **Empirical** — experiments with test users; thorough but rarely used in practice
- **Heuristic** — informal judgement-based; most common in real life

### Why Study Heuristic Evaluation?

- Only **6%** of Danish software companies used the thinking-aloud method (Milsted et al., 1989); no one used any other empirical/formal method
- Most real-world evaluations are heuristic — studying them has practical value

---

## Heuristic Evaluation

### Definition

> Heuristic evaluation = looking at an interface and forming an opinion about what is good and bad, ideally guided by usability principles.

### The Nine Usability Heuristics (Molich & Nielsen, 1990)

> These heuristics reduce the complexity of thousand-rule guideline documents to a practical, teachable set.

1. Simple and natural dialogue
2. Speak the user's language
3. Minimize user memory load
4. Be consistent
5. Provide feedback
6. Provide clearly marked exits
7. Provide shortcuts
8. Good error messages
9. Prevent errors

---

## Empirical Test of Heuristic Evaluation

### Methodology

> The same basic method was used across all four experiments: evaluators received an interface design, wrote a report on usability problems, and were scored against a master list.

- Scoring was **liberal** — credit given even for incomplete descriptions of problems
- Master lists were updated after initial review (experts aren't perfect either)

### Summary of Four Experiments

| Experiment | Evaluators | Known Problems | Avg. % Found |
|---|---|---|---|
| Teledata (videotex) | 37 | 52 | 51% |
| Mantel (phone info system) | 77 | 30 | 38% |
| Savings (voice response) | 34 | 48 | 26% |
| Transport (voice response) | 34 | 34 | 20% |

### Experiment 1: Teledata
- Danish videotex system; evaluators given 10 screen dumps
- Evaluators: 37 CS students, trained on heuristics
- **Best performance** of the four experiments (51%)

### Experiment 2: Mantel
- Fictional telephone directory system; specification-only (no live system)
- Evaluators: 77 readers of *Danish Computerworld* (industry professionals)
- No heuristics lecture given — relied on intuition

### Experiments 3 & 4: Savings & Transport (Voice Response)
- Both used the **same 34 CS students** — enables cross-experiment comparison
- Voice interfaces are especially hard to evaluate due to **low persistence** (messages disappear once spoken)
- Four shared inconsistency problems (e.g., the `#` key used differently) counted in both systems

---

## The Usability Problems

### Examples by Detection Rate

> Problems ranged from near-universal to easily overlooked, illustrating the wide variance in problem visibility.

- **95%** found: Mantel overwrites the entered phone number when displaying results
- **62%** found: Transport shifts menus without pause or indication
- **54%** found: Error message "UNKNOWN IP" in Teledata is unreadable
- **35%** found: Savings system's online help is undiscoverable without printed guide
- **12%** found: Transport access keys based on internal departmental structure, not public bus numbers

### Validity of Problems

> Two arguments support the validity of identified usability problems:

1. Most are "obviously" problematic by established usability knowledge
2. With 34+ people working through each interface, major problems are unlikely to go unnoticed

---

## Evaluation Results

### Key Findings

> Heuristic evaluation is **difficult** — even in the best case, only half of problems were found by individual evaluators.

- Average problems found: **51%, 38%, 26%, 20%** across the four experiments
- Distribution roughly follows a **normal distribution** — most evaluators perform near average
- Voice response systems were hardest to evaluate

### Individual Differences (Table 3 Summary)

| Experiment | Min % | Max % | Q1 % | Q3 % | Max/Min |
|---|---|---|---|---|---|
| Teledata | 22.6 | 74.5 | 43.2 | 58.5 | 3.3 |
| Mantel | 0 | 63.3 | 30.0 | 46.7 | ∞ |
| Savings | 10.4 | 52.1 | 18.8 | 31.3 | 5.0 |
| Transport | 6.7 | 46.7 | 11.8 | 26.5 | 7.0 |

- Q3/Q1 ratio ≈ **2** (comparable to text editing tasks; lower than programming)
- Cross-experiment correlation is **weak** (R²=0.33) — good evaluators in one task may not be good in another
- Harder interfaces show **larger individual differences**

### False Positives

> False positives were rare and typically flagged by only one evaluator — easily resolved by group discussion or empirical testing.

---

## Aggregated Evaluations

### Why Aggregation Works

> Problem-finding does NOT form a perfect cumulative (Guttman) scale — poor evaluators sometimes catch hard problems, and good evaluators sometimes miss easy ones.

- This **non-cumulative** nature means combining evaluators yields more than the best individual alone
- Guttman reproducibility coefficient R = 0.85 (approximate, not perfect scale)

### How Aggregation is Done

1. Each evaluator independently reviews the interface and writes a report
2. A central authority (usability expert or group meeting) consolidates findings
3. Combined list = union of all identified problems

> Independence is critical — evaluators working together may bias each other and reduce variety in findings.

### Results of Aggregation (Table 4)

| Aggregate Size | Teledata | Mantel | Savings | Transport |
|---|---|---|---|---|
| 1 | 51% | 38% | 26% | 20% |
| 2 | 71% | 52% | 41% | 33% |
| 3 | 81% | 60% | 50% | 42% |
| 5 | 90% | 70% | 63% | 55% |
| 10 | 97% | 83% | 78% | 71% |

> Aggregates of **5 evaluators** find approximately **two-thirds** of all usability problems — strong performance for an informal, low-cost method.

### Diminishing Returns

- Rapid improvement from **1 → 5 evaluators**
- Flattens between **5 → 10 evaluators**
- Point of diminishing returns reached at **~10 evaluators**

---

## Conclusions

### Recommendations

> Do not rely on a single evaluator. Use 3–5 independent evaluators, then invest remaining resources in complementary methods.

- Optimal group size: **3–5 evaluators**
- Evaluators should work **independently** before comparing results
- Supplement with methods like **thinking aloud**

### Advantages of Heuristic Evaluation

- **Cheap**
- **Intuitive** — easy to motivate people to participate
- **No advance planning** required
- **Usable early** in the development process

### Disadvantages

- Identifies problems but may **not suggest solutions**
- Biased by evaluators' **current mindset**
- Generally **does not generate design breakthroughs**
- Only tested on **small-scale interfaces** — scalability unknown
- Focused on polishing completed designs, not holistic design selection

---

## Key Concepts to Remember

> Exam-critical takeaways from Nielsen & Molich (1990):

- **Heuristic evaluation** = informal, judgement-based UI review using usability principles
- **9 heuristics** are the practical basis (see list above)
- Single evaluators find only **20–51%** of problems
- **3–5 independent evaluators** is the recommended sweet spot
- Aggregation works because problem-finding is **not purely cumulative**
- Voice/audio interfaces are **harder** to evaluate (low persistence)
- Always **supplement** heuristic evaluation with empirical methods

---

# Exam Study Notes: Cognitive Walkthroughs
**Authors:** Polson, P. G., Lewis, C., Rieman, J., & Wharton, C.[cite: 1]
**Full Title:** Cognitive walkthroughs: a method for theory-based evaluation of user interfaces[cite: 1]
**Source:** Int. J. Man-Machine Studies (1992)[cite: 1]

---

## I. Core Definition & Purpose
* **The Method:** A theory-based evaluation tool used early in the design cycle to assess usability by simulating a user's mental processes[cite: 1].
* **Primary Focus:** **Ease of Learning**. It specifically evaluates how easily a user can learn to perform a task by exploration (guessing) rather than through formal instruction[cite: 1].
* **Key Advantage:** Unlike empirical testing, a walkthrough can be performed before an implementation or even a mock-up exists[cite: 1].

---

## II. Theoretical Foundations
The method is built on two primary cognitive frameworks:

### 1. The Construction-Integration (CI) Model (Kintsch)
* Users construct a mental representation of a task and integrate it with background knowledge[cite: 1].
* **Activation Flow:** Activation flows from the top-level goal to representations of actions[cite: 1]. When an action (like a button) is sufficiently "activated," the user executes it[cite: 1].
* **The Path:** To succeed, an associative path must exist: **Active Goal → Button Label → Button Description/Location → Physical Action**[cite: 1].

### 2. The Action Cycle
Derived from Norman’s theory, it involves four stages:
1.  **Goal Formation:** The user decides what they want to do[cite: 1].
2.  **Exploration:** The user looks for actions that match the goal[cite: 1].
3.  **Selection:** Choosing an action (often via the **Label Following** heuristic)[cite: 1].
4.  **Feedback Interpretation:** Evaluating the system's response to see if progress was made[cite: 1].



---

## III. Key Concept: Goal Management

### "And-Then" Goal Structures
* Many tasks are organized into "and-then" structures where subgoals must be accomplished in a fixed, linear order[cite: 1].
* These consist of "want-to" nodes (intentions) and "done-it" nodes (achievements)[cite: 1].



### The "Supergoal Kill-off" (The Semicolon Problem)
* **What it is:** A common error where a user prematurely terminates a task[cite: 1].
* **The Cause:** If a subgoal is too similar to the original supergoal, the "done-it" node for the subgoal triggers the deactivation of the supergoal[cite: 1].
* **Example:** In an ATM transaction, the goal is "Give system my PIN." The first subgoal is "Type in PIN" and the second is "Press ENTER"[cite: 1]. If "Type in PIN" is seen as the same as the main goal, the user might stop and forget to press ENTER[cite: 1].

---

## IV. The Walkthrough Procedure: Phase 1 (Preparation)
Before the evaluation begins, the analyst needs:
1.  **Design Description:** Detailed interface specs[cite: 1].
2.  **Task Scenario:** A representative task from the user's viewpoint[cite: 1].
3.  **Correct Action Sequence:** The exact "best" steps to finish the task[cite: 1].
4.  **Anticipated User Population:** Definitions of their background knowledge (e.g., "knows what a # sign is")[cite: 1].
5.  **User’s Initial Goals:** What the user *actually* wants to do when they sit down[cite: 1].

---

## V. The Walkthrough Procedure: Phase 2 (Evaluation Questions)
For **every action** in the correct sequence, the analyst must ask:

### 1. Goal Structure
* **Correct Goals:** Are the goals necessary for this step currently active in the user's mind?[cite: 1]
* **Mismatch:** Will the user have these goals, or will they have dropped them/never formed them?[cite: 1]

### 2. Choosing and Executing the Action
* **Availability:** Is it obvious that the action is a choice? (e.g., is the button hidden?)[cite: 1]
* **Label Link:** Is the label clearly associated with the action and the user's goal?[cite: 1]
* **Wrong Choices:** Are there other actions that look like a better match to the current goal?[cite: 1]
* **Hard to Do:** Is the physical action (e.g., a complex chorded keypress) tricky?[cite: 1]

### 3. Modification of Goal Structure
* **Progress:** Will the user see they are making progress?[cite: 1]
* **Accomplished Goals:** Is it obvious that a goal is finished?[cite: 1]
* **False Completion:** Does an *incomplete* goal look like it’s done?[cite: 1]
* **New Goals:** Does the system provide a prompt that clearly leads to the next goal?[cite: 1]

---

## VI. Comparison with Other Methods
| Method | Strengths | Weaknesses compared to Walkthrough |
| :--- | :--- | :--- |
| **GOMS / CCT** | Predicts time/expert performance[cite: 1]. | Doesn't model exploration or learning[cite: 1]. |
| **PUMS** | Detailed reasoning modeling[cite: 1]. | High burden; requires complex coding[cite: 1]. |
| **Heuristic Eval** | Cheap, intuitive[cite: 1]. | Less structured; doesn't trace goal formation[cite: 1]. |
| **User Testing** | Finds the most errors[cite: 1]. | Doesn't always explain *why* errors happen[cite: 1]. |

---

## VII. Exam Tips: Common Evaluation Pitfalls
* **Granularity:** If actions are grouped too broadly (e.g., "Enter PIN"), you might miss "Supergoal Kill-off" errors[cite: 1].
* **Analyst Bias:** Experts often assume users know more than they do; always check the "Anticipated User Population" section[cite: 1].
* **Label Matching:** Users will follow labels that share words with their goal even if the action is wrong[cite: 1].

---


# 3.7

# Towards a Framework for Integrating Agile Development and User-Centred Design
**Authors:** Stephanie Chamberlain, Helen Sharp, and Neil Maiden
**Source:** ChamberlainSharpMaiden-TowardsaFramework.pdf (XP 2006)

---

## 1. Overview and Problem Statement
Integrating User-Centred Design (UCD) and Agile is attractive because developers are rarely usability experts, and both fields value user involvement. However, fundamental differences in pace, documentation, and philosophy make integration difficult.

* **Agile Manifesto:** Emphasizes customer involvement, but in practice, "real" end-users rarely take the role of the customer.
* **UCD Aim:** To involve users meaningfully throughout the entire development lifecycle, from initial research to iterative testing.

---

## 2. Theoretical Comparison: Agile vs. UCD

### 2.1 The Three Primary Similarities
1. **Iterative Development:** Both build on empirical information from previous cycles (Agile via refactoring/feedback; UCD via iterative design).
2. **User Emphasis:** Agile uses participation (Scrum reviews/Product Owners); UCD focuses early and continually on users.
3. **Team Coherence:** Both require the whole team to be aligned—Agile through the "Planning Game" and UCD by keeping the user's mental model central.

### 2.2 The Two Primary Differences
1. **Documentation:** UCD practitioners believe design products (personas, specs) are vital for communication; Agile seeks "minimal documentation."
2. **Up-front Investigation:** UCD encourages understanding users *before* the build begins; Agile is biased against any up-front work that happens at the expense of writing code.

---

## 3. Case Studies: Analysis of Three Projects
The paper analyzes a field study at a large media organization. Each project integrated the two methods differently:

### Project I (Civic Life Website) - Integrated Scrum/UCD
* **Strategy:** Designers did not enter the Scrum until there was clear value. They used a separate "up-front" period for research.
* **Workflow:** One designer "fed" the Scrum with prototypes while two others conducted ongoing user research.
* **Tools:** Used personas, user journeys (scenarios), and analyzed existing usage patterns.

### Project S (Interactive TV Quiz) - Parallel XP/UCD
* **Strategy:** High-pressure project with fixed transmission dates. XP was the primary driver.
* **User Involvement:** Minimal direct user contact. User needs were represented by "proxy users" from within the team (e.g., a broadcast assistant).
* **Observation:** UCD tools were often overlooked due to extreme time pressure.

### Project M (Internal Message-Board System) - Separate Scrum/UCD
* **Strategy:** Designers found attending Scrum with developers unhelpful. They ran a parallel UCD process.
* **Observation:** This led to segregation and detachment. Developers and designers ended up operating in silos.

---

## 4. Four Core Emergent Themes
The field study identified these four areas as the biggest "friction points" in integration:

### 4.1 User Involvement
* Users are often represented by "proxies" within the organization rather than real end-users.
* **Tactics:** Personas, user journeys, and analyzing patterns from existing systems help bridge the gap.

### 4.2 Collaboration and Culture
* **Power Struggles:** Disciplines often use their methodology as a "defense mechanism" against others. Developers might build a back-end based on a technical lead's spec before a designer has finished the user journey.
* **Defensiveness:** Observed when Scrum Masters or Leads feel their estimates or authority are being questioned.

### 4.3 Prototyping
* **The Pace Problem:** Design prototyping (often paper) is much faster than development prototyping.
* **Lag Time:** Developers may take weeks to implement a prototype that a designer needs for testing, leading to a "lag" in the iteration cycle.

### 4.4 Project Lifecycle
* **Up-front Design:** UCD requires research, mapping mental models, and prioritizing tasks *before* the first sprint.
* **The Business Analysis Phase:** Successful projects (like M) sometimes dedicated a whole sprint specifically to requirements gathering at the start.

---

## 5. The Five Principles of the Framework
These are the authors' recommendations for successful integration:

1. **User Involvement:** Involve users directly, but support this with proxy roles (like a dedicated customer representative) on the internal team.
2. **Collaboration and Culture:** Designers and developers must work together daily. The customer must be an active team member, not a passive bystander.
3. **Prototyping:** Designers must "feed the developers" with prototypes and feedback on a cycle that matches the development velocity.
4. **Project Lifecycle:** UCD practitioners must be given a "discovery period" to understand user needs before any code is committed to a shared environment.
5. **Project Management:** The integration must exist within a cohesive framework that facilitates communication without being overly bureaucratic.

---

## 6. Exam-Critical Conclusions: Why Integration Fails
If you are asked to analyze a failing project, look for these "Hurdles" mentioned in the paper:
* **Power struggles:** One discipline (usually Dev) overriding the design requirements.
* **Outcome Capacity:** Development takes significantly longer than design, creating frustration.
* **Siloing:** Designers not taking part in Scrum or developers not being involved in user journeys.
* **Resource Mismatch:** Designers being spread across too many projects, causing them to miss key Agile meetings.

# How do Design and Evaluation Interrelate in HCI Research?
**Authors:** Christine E. Wania, Michael E. Atwood, Katherine W. McCain[cite: 3]
**Source:** WaniaAtwoodMcCain-HowDoDesignAndEvaluationInterrelate.pdf[cite: 3]

---

## 1. Introduction and Definition of Human-Computer Interaction (HCI)
* **Official ACM SIGCHI Definition:** HCI is a discipline concerned with the design, evaluation, and implementation of interactive computing systems for human use and with the study of the major phenomena surrounding them[cite: 3].
* **Practical Goal:** Understanding and creating software and technology that people will want to use, be able to use, and find effective[cite: 3].
* **Multidisciplinary Nature:** Combines theories from computer science, cognitive and behavioral psychology, anthropology, sociology, and ergonomics[cite: 3].

### The Four Foundations of HCI (Foundational Threads)
HCI was built on technical developments from the 1960s and 1970s[cite: 3]:
1. **Software Engineering:** Introduced prototyping and iterative development[cite: 3].
2. **Human Factors:** Focused on software psychology and human factors of computing systems[cite: 3].
3. **Computer Graphics:** Contributed user interface software and tools[cite: 3].
4. **Cognitive Science:** Provided models, theories, and frameworks[cite: 3].

---

## 2. The Design vs. Evaluation Divide
* **The Reality:** While design and evaluation are defined as closely related, they are typically separated in practice[cite: 3].
* **Professional Separation:** Academia often teaches these skills separately, and industry typically hires individuals to be either "designers" or "evaluators"[cite: 3].
* **Common Goal:** Both share the goal of usability but take different paths to achieve it[cite: 3].
* **Emerging View:** Modern research argues that design and evaluation are an evolutionary process situated in the context of use[cite: 3]. It is impossible to predict all requirements or unintended consequences before a system is implemented; therefore, software should be "grown," not just "built"[cite: 3].

---

## 3. Taxonomy of Design Methods
Design methods have evolved through three generations[cite: 3]:
* **First Generation:** Product-oriented; focused on systems theory and software engineering[cite: 3].
* **Second Generation:** Process-oriented; focused on user participation and democracy (1970s)[cite: 3].
* **Third Generation:** Use-oriented; focuses on the actual use situation and assessing quality in use[cite: 3].

### Major Design Philosophies
* **Participatory Design (PD):** Emphasizes workplace democracy and human development[cite: 3]. It involves users as active, creative participants and full partners in the design process[cite: 3].
* **User-Centered Design (UCD):** A philosophy where user needs and goals (not technology) drive development[cite: 3]. While users are involved, they may not always be "full participants" in the way they are in PD[cite: 3].
* **Interaction Design (ID):** The process of designing interactive products to support people in everyday and working lives[cite: 3]. Key characteristics include a focus on users, iteration, and identifying specific usability/user experience goals at the start[cite: 3].

---

## 4. Taxonomy of Evaluation Methods
Evaluations are categorized into four basic types: automatic, empirical, formal, and informal[cite: 3].

### Informal or Inspection-Based Evaluation
* **Usability Inspection Methods (UIMs):** Non-empirical methods where evaluators inspect the interface[cite: 3].
* **Heuristic Evaluation:** Evaluators assess the UI based on established "rules of thumb" or heuristics[cite: 3].
* **Cognitive Walkthrough:** A theory-based method simulating the user's cognitive processes to evaluate learnability[cite: 3].

### Formal or Model-Based Evaluation
* **GOMS:** Acronym for Goals, Operators, Methods, and Selection Rules[cite: 3]. It uses calculations or simulations of a human model to predict usability measures[cite: 3].

### Empirical or User-Based Evaluation
* **Usability Testing:** Observing real users as they use a product to see if they can complete features within a reasonable amount of time and effort[cite: 3].
* **Think Aloud:** Users vocalize their mental process during a task[cite: 3].

---

## 5. Author Cocitation Analysis (ACA) and The 7 Clusters
The authors used bibliometric analysis of HCI literature (1990–2004) to visualize how the community sees the relationship between design and evaluation[cite: 3].

### The Author Cocitation Map (Two Dimensions)

* **X-Axis (Theory to Application):** Spans from theory building (left) to building usable systems (right)[cite: 3].
* **Y-Axis (Aggregate to Individual):** Spans from focusing on groups/collaboration (top) to focusing on the individual user's cognition (bottom)[cite: 3].

### The Seven Major HCI Clusters
1. **User-Centered Design:** Focuses on methods for creating and evaluating usable systems[cite: 3].
2. **Participatory Design:** Focuses on workplace democracy and active cooperation between users and designers[cite: 3].
3. **CSCW (Computer-Supported Collaborative Work):** Focuses on systems that enhance group collaboration in the workplace[cite: 3].
4. **Cognitive Engineering:** Studies the cognitive properties of people and how they influence interactions with the environment[cite: 3].
5. **Cognitive Theories and Models:** Focused on understanding *how* users accomplish tasks and *why* they find systems usable[cite: 3].
6. **Design Theory and Complexity:** Concerned with building the high-level theories of design[cite: 3].
7. **Design Rationale:** Acts as a "boundary spanner," documenting *why* a system was designed a certain way to help with future redesign and predicting consequences of changes[cite: 3].

---

## 6. The Center of the HCI Community: Context of Use
* **The Center:** The intersection of the axes (Theory-Application and Group-Individual) represents the core of the community[cite: 3].
* **Key Authors at the Center:** Gerhard Fischer, Terry Winograd, Lucy Suchman, Ed Hutchins, and Gary Olson[cite: 3].
* **The Unifying Theme:** What ties these central authors together is a focus on the **Context of Use**[cite: 3].
* **Key Concepts:**
  * **Situated Action (Suchman):** Cognition is tied to the specific situation[cite: 3].
  * **Cognition in the Wild (Hutchins):** Studying cognition in real-world settings rather than labs[cite: 3].
  * **Seeding-Evolution-Reseeding (Fischer):** An incremental development model based on context[cite: 3].

---

## 7. Conclusions for Research and Education
* **Integration via Philosophy:** The analysis shows that design and evaluation aren't separate communities, but rather part of shared **philosophies**[cite: 3].
* **Educational Shift:** Instead of teaching design and evaluation as separate courses, they should be taught within a specific philosophy (e.g., a course on Participatory Design covering its specific design and evaluation methods)[cite: 3].
* **Future Trend:** The field is moving toward understanding design and evaluation strictly within the **real context of use**[cite: 3].


---

# 3.8

# Characterizing Homelessness Discourse on Social Media
**Authors:** Andrea Hu, Stevie Chancellor, Munmun De Choudhury
**Source:** HuChancellorChoudhury-CharacterizingHomelessness.pdf (CHI 2019)

---

## 1. Abstract and Research Goal
This paper uses computational linguistic analysis on Tumblr to understand how homeless individuals express their needs, frustrations, and social distress. By comparing homeless and non-homeless bloggers, the study identifies unique ways this underserved population seeks emotional and practical support.

---

## 2. Introduction: The Digital Life of the Homeless
* **Connectivity:** Social media is a vital tool for the homeless to maintain relationships despite transience and physical barriers.
* **Mobile Ownership:** Surveys show mobile phone ownership among the homeless ranges from 61.5% to 76%.
* **Device Valuation:** Homeless individuals view their phones as essential as food and are generally unwilling to sell them even during extreme financial hardship.
* **Platform Usage:**
  * 48% of homeless participants in a 2010 study used Facebook.
  * 79% of homeless youth in Seattle (2011) used social media at least once a week.
* **Why Tumblr?** Tumblr's support for pseudonymous accounts makes it a safe space for disclosing stigmatizing information. It allows for "elaborate narratives" through long-form blogging.

---

## 3. Methodology and Data Collection

### Data Scrape
* **Source:** Public Tumblr API.
* **Hashtags:** Collected posts tagged with #homeless, #homelessness, #homeless shelter, #poverty, and #begging.
* **Total Corpus:** 26,098 text posts.

### Identifying Homeless Bloggers
* **Manual Labeling:** Researchers labeled 1,000 random posts to find "self-disclosures" (people stating they are, were, or are about to be homeless).
* **Veracity Check:** Blogs containing a self-disclosure were categorized as "homeless bloggers."
* **Final Set:** 580 homeless posts (from 142 bloggers) and 1,996 not-homeless posts (from 739 bloggers).

### Computational Techniques
1. **LIWC (Linguistic Inquiry and Word Count):** Analyzes psycholinguistic word categories.
2. **Log Likelihood Ratios:** Compares hashtag frequency between the two groups.
3. **Word2Vec (Word Embeddings):** Uses cosine similarity to find contextual relationships between words.
4. **LDA (Latent Dirichlet Allocation):** Unsupervised topic modeling to find recurring themes.

---

## 4. Key Findings: Psycholinguistic Analysis
* **Emotional Distress:** Homeless bloggers use significantly more words related to negative affect (NA), anger, sadness, and anxiety (12-54% higher than non-homeless).
* **Daily Struggles:** High use of words related to 'work', 'money', 'health', 'body', and 'humans' (16-44% higher).
* **Self-Focus:** A 39% higher use of first-person pronouns (I, me) indicates a strong self-attentional focus on personal experiences and survival.
* **Target Audience:** Friend-related words were more common than family-related words, possibly due to Tumblr's specific community structure.

---

## 5. Hashtag and Topic Differences

### Homeless Bloggers (Focus: Survival & Distress)
* **Financial/Health Tags:** #poverty, #destitute, #suicide, #anxiety, #alcoholism, #self_harm.
* **Professional/Practical Tags:** #jobless, #unemployable, #housing, #tent_life, #hunger.

### Not-Homeless Bloggers (Focus: Advocacy & Charity)
* **Altruistic Tags:** #non-profit, #charity, #kindness, #gratitude, #generosity, #ministry.
* **Social Commentary:** These users discuss homelessness as a societal issue rather than a lived experience.

### The Significance of "Car"
* In the Word2Vec analysis, "car" appeared as a top-similar term for "homeless", "help", "food", and "poor."
* **Context:** For the homeless, a car is viewed as a temporary shelter and one of the last items of personal ownership after losing a house.

---

## 6. LDA Topic Modeling Comparison

### Homeless Topics (13 Topics)
* **Survival Items:** Discussions about kittens/pets (companionship), tents, and cars.
* **Major Events:** Christmas, Thanksgiving, and the struggle to find "dinner."
* **Support Systems:** Veterans assistance, HUD, and disability rights.
* **Social Connections:** Themes involving "love," "friends," and "mother."

### Not-Homeless Topics (17 Topics)
* **Public Figures/News:** Pope Francis, news updates, and volunteering.
* **Religion/Spirituality:** Topics involving God, Jesus, and church ministry.
* **Awareness:** LGBTQ youth homelessness and advocacy projects.

---

## 7. Discussion: Social Connectedness and Utility
* **Social Support:** Tumblr serves as a unique mechanism for both emotional needs (venting, finding dignity) and practical needs (seeking financial help via GoFundMe or PayPal).
* **Digital Connectedness:** Homeless bloggers use the platform to stay connected with peers while navigating "stigmatizing" life events.
* **Stigma Management:** Tumblr allows for "indirect disclosures," where users can send clues about their situation and test the waters before asking for help.

---

## 8. Recommendations for Future HCI Work
1. **Targeted Design:** Social media should be designed to more effectively meet the practical survival needs (shelter/financial) of homeless users.
2. **Real-time Tools:** Development of recommendation tools that point users to local resources (shelters, short-term jobs) based on their posts.
3. **Streamlined Aid:** Integrating donation platforms (GoFundMe/PayPal) more seamlessly into social apps to connect donors with those in need.
4. **Advocacy Platforms:** Using these digital artifacts to surface the needs of underserved populations to nonprofits and lawmakers.

---

# The Aware Home: A Living Laboratory for Ubiquitous Computing Research
**Authors:** Cory D. Kidd, Robert Orr, Gregory D. Abowd, Christopher G. Atkeson, Irfan A. Essa, Blair MacIntyre, Elizabeth Mynatt, Thad E. Starner, and Wendy Newstetter
**Institution:** Georgia Institute of Technology (1999)

---

## 1. Project Overview
The Aware Home is a "living laboratory" designed to research ubiquitous computing in the context of everyday home life. Unlike typical office-based research, this project focuses on the "free choice" environment of the home, where activities are not dictated by organizational productivity but by personal preference and domestic rhythms.

### The Prototype Structure
* **Layout:** A two-story home with two identical, independent living spaces. Each floor includes two bedrooms, two bathrooms, an office, kitchen, dining room, living room, and laundry.
* **Basement:** Contains a shared home entertainment area and a centralized control room for computing services.
* **Purpose of Dual Spaces:** Allows for controlled experiments where researchers or participants can live on one floor while the other is used for active prototyping or demonstrations.

---

## 2. Technology-Centered Research Agenda

### Context Awareness and Ubiquitous Sensing
The project aims to bridge the gap between human context and computer interpretation. This involves building sensors that can interpret the whereabouts and activities of inhabitants.
* **Vision-Based Sensors:** Tracking multiple individuals within the home.
* **Smart Floor:** A non-intrusive tracking system that identifies and locates individuals based solely on their footsteps.

### Human-Home Symbiosis
Research explores the interaction between "on-body" sensing (wearable computing) and "off-body" sensing (the home's infrastructure).
* **Collaboration:** Wearables gather data wherever the user goes, while the home infrastructure provides computation and sensing at a distance.
* **Information Exchange:** Personal data from wearables can be filtered and released to the house as needed, or the house can provide data to the wearable for mobile use.

### The Smart Floor Project
A specialized system using force-sensitive load tiles to gather **Ground Reaction Force (GRF)** profiles.
* **Mechanism:** Uses Hidden Markov Models (HMMs) and feature-vector averaging to identify users.
* **Accuracy:** Capable of identifying users within a small population (approx. 10 people) with over 90% accuracy.
* **Alternative Tracking:** Exploring piezoelectric wires, optical fibers, and vibration sensors for finer-grained movement tracking.

---

## 3. Human-Centered Research Agenda

### Support for the Elderly (Aging in Place)
A primary application of the Aware Home is assisting the elderly to live independently for longer, improving their quality of life and reducing the need for institutionalization.
* **Social Connections:** Creating persistent links between elderly parents and adult children to provide "peace of mind."
* **Everyday Cognition:** Augmenting memory and planning capabilities that naturally decline with age.
* **Crisis Sensing:** Detecting emergencies (e.g., falls or medical distress) to contact outside services automatically.

### Finding Lost Objects (FLO)
A system designed to locate Frequently Lost Objects such as keys, wallets, or remote controls.
* **Technology:** Uses small radio-frequency (RF) tags and a long-range indoor positioning system.
* **Interface:** Users interact via LCD touch panels and receive spatialized audio cues (e.g., "Your keys are in the bedroom").
* **Redundancy:** If tags fail, other tracking systems (like the Smart Floor) can provide context, such as who was last seen with the object and where.

---

## 4. Evaluation and Social Challenges

### Qualitative Rhythms of Home Life
Designing for the home requires a shift from "Tayloristic" notions of efficiency to an understanding of domestic life.
* **Methodology:** Use of ethnographic and qualitative techniques to observe how people structure their time and space.
* **Authentic Experience:** Following the "Classroom 2000" model, researchers emphasize that deep understanding of ubiquitous computing only comes from long-term, authentic use by real inhabitants.

### Privacy and Security
Constant monitoring via audio, video, and medical sensors raises significant privacy concerns.
* **User Control:** Occupants must have knowledge and control over how their information is distributed.
* **Security Models:** Proposals include storing sensitive personal data on a wearable computer to allow the user to act as the "gatekeeper" for their own information.

---

# Spaces and Traces: Implications of Smart Technology in Public Housing
**Authors:** Sandjar Kozubaev, Fernando Rochaix, Carl DiSalvo, and Christopher A. Le Dantec
**Published:** CHI 2019

---

## 1. Abstract and Research Focus
This research examines the deployment of smart home technologies beyond the traditional single-family, middle-class narrative. It focuses on the unique challenges within **US public housing**, where issues of surveillance, individual autonomy, and privacy intersect with complex social policies and diverse living arrangements. The study uses insights from participatory design workshops with residents and building managers to uncover how data collection and monitoring impact vulnerable populations, specifically the poor and elderly.



---

## 2. Introduction: Opening the Aperture
Domestic HCI research often assumes a wealthy, single-family context. This paper shifts the focus to **multi-family public housing**.
* **Problem Definition:** Smart home assumption of individualized control often meets the reality of centralized building automation in public housing.
* **Collaboration:** The research was a partnership with **Atlanta Housing**, the largest public housing agency in the southeast US.
* **Context:** The site (formerly Herndon Homes) was a multi-building development designed for sustainability, community building, and economic development.

---

## 3. Related Work and Theoretical Framing
### The Politicized Home
* **Smart Homes:** Evolution has shifted from advanced intelligent environments to an ecosystem of ubiquitous sensors.
* **Public Policy:** Public housing is inherently political. Unlike private homes, the power arrangements involve social service providers and state authorities.
* **Regulatory Enforcement:** Smart technologies in this setting can become tools for enacting and enforcing public policy (e.g., tracking compliance).

### Aging in Place
* Senior residents in public housing have unique health and awareness needs.
* Many passive monitoring systems are designed assuming an active caregiver is watching the data; this is often not the case for low-income seniors.
* The focus is on maximizing mutual support through built social networks among residents.

---

## 4. Methodology: Participatory Design Workshops
The researchers hosted three workshops in 2018 rooted in speculative futures and making.



### Workshop 1: Creating Sensors
* **Goal:** Introduce key concepts.
* **Activity:** Participants used "smart device cards" and a design game involving dice and stickers to imagine hypothetical smart devices (combining inputs like humidity/light with outputs like sound/text).

### Workshop 2: Uncertain Futures
* **Goal:** Critical reflection on consequences.
* **Activity:** Used "what if" prompt cards (e.g., "What if a smart speaker recorded your child doing all their homework?"). This pushed participants to think about privacy, storage, and malfunctions.

### Workshop 3: Seniors and Property Managers
* **Goal:** Understand specific operational and age-related needs.
* **Participants:** Senior residents and property management/maintenance staff.
* **Focus:** Concrete concerns like thermostats, smoke detectors, and managing medical emergencies.

---

## 5. Major Research Themes

### Tracking and Monitoring
* **Health and Safety:** Participants saw value in sensors for managing chronic conditions (e.g., asthma in children or dementia in seniors).
* **Personal Safety:** Tracking was viewed as a way to increase security when walking home after dark.
* **Visibility:** Tech enables a new kind of visibility that moves between self-monitoring and monitoring by outside authorities.

### The Boundaries of Privacy
* **Public vs. Private:** Residents generally welcomed sensors in public areas but fiercely protected the privacy of their individual units.
* **Distrust:** There was high suspicion regarding "always-on" devices like smart speakers, which residents viewed as eavesdropping.
* **Ambiguity:** Semi-public spaces (hallways, gyms) created friction, as smart computational capabilities could classify behavior and deduce patterns without explicit resident consent.

### Shifting Baselines and Infrastructure
* **The Digital Divide:** There is a chasm between the availability of tech and the baseline expectation of how to use it.
* **Technology as Infrastructure:** For seniors, the **TV** is the most critical technology.
* **Connective Tissue:** In a connected community, services like broadband and wireless data must be viewed as **infrastructure** (like water or heat) rather than an individual consumer cost.



---

## 6. Design and Policy Implications

### Accountabilities of Tracking
* Data and collection tools should be accessible to residents to support local, "smart" social practices.
* There is a risk that data could be used by housing providers to increase the burden on residents (e.g., determining eligibility for services based on algorithmic behavioral analysis).

### Self-Determination
* Residents expressed a desire for control over their data, such as the ability to view and erase recordings.
* Organizations should adopt **Privacy by Design (PbD)**, integrating privacy into organizational goals rather than delegating it to third-party vendors.

### Endpoint vs. Infrastructure
* Smart home narratives focus on the "endpoint" (the smart lock or camera), but change comes from the "enabling infrastructure."
* Basic amenities should be framed as mental health maintenance or community wellness tools.

---

## 7. Conclusion: Participation and Agency
While the goal of many smart initiatives is to bridge the digital divide, adding sensors into an environment already fraught with regulation and precarity can create more anxiety.
* **Resilience:** HCI research should empower support networks within these communities.
* **Agency:** A well-designed interface is insufficient if the user cannot assert real control over the "spaces and traces" of their personal data.

---

# Distributed Cognition as a Theoretical Framework for Information Visualization
**Authors:** Zhicheng Liu, Nancy J. Nersessian, and John T. Stasko
**Source:** LiuNersessianStasko-DistributedCognitionInfoVis.pdf (2008)

---

## 1. The Core Problem in InfoVis
Information Visualization (InfoVis) is defined as "the use of computer-supported, interactive, visual representations of abstract data to **amplify cognition**." While the technical aspects of representation and interaction are well-researched, the "cognition" part is often poorly understood or ignored.

* **Lack of Theory:** The field lacks encompassing theories to explain *why* a visualization is effective.
* **Over-reliance on Intuition:** Designers often depend on personal experience or simple heuristics (like Shneiderman’s Mantra) which lack the rigor of formal predictive theory.
* **The Goal:** Subsitantiate the theoretical foundation of InfoVis using the Distributed Cognition (DCog) framework.

---

## 2. Distributed Cognition (DCog) vs. Traditional Cognition

### Traditional "Reductionist" View
* **Unit of Analysis:** The individual human mind.
* **Model:** Perception -> Cognition -> Action.
* **Assumption:** Cognition happens "inside the head" by processing symbols and abstract representations in the brain.
* **Role of Artifacts:** Tools are seen as mere "scaffolds" or memory aids that make internal processing easier.

### Distributed Cognition (DCog) View
* **Unit of Analysis:** The **Cognitive System** (Human + Artifact + Environment).
* **Assumption:** Cognition is an **emergent property** of interaction. It is not bounded by the individual but is "stretched across" people and tools.
* **Philosophical Shift:** Tools do not just amplify an existing internal process; they **transform** the task into a different set of cognitive skills (e.g., changing a complex calculation into a simple pattern-matching task).

---

## 3. Internal vs. External Representations

### The Tower of Hanoi Isomorphs
The paper cites Zhang and Norman’s experiments with different versions of the Tower of Hanoi (Orange, Donut, and Coffee versions):
* **Externalization of Rules:** In some versions, rules are built into the physical properties of the artifact (e.g., a smaller cup cannot hold a larger one without spilling).
* **Finding:** When more information/rules are externalized, task completion time is shorter and error rates are significantly lower.
* **Key Lesson:** External representations are more than just inputs; they determine the cognitive strategies used to solve the problem.

---

## 4. Interaction: Pragmatic vs. Epistemic Actions
Interaction is not just a one-way street from human to computer. It is a reciprocal coordination.

* **Pragmatic Actions:** Actions taken to bring the user closer to a physical goal (e.g., clicking "Save" or moving a file).
* **Epistemic Actions:** Actions taken to improve the human’s mental computation or reduce cognitive load.
  * **Example (Tetris):** Rotating a piece multiple times more than necessary to help the brain "see" where it fits.
  * **Purpose:** These actions change the environment to make the internal mental work easier.

---

## 5. Coordination and Cognitive Coupling
Interaction in InfoVis should be viewed as the **propagation of representation states** across different media (e.g., from a notepad to a screen to a mental model) through coordination.

* **Emergence:** Cognition arises moment-by-moment through these coordinated actions.
* **Science of Interaction:** Rather than just a taxonomy of techniques (zoom, filter), InfoVis needs to understand how interaction enables the construction of meaning from visual structures.

---

## 6. Social and Contextual Visualization
The "one-person-one-computer" model is often an oversimplification.
* **Social Systems:** Data analysis is often collaborative. Insights are generated through the interaction of multiple people and shared artifacts.
* **Storytelling:** Projects like "Many Eyes" demonstrate how the web infrastructure allows representational states to propagate through social groups.

---

## 7. Methodological Approach: Cognitive Ethnography
To study the emergent properties of InfoVis, researchers should use **Cognitive Ethnography** rather than just lab experiments.

* **In Situ Fieldwork:** Observing actual users in their real environment to see how they develop coordinative strategies.
* **Analytic Strategy:** Focus on how meaning and understanding are constructed from interacting with external representations.
* **Complementary to Experiments:** Ethnography identifies the "how" and "why," which can then be tested via controlled experiments.

---

## 8. Critical Exam Takeaways: Redefining Evaluation
* **Usefulness vs. Usability:** Evaluation should focus on whether a system is **useful** (does it support the necessary cognitive processes?) rather than just **usable** (is it easy to click buttons?).
* **Negative Effects:** Poorly designed InfoVis systems can actually **destroy** current valuable practices by eliminating the possibility of performing certain epistemic actions (e.g., making notes on a paper margin).
* **Insight as Conceptual Change:** Insights are generated when a user’s internal representation undergoes a transformation due to coupling with an external visual structure.

---

## 9. Defining Quotes for the Exam
* "Cognition is more an emergent property of interaction than a property of the human mind."
* "The study of distributed cognition is very substantially the study of the variety and subtlety of coordination."
* "The purpose of visualization is insight, not pictures."

---

# Serpentine: A Reversibly Deformable Cord Sensor for Human Input
**Authors:** Fereshteh Shahmiri, Chaoyu Chen, Anandghan Waghmare, Dingtian Zhang, Shivan Mittal, Steven L. Zhang, Yi-Cheng Wang, Zhong Lin Wang, Thad E. Starner, and Gregory D. Abowd
**Source:** CHI 2019 Paper (Shahmirietal-Serpentine.pdf)

---

## 1. Abstract & Introduction
Serpentine is a self-powered, reversibly deformable cord sensor capable of sensing a variety of human inputs through mechanical deformation. It leverages the principle of Triboelectric Nanogenerators (TENG), allowing it to operate without an external power source for sensing.

* **Core Characteristics:** Flexible, twistable, stretchable, and squeezable.
* **Accuracy:** 95.7% for user-dependent realtime recognition; 92.17% for user-independent offline detection.
* **Design Philosophy:** Uses inexpensive, readily available materials to create a battery-free input device suitable for ubiquitous computing.

---

## 2. Operating Principles: Triboelectric Nanogenerator (TENG)
The sensor harvests energy directly from the physical deformation caused by human interaction. This is achieved via two primary TENG modes:

### A. Contact-Separation Mode (Touch)
* **Mechanism:** Occurs when a finger (dielectric) touches the outer silicone layer.
* **Physics:** Electrons transfer from skin to silicone (making silicone negatively charged). As the finger moves away, an outer electric field is induced.
* **Result:** To counterbalance this field, electrons flow between the nylon and copper electrodes, creating a detectable current.

### B. Lateral Sliding Mode (Stretching)
* **Mechanism:** Occurs when a longitudinal force is applied along the cylindrical axis (stretching).
* **Physics:** Friction occurs between the internal silicone dielectric and the PVA insulation of the copper wire.
* **Result:** The relative sliding of these layers generates a current between electrodes as the induced electric field is balanced.

---

## 3. Sensor Structure & Fabrication (The 5 Layers)
The cord is fabricated using a coaxial structure to maximize surface area contact and energy generation.

1. **Layer 1 (Inner Core):** Solid silicone rubber tube (2.5 mm diameter) made from a mix of Ecoflex 00-50 and PDMS (4:1 ratio).
2. **Layer 2 (Inner Electrode):** PVA-enamelled copper wire (0.17 mm) wound tightly around the core at 50 turns per centimeter.
3. **Layer 3 (Dielectric Coating):** A layer of silicone rubber solution applied to encapsulate the copper wire.
4. **Layer 4 (Outer Electrode):** Silver-plated nylon thread (0.18 mm) wound around the assembly at 50 turns per centimeter. Chosen for high tensile strength and puncture resistance.
5. **Layer 5 (Outer Encapsulation):** Final coating of silicone rubber. The completed sensor is approximately 4.5 mm in diameter.

---

## 4. Input Modalities (Six Primary Interactions)
The study defines six gestures inspired by the natural affordances of a cord:

1. **Double Pinch:** Squeezing the cord like clay.
2. **Twirl:** Like twirling hair around a finger.
3. **Pluck:** Like pulling and releasing a harp string.
4. **Stretch:** Extending the cord along its axis.
5. **Twist:** Rolling the cord between thumb and forefinger.
6. **Wiggle:** Rapidly moving the cord back and forth like a bell rope.

---

## 5. Data Processing & Machine Learning Pipeline
Serpentine uses a sophisticated software pipeline to classify gestures in real-time.

* **Acquisition:** Data collected via Digilent Analog Discovery 2 oscilloscope.
* **Segmentation:**
  * *Stage 1:* Energy-based sliding window (1s long, 50% overlap) detects the start/end of a gesture.
  * *Stage 2:* Finer refinement using a moving average; points below the 60th percentile of magnitude are ignored.
* **Feature Extraction:**
  * Calculated over a 40-sample window.
  * Features include: Zero crossing rate, spectral centroid, spectral flux, spectral rolloff, Hilbert wavelet transform, and Haar wavelet.
  * Statistical features (mean, std dev, skew, kurtosis) are added to normalize varying interaction lengths.
* **Classifier:** Random Forest machine learning model.
* **Latency:** Approximately 2.5 seconds for sensing and recognition.

---

## 6. Evaluation & Results

### Quantitative Findings
* **Most Reliable Gesture:** Pluck (100% accuracy).
* **Least Reliable Gestures:** Twist (88.3%) and Double Pinch (95%).
* **Confusion Point:** Users often performed Twists and Pinches similarly, leading to classifier confusion.
* **False Negatives:** 13 instances observed (mostly Twirl/Twist) when performed too fast or too gently.

### Qualitative Findings
* **User Favorites:** Stretch and Pluck were rated the most natural and "no-brainer" gestures.
* **Fatigue:** Twist and Double Pinch were reported as the most fatiguing and mentally demanding.
* **Social Context:** Users felt Twirl, Stretch, and Pinch were subtle enough for public use, while Pluck and large Wiggles were socially obtrusive.
* **Tactile Feel:** Participants described the cord as "bouncy," "squishy," and "fun to interact with."

---

## 7. Advanced Applications
1. **Wearable Control:** Hoodie strings used to control music (Twist = volume, Stretch = skip song, Pinch = play/pause). Waterproof nature allows for use in rain or underwater.
2. **Expressive Switch:** A lamp pull-cord where Stretching toggles power, Wiggling changes color, and Twirling adjusts brightness.
3. **Game Controller:** A tangible slingshot for Unity-based games where Pluck strength maps to projectile power.

---

## 8. Critical Exam Takeaways: Limitations & Future
* **Dynamic Only:** Serpentine only detects *changing* forces. It cannot detect a static state (e.g., if you hold the cord in a stretched position, the signal disappears).
* **Self-Powered Potential:** While currently used only for sensing, the energy generated could potentially power low-power wireless communication (e.g., analog backscatter).
* **Durability:** The sensor survived 30,000 loading cycles without loss of sensitivity.
* **Intensity Sensing:** The output signal amplitude is proportional to force, meaning future iterations could detect "how hard" someone pinches or pulls.

---