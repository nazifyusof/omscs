# 2.6

# Chapter 3 — Interaction Elements

## 3.4 Mental Models and Metaphor
**Author:** I. Scott MacKenzie  
**Publisher:** Morgan Kaufmann (Elsevier)

> Mental models (also called *conceptual models*) connect user experience to system behaviour, allowing users to leverage prior knowledge.

### What Are Mental Models?

- A mental model is a user's internal understanding of how a system works, built on **physical analogy or metaphor**
- Based on prior real-world experience; when a good model exists, interaction feels **natural and intuitive**
- The key question in HCI: *"What is the user's mental model of...?"*

### The Desktop Metaphor

- HCI's **first major mental model**: the office/desktop metaphor for GUIs
- Introduced in the **late 1970s to early 1980s** to ease users into unfamiliar graphical interfaces
- Exploited familiar concepts: documents, folders, filing cabinets, trashcans, drag-and-drop
- Reference: Johnson et al. (1989)

### Implementation Models — What to Avoid

- **Implementation models** force users to follow the *internal logic of the software*, not their own mental model
- Example (Cooper & Reimann, 2003): A software fax product that prompts users for technical details in the order convenient to the program, not the user
- **Rule:** Design should follow the *user's mental model*, not the program's internal structure

---

### Icons and Toolbars

- Toolbar buttons use **icons** (pictorial representations) instead of labels due to space constraints
- Icons should trigger a **mental image** linked to a real-world experience relevant to the button's action
- Some icons are intuitive (e.g., magnifying glass = zoom); others are not (e.g., "Picture Tube" in Paint Shop Pro)
- **Tooltips / Screen Tips**: introduced by Apple in **1991** as "balloons"
    - Hovering over a button pops up a brief description
    - Compensates for unclear icons

> "Each user learns the smallest set of features that he needs to get his work done, and he abandons the rest." — Cooper (1999, p. 33)

---

### Compass and Clock Metaphors for Direction

#### Compass Metaphor
- Leverages users' ingrained understanding of compass directions (N = up/forward, W = left, etc.)
- HCI example: **Lindeman et al. (2005)** — vibro-tactile belt with 8 actuators placed at compass positions
    - Users navigated a virtual building using compass mental model
- Also used in **pie menus** (Callahan et al., 1988) and **marking menus** (Kurtenbach, Sellen & Buxton, 1993; Li et al., 2005)

#### Clock Metaphor
- Provides **finer granularity** than compass (12 divisions vs. 8)
    - Common expression: "obstacle at 2 o'clock"
- HCI uses:
    - **Numeric entry with a stylus** (McQueen, MacKenzie & Zhang, 1995; Goldstein et al., 2000; Isokoski & Käki, 2002)
        - Numbers entered by stroke direction corresponding to clock position
        - 12 o'clock = 0; 10 & 11 o'clock = system commands
        - Result: **24% faster** than handwritten digits
    - **Locating objects/people** (Sáenz & Sánchez, 2009; Sellen et al., 2006)

---

### Case Studies: Navigation Aids for the Blind

#### Sáenz & Sánchez (2009) — Auditory Clock Metaphor System
- Mobile device providing **spoken audio** about nearby object locations
- Uses clock metaphor (user faces 12 o'clock); e.g., *"door at 3 o'clock"*
- Enabled **eyes-free building navigation**
- **Limitation:** Evaluation was *not experimental*
    - No independent or dependent variables defined
    - Used qualitative questionnaire only (e.g., "The software was motivating")
    - Missed opportunity for empirical measurement of speed, accuracy, error rates

#### Rümelin et al. (2012) — NaviRadar (Tactile Feedback)
- Uses **vibro-tactile pulses** instead of audio for direction cues
- Pulse combinations encode direction:
    - Two short pulses = straight ahead
    - Three short pulses = behind user
    - Longer 1st pulse = farther left; longer 2nd pulse = farther right
- Avoids auditory feedback (useful in noisy environments)
- **Strength:** Took a fully **empirical approach**
    - Independent variables: pulse intensity, duration, rhythm
    - Dependent variables: deviation between indicated and reported directions
    - Enables replication and systematic improvement by other researchers

---

### Empirical vs. Non-Empirical Evaluations — Key Distinction

| Aspect | Sáenz & Sánchez (2009) | Rümelin et al. (2012) |
|---|---|---|
| Evaluation type | Qualitative / non-experimental | Empirical / experimental |
| Independent variables | None defined | Pulse intensity, duration, rhythm |
| Dependent variables | None defined | Direction deviation accuracy |
| Generalisability | Low | High |
| Utility for future research | Limited | Enables comparison and improvement |

> Qualitative assessments are an **essential** component of evaluation, but navigation/locating systems are well suited to **experimental testing** for richer, actionable insights.

---

## Key Terms

| Term | Definition |
|---|---|
| **Stimulus-response compatibility** | Degree to which control movement naturally maps to display response |
| **Population stereotype** | A culturally learned convention accepted by most in a region |
| **Mental model / Conceptual model** | User's internal understanding of a system based on prior experience |
| **Implementation model** | System design that follows internal program logic rather than user expectations |
| **Icon** | A pictorial representation on a button or tool that triggers a mental association |
| **Tooltip / Screen tip** | A popup description that appears when hovering over a GUI element |
| **Physical analogy** | A real-world spatial relationship that maps directly onto an interface interaction |

---

## 3.8 Interaction Errors
**Author:** I. Scott MacKenzie  
**Publisher:** Morgan Kaufmann (Elsevier)

> "Human performance is like food, while physical properties are like plates and bowls. It is good and nutritious food that we strive for."

### Overview

- Most HCI analysis focuses on **physical properties** of the interface (degrees of freedom, spatial/temporal relationships between inputs and outputs)
- But ultimately, **human performance is what counts** — physical properties are secondary
- Empirical HCI research seeks to find the physical properties and combinations that **improve and enhance human performance**
- **Errors only hinder** — unlike task time (which can enhance or hinder by degree), errors are purely negative
- The **absence of errors is invisible**; errors are what users notice and feel

### The Error Landscape

- Common view: difficult desktop problems are solved; focus should shift to new frontiers (mobile, ubiquitous computing, social networking, gaming)
- **Reality:** Desktop computing is still full of problems — many small, persistent ones
- Four errors are examined, ordered by a progression from **high severity / low frequency → low severity / high frequency**

---

### The Four Interaction Errors

#### Error 1 — Discard Changes Dialog (High Cost, Low Frequency)

- Classic example of a **serious UI design flaw**
- Two similar-looking dialogs: *"Save changes?"* vs. *"Discard changes?"*
    - Pressing Enter on "Save changes?" → safe
    - Pressing Enter on "Discard changes?" → **data is permanently lost**
- Root cause: **broken user expectation** — users act without reading carefully when they expect a consistent dialog
- Fix: Standardise on "Save changes?" dialog across all applications
- **Current status:** Largely resolved in modern desktop applications — consistent "Save changes?" dialog is now the norm
- Reference: Cooper (1999, p. 14)

> Broken expectations sooner or later cause errors.

#### Error 2 — CAPS_LOCK During Password Entry (Medium Cost, Low-Medium Frequency)

- When `CAPS_LOCK` is active, password entry fails silently — the user may not know why
- Repeated failed attempts can **lock the account**
- This is a **design flaw**, not a user error — easily correctable with a few lines of code
- Many systems now show a `CAPS_LOCK` warning alert; others still do not
- **Current status:** Improving, but inconsistent across systems

#### Error 3 — Scrolling Frenzy / Position-to-Velocity Control Shift (Medium Cost, Medium Frequency)

- When dragging selected text that extends past the viewable region:
    - **Inside** viewable region → **position-control** (mouse displacement = dragging position)
    - **Outside** viewable region → **velocity-control** (mouse displacement = dragging speed)
- This transition is **abrupt and unpredictable**
    - In some applications, scrolling is so fast the selection reaches the end of the document in **~200 ms** (faster than the user can react)
    - In others, scrolling is uselessly slow
- The user experience breaks down — interaction degrades to **error recovery**
- This is a **design-induced error**: the user did nothing wrong
- **Current status:** More controlled in newer applications, but still inconsistent

#### Error 4 — Focus Uncertainty (Low Cost, High Frequency)

- **Focus** = which UI component is currently active and receives keyboard input
    - Buttons: indicated by a dashed border
    - Input fields: indicated by a flashing insertion bar (`|`)
- **Focus advancement** = progression of focus from one UI component to the next
- **Problem:** Wide inconsistency in how and when focus advances
    - Example: login dialog — sometimes you can type immediately; sometimes you must click the field first
    - Example: multi-segment account number fields — does focus auto-advance after each segment? Users don't know
- User is forced to remain **"on guard"** — attention is diverted from the task to monitoring the system
- Every attention shift = **two gaze shifts (saccades)**, each taking 70–700 ms (Card et al., 1983)
- **Current status:** Still a mess — the most frequent and least-fixed of the four errors

> "The user is like a wood carver who sharpens tools rather than creates works of art."

---

### Design-Induced Errors

- Small errors are often incorrectly labelled as **user errors**
- More accurately, they are **design-induced errors** (Casey, 2006, p. 12)
- Defined as errors that occur when designers fail to account for human characteristics, capabilities, and behaviours (Casey, 1998, p. 11)
- Little errors tend to linger because:
    - Their consequences are minor (extra click, gaze shift)
    - They are not on designers' or programmers' radar
    - Programmers prioritise **feature checklists** over subtle UX refinements
    - **Programmers' discretion** often drives interaction design by default (Cooper, 1999, p. 47)

---

### Cost vs. Frequency of Errors (Figure 3.46)

| Error | Cost | Frequency | Status |
|---|---|---|---|
| Discard changes | High | Low | Largely resolved |
| CAPS_LOCK | Medium | Low–Medium | Improving |
| Scrolling frenzy | Medium | Medium | Much improved in new apps |
| Focus uncertainty | Low | High | Still widespread |

> High-cost errors get attention and get fixed. Low-cost, high-frequency errors slip past — they are the most interesting research opportunities.

---

### Microstrategies

- User experiences are built from **collections of microstrategies** — fine-grained, moment-to-moment interactions
- Reference: Gray & Boehm-Davis (2000, p. 322) — subtle features of interactive technology influence how users perform tasks
- Every unnecessary gaze shift, hesitation, or guard moment is a microstrategy **imposed on the user by the system**
- **Design goal:** Minimise unnecessary microstrategies so users focus on their task, not on managing the computer

---

### Key Terms

| Term | Definition |
|---|---|
| **Design-induced error** | An error caused by poor design that fails to account for human behaviour, mistakenly attributed to the user |
| **Position-control** | Input displacement maps to output *position* |
| **Velocity-control** | Input displacement maps to output *speed* |
| **Focus** | The active UI component that receives keyboard input |
| **Focus advancement** | The movement of focus from one UI widget to the next |
| **Saccade** | A rapid eye movement between fixation points; takes ~30 ms for movement, longer for fixation/processing |
| **Microstrategy** | A fine-grained user action or attention allocation during interaction |

---

# Chapter 5 — Human Error? No, Bad Design
**Author:** Don Norman  
**Chapter:** Five — Human Error? No, Bad Design

> "Most industrial accidents are caused by human error: estimates range between 75 and 95 percent. How is it that so many people are so incompetent? Answer: They aren't. It's a design problem."

## 5.1 Understanding Why There Is Error

### The Core Argument

- Industrial accidents attributed to human error: **75–95%**
- Norman's position: when error rates are this high, the system and design are responsible — not the people
- Physical limitations in users are well understood by designers; **mental limitations are grossly misunderstood**
- The correct response to error: **find the fundamental cause and redesign** the system — not blame and punish

### Common Causes of Error

- Tasks that require **unnatural behaviour**: sustained alertness for hours, precise input, multitasking
- **Interruptions** — a major, under-addressed root cause
- **Time stress** — pressure not to slow down processes in manufacturing, hospitals, commercial operations
- **Attitudes toward error** — blame-and-punish culture prevents systemic improvement

### Deliberate Violations

- Not the same as errors — violations are **intentional** deviations from known proper behaviour
- Types:
    - **Routine violations** — noncompliance so frequent it is ignored
    - **Situational violations** — special circumstances justify bending the rule
- Often occur because rules are written for **legal compliance**, not real work requirements
- When violations succeed, workers are often rewarded → **unwittingly reinforces noncompliance**
- Deliberate violations are outside the scope of design-level error analysis (they are organisational/societal issues)

---

## 5.2 Root Cause Analysis

> "Root cause analysis is the name of the game: investigate the accident until the single, underlying cause is found."

### Problems with Conventional Root Cause Analysis

- Most accidents have **multiple causes** — no single root cause
- Analysis typically stops as soon as a **human error** is found, which is too shallow
- If a machine breaks, we ask *why did the part break?* — we should ask the same about human failures

### The Five Whys (Toyota)

- Developed by **Sakichi Toyoda**, used in the **Toyota Production System**
- Principle: after finding a reason, keep asking *why* until the true underlying cause is found
- Does **not guarantee** success — can lead different investigators to different answers
- Powerful nonetheless as a tool against premature conclusion

### The F-22 Crash Example

| Question | Answer |
|---|---|
| Why did the plane crash? | Uncontrolled dive |
| Why didn't the pilot recover? | Failed to initiate timely recovery |
| Why was that? | Possibly unconscious / oxygen deprived |
| Why was that? | Unknown — needs investigation |

- Air Force stopped at "pilot error"; Inspector General correctly pushed further
- Lesson: **human error in the chain is the beginning of the analysis, not the end**

---

## 5.3 Two Types of Errors: Slips and Mistakes

> Developed by Norman and British psychologist **James Reason**.

### Definitions

| Term | Definition |
|---|---|
| **Human Error** | Any deviance from "appropriate" behaviour |
| **Slip** | Goal is correct, but the action performed is wrong — execution is flawed |
| **Mistake** | The goal or plan itself is wrong — even correct execution produces an error |

### Where They Occur in the Seven Stages of Action

- **Slips** → lower stages (Perform, Perceive, Interpret, Specify)
- **Mistakes** → higher stages (Goal, Plan, Compare/Evaluate)
- **Memory lapses** → at the *transitions* between any stages (can produce either slips or mistakes)

---

## 5.4 Classification of Slips

> Slips occur more frequently in **skilled/expert users** than novices — because experts act automatically and pay less conscious attention.

### Action-Based Slips

#### Capture Slips
- A **more familiar or recently performed action** hijacks the intended action
- Requires that the two action sequences share **identical opening steps**, diverging later
- At the divergence point, if attention lapses, the familiar sequence takes over
- Example: counting pages but switching to "Jack, Queen, King" after recently playing cards
- **Design implication:** avoid procedures with identical opening steps — make sequences **differ from the very start**

#### Description-Similarity Slips
- Acting on the **wrong object** because its description is too vague to distinguish it from the target
- More likely when tired, stressed, or overloaded; more objects present = higher error risk
- Example: throwing a sweaty shirt into the toilet instead of the laundry basket (both are "containers")
- **Design implication:** controls and displays for different functions must be **visually and physically distinct** — e.g., shape-coded aircraft controls (throttle vs. flap vs. landing gear)

#### Mode-Error Slips
- Occur when the **same control has different meanings in different modes**
- Inevitable when devices have more functions than controls (e.g., smartphones, aircraft autopilot)
- Dangerous because the operator may not know which mode is active
- Example: Airbus accident — pilots entered –3.3 intending angle of descent (–3.3°) but system was in vertical speed mode (–3,300 ft/min → fatal crash)
- **Design implication:** make modes **visible and distinct**; eliminate unnecessary modes where possible

### Memory-Lapse Slips
- The intended action is **simply not performed** — nothing to see, nothing to detect
- Immediate cause: **interruptions** between deciding to act and completing the action
- Examples: walking away from a photocopier without the original; forgetting a child at a rest stop; leaving an ATM card in the machine
- **Design solutions:**
    - Minimise number of steps
    - Provide vivid reminders
    - Use **forcing functions** (e.g., ATM dispenses money only after card is removed)

---

## 5.5 Classification of Mistakes

> Mistakes arise from **conscious deliberation** — the same cognitive strengths that make us creative also make us prone to overgeneralisation.

### Rasmussen's Three Levels of Behaviour (Danish engineer Jens Rasmussen)

| Level | Description | Error Type |
|---|---|---|
| **Skill-based** | Routine, expert, automatic behaviour | Slips |
| **Rule-based** | Applying known rules to a familiar abnormal situation | Mistakes or slips |
| **Knowledge-based** | Novel situation — conscious problem-solving required | Mistakes |

### Rule-Based Mistakes
- Wrong rule selected, OR the rule itself is flawed, OR the outcome is incorrectly evaluated
- Driven by memory — we match current situations to past experiences, with biases toward **recency, regularity, and uniqueness**
- Example: Kiss nightclub fire (Brazil, 2013) — guards blocked exits following a rule that didn't account for emergencies; band used indoor-unsafe pyrotechnics
- Example: driver lifts foot off brake when anti-lock brakes vibrate, mistaking normal function for malfunction
- **Design response:** display system state clearly and graphically; provide decision support

### Knowledge-Based Mistakes
- Novel situation with no applicable skill or rule → **slow, conscious problem-solving**
- Best addressed through **good conceptual models** and, in complex cases, AI-assisted decision support
- Current limitation: automation tends to fail precisely when knowledge-based decisions are most needed

### Memory-Lapse Mistakes
- Forgetting the goal or plan entirely (not just a step) — often due to interruptions
- **Design cure:** keep goals, plans, and system state continuously visible; design for resumption after interruption

---

## 5.6 Social and Institutional Pressures

> "Never underestimate the power of social pressures on behaviour, causing otherwise sensible people to do things they know are wrong and possibly dangerous."

### Key Cases

- **Tenerife disaster (1977):** KLM 747 took off without clearance; 583 killed. Causes: time pressure, economic pressure, weather, cultural authority gradient between captain and first officer
- **Air Florida crash (1982):** Took off with ice on wings despite first officer's four warnings; captain took no corrective action — social authority gradient + time pressure

### Implications for Design
- Good design alone is insufficient — we need **training cultures that reward safety** over speed
- Equipment should make **potential dangers explicit and visible**
- Address cultural authority gradients: **junior staff must be empowered to halt unsafe actions**

---

## 5.7 Checklists

> "Checklists are powerful tools, proven to increase the accuracy of behaviour and to reduce error, particularly slips and memory lapses."

- Especially valuable in **complex, multi-step, interruption-prone** tasks
- Best done **collaboratively** — one reads, one executes — not sequentially by a single person
- **Paradox of groups:** adding more checkers can reduce thoroughness (everyone assumes others will catch errors)
- Medical professionals have historically resisted checklists — seen as an insult to competence
- In commercial aviation, checklists are **mandatory** — it took decades to achieve this acceptance
- **Flaw of printed checklists:** force sequential ordering; can lead to skipped items
- **Advantage of electronic checklists:** can track skipped items and prevent marking as complete until all steps done

---

## 5.8 Reporting Error

- Errors that are **reported** can be prevented from causing harm
- Social and institutional barriers to reporting: fear of punishment, embarrassment, liability
- **The correct attitude:** thank those who report errors; gather data; use it to redesign

### Toyota Jidoka
- Workers are expected and required to report errors — even stopping the assembly line (via the *andon* cord)
- Root cause is then investigated using the Five Whys
- Failure to report is punished — a culture of radical transparency

### Poka-Yoke (Shigeo Shingo)
- Translates as **"error proofing"** or "avoiding error"
- Technique: add physical fixtures, jigs, or constraints that make incorrect actions impossible
- Examples: asymmetric screw holes (part fits only one way), fluid reservoir openings of different sizes/shapes, covered emergency switches
- Combines **affordances, signifiers, mapping, constraints, and forcing functions**

### NASA Aviation Safety Reporting System
- Pilots submit **semi-anonymous** reports of errors they made or observed
- NASA detaches identifying info after collecting it → FAA cannot punish the reporter
- Sufficient similar reports → NASA analyses and issues recommendations to airlines and FAA
- Medicine lacks an equivalent — physicians fear licence loss or lawsuits

---

## 5.9 Detecting Error

| Error Type | Detectability | Reason |
|---|---|---|
| Action slips | Relatively easy | Discrepancy between intended and actual act is visible — if feedback is present |
| Memory-lapse slips | Difficult | Nothing is done, so nothing to see |
| Mistakes | Difficult | Actions are consistent with the wrong goal — correct execution gives false confidence |
| Memory-lapse mistakes | Especially difficult | Entire plan forgotten; absence harder to detect than presence |

### Explaining Away Mistakes

- Once people find a plausible explanation for an anomaly, they discount it
- Most major industrial accidents are **preceded by warning signs** that were individually explained away
- **Hindsight bias** (Baruch Fischhoff): after an event, the outcome seems obvious and predictable; during the event, operators face overwhelming, ambiguous information
- Best accident analyses take time — investigators must reconstruct the operators' viewpoint, not impose post-hoc clarity

---

## 5.10 Designing for Error

### Design Principles

- **Understand causes** of error and design to minimise them
- **Sensibility checks** — does the action pass a common-sense test? (e.g., flagging a medication dose 1000× the normal amount)
- **Make actions reversible** — Undo command is one of the most powerful error-reduction tools
- **Make errors less costly** — avoid situations where one action causes irreversible widespread damage
- **Make errors discoverable** — provide clear, perceptible feedback; show system state
- **Treat actions as approximations** — help the user complete the intended action, don't just issue error messages

### Confirmation and Error Messages

- Confirmation dialogs are often **ill-timed** — user is already committed to the action and confirms without reading
- More effective: **prominently display both the action AND the object** being acted on
- Against slips: confirmations can help (user is surprised by the dialog)
- Against mistakes: confirmations often fail (user expected the dialog and confirms automatically)

### Interruptions

- A **major source** of slips and memory-lapse errors
- Cost of interruption = time of interruption + cost of **resuming** the interrupted task
- FAA "Sterile Cockpit Configuration": pilots may only discuss flight-related topics during takeoff and landing
- Multitasking is **not efficient** — evidence shows severe performance degradation and increased errors

### Warning Signals

- Often **not the answer** — especially in environments already flooded with alarms (nuclear plants, cockpits, hospitals)
- Operators cope by **disabling warnings** — creating new hazards
- Effective warnings must: attract attention, convey the nature of the event, and be coordinated across instruments

---

## 5.11 The Swiss Cheese Model (James Reason)

> Most errors do not cause accidents — accidents require **multiple failures to align simultaneously**.

- Each "slice of Swiss cheese" = a defence layer or system condition
- Holes in the cheese = vulnerabilities or failures
- An accident occurs **only when holes in all slices line up** — a rare convergence
- Well-designed systems have many layers (slices) and few/small holes → **resilient against individual failures**

### Design Implications

- **Add more slices** → more defensive layers (e.g., checklists, dual-person verification)
- **Reduce hole size** → better-designed equipment and procedures reduce slip/mistake opportunities
- **Alert operators** when multiple holes are aligning

### "If Only" Statements

- Every accident can be traced to some action that, if different, would have prevented it
- But this does not mean that action was **the** cause — all factors must align
- Reputable investigators (e.g., NTSB) reject the single-cause narrative — their job is to understand the **system**

---

## 5.12 The Paradox of Automation

- Automation handles **dull, repetitive tasks** well → reduces errors and fatigue in normal conditions
- But automation **fails without warning** and often during the most complex situations — exactly when it is most needed
- When automation fails, the human is **"out of the loop"** — no longer monitoring, slow to detect and respond
- Example: Royal Majesty cruise ship (1997) — GPS disconnected silently; navigation switched to dead reckoning; ship ran aground on Cape Cod after days of unnoticed drift
- Human + machine should be treated as a **collaborative system**, not a division of labour

---

## 5.13 Resilience Engineering

- Goal: design systems (equipment, procedures, management, training) to **respond effectively to problems as they arise**
- Treats safety as a **core value**, not a count of errors
- Key practice: deliberately cause failures in systems to test backup systems and redundancies
- Resilience is measured by the ability to **anticipate changing risk** before failure occurs
- Reference: Hollnagel, Woods & Leveson (2006)

---

## 5.14 Key Design Principles for Error

- Put **knowledge in the world** — don't require it all to be in the head
- Use **natural and artificial constraints** — physical, logical, semantic, cultural
- Apply **forcing functions** and natural mappings
- Bridge the **Gulf of Execution** (feedforward — make options visible) and **Gulf of Evaluation** (feedback — make results clear)
- Assume every possible mishap **will** happen — design to protect against it

---

## Key Terms

| Term | Definition |
|---|---|
| **Slip** | Error where the goal is correct but the action is wrong (execution failure) |
| **Mistake** | Error where the goal or plan itself is wrong |
| **Capture slip** | A familiar action sequence hijacks the intended one at a shared step |
| **Description-similarity slip** | Correct action performed on the wrong, similar-looking object |
| **Mode error** | Error caused by a control having different meanings in different modes |
| **Memory-lapse slip** | An intended action is simply not performed due to forgetting |
| **Root cause analysis** | Systematic investigation to find the deepest underlying cause of an incident |
| **Five Whys** | Toyota technique: keep asking "why?" until the root cause is found |
| **Swiss cheese model** | Reason's model: accidents require multiple system failures to align simultaneously |
| **Poka-yoke** | Japanese technique for error-proofing through physical constraints |
| **Jidoka** | Toyota philosophy of stopping work to signal and fix problems at the source |
| **Resilience engineering** | Design paradigm focused on systems' ability to anticipate and recover from failure |
| **Design-induced error** | An error caused by poor design that is mistakenly attributed to the user |
| **Hindsight bias** | Tendency to view past events as predictable after the fact |
| **Deliberate violation** | Intentional deviation from known proper procedure — distinct from errors |

---

# 2.7

---

# GOMS, Distributed Cognition, And The Knowledge Structures Of Organizations
**Authors:** Robert L. West, Alan Wong, Alonso H. Vera  
**Institution:** Department of Psychology, University of Hong Kong  
**Type:** Academic Paper

---

# Overview

> "GOMS can be used to model HCI tasks within the relevant contextual aspects of organizations, such as companies and institutions."

- **Central argument:** GOMS — originally designed for individual human-computer interaction — can be extended to model entire organisations as **distributed cognitive systems**
- Responds to Mantovani (1996)'s critique that HCI lacks an integrated model of social context
- Authors' position: the social context problem is not that existing tools are inadequate, but that researchers have not applied them broadly enough

---

# What is GOMS?

> Developed by Card, Moran & Newell (1983). Designed to capture how **experts** execute **well-learned, routine tasks**.

## Components

| Component | Description | Example |
|---|---|---|
| **G — Goals** | What the user wants to achieve | "Look up a Chinese character" |
| **O — Operators** | Atomic actions (physical, perceptual, or cognitive) | Move mouse, search screen, add two numbers |
| **M — Methods** | Combinations of sub-goals and operators used to achieve a goal | A sequence of steps to save a file |
| **S — Selection Rules** | Rules for choosing between competing methods | "If the file is large, use method B" |

## Types of Operators
- **Physical** — e.g., move the mouse, press a key
- **Perceptual** — e.g., search the screen, read a display
- **Cognitive** — e.g., add two numbers, recall a procedure

## Key Properties
- Originally modelled **individual** users, but the **unit of analysis is flexible**
- Can describe a single person OR an entire room of humans and computers
- Works at the **knowledge level** — granularity depends on research goals
- Has since been improved to account for: learning, errors, working memory limits, parallel processing (Olson & Olson, 1990)

---

# Extending GOMS to Organisations

## Organisations as Distributed Cognitive Systems
- Organisations involve high amounts of **routine, well-learned activity** — exactly what GOMS models best
- Social and cultural rules mediating interpersonal relationships within organisations are also **routine in nature**
- Therefore, GOMS can describe the **knowledge level** of organisational systems, including the knowledge structures behind social interactions

> A social interaction is defined as any interaction between two or more people.

## Advantages of Using GOMS at the Organisational Level

1. **Well-established tool** — large body of studies demonstrating its application to specific problems
2. **Common modelling language** — cross-disciplinary work (cognitive science, social psychology, game theory, sociology, anthropology) can share a single accessible framework
3. **Compatibility** — organisational GOMS models are compatible with existing GOMS models of specific sub-tasks within that organisation
4. **Specific outputs** — can address time estimates, resource efficiency, goal conflicts, goal fulfilment, and organisational robustness

---

# Modelling Social Actions

## Two Broad Types of Social Actions (from the individual's perspective)
1. **Actions relating to other individuals** — e.g., "Do I trust this person?"
2. **Actions relating to groups** — e.g., "Will the market go up?"

## Social Operators
- Can be modelled using mechanisms from social psychology
- Example: Fishbein & Ajzen's (1974) **reasoned action theory** can predict attitudes toward alternative actions
- Gut-level decisions can be modelled using **Damasio's Somatic-Marker Hypothesis** (1994)
- Can also be represented using AI models such as **ACT-R** (Anderson, 1993) or **SOAR** (Newell, 1990)

## Level of Abstraction
- Operators do not need to be limited to simple button presses
- Any process can be made into an operator — e.g., an architect calling an operator to judge **aesthetic quality**
- The output of a complex operator can serve as a **selection rule** (e.g., if aesthetic → continue drawing; if not → discard)
- The key is finding the **most useful level of abstraction** for the task being modelled

## GOMS as a Model of Social Thought
- When predicting what another person will do, individuals may construct something very much like a **GOMS model of that person** and mentally simulate it
- This mirrors how intelligent software agents use GOMS to predict user behaviour (Vera & Rosenblatt, 1995)

---

# The Importance of Goals

## Individual Goals within Organisations
- Standard GOMS implicitly assumes the user's highest goal is to **do the task as well as possible**
- Must ask: *why does the employee want to complete the task?*
    - Usually: payment, avoiding dismissal → goal hierarchy need go no higher
    - Sometimes: more complex higher-level goals determine what tasks are chosen

## Organisational Goals vs. Individual Goals
- Organisations have stated goals (e.g., "create a clean environment")
- But individuals can work within an organisation **without adopting its higher-level goals**
- Key question: does the structure of the organisation cause individual goals to **collectively result** in the organisation's stated goal?
- Especially important for governmental and public service organisations
- GOMS can provide a **process model** of how goals such as institutionalised racism emerge — because goals are triggered by a clear chain of higher-level goals and selection rules

---

# Top-Down Effects of Goals

## The Core Debate
- Mantovani (1996): even simple actions like shoe-tying are shaped by social/cultural context — they cannot be treated in isolation
- Traditional cognitive science / GOMS position: simple actions **can** be treated in relative isolation
    - The process of shoe-tying remains essentially constant regardless of whether it serves a run in the park, a night at the opera, or overthrowing a dictatorship
    - Any effects of social context on low-level operators are **mediated by basic cognitive variables** (memory load, attention, speed-accuracy tradeoffs)

## Authors' Position
- Low-level operators (e.g., clicking a mouse) are **generally unaffected** by higher-level social/cultural goals
- When they are affected, the effect is mediated by well-defined variables: **memory load, attention demands, stress**
- Same applies to social operators — for the most part unaffected by higher-level goals, but when they are, mediation is through a **limited number of variables**

## Practical Application
- Attach an **index** to each employee to track cognitive/social variables (e.g., stress, memory load) at each step
- This is useful in systems where human error can have serious consequences

---

# Spin-Off Effects

> Evaluating methods solely in terms of how they satisfy the **immediate goal** may miss important effects on **other goals** elsewhere in the system.

## Example: Chinese-English Dictionary HCI
- Initial highest-level goal: look up a Chinese character and find its meaning
    - Generated high-tech suggestions (neural network character recognition)
- Actual higher-level goal of users: **learn to read Chinese**
    - Led to the conclusion that the traditional **radical search method** was better
    - Reason: parsing characters into pictographic components aids character recognition — the learning process is embedded in the lookup process
- **Lesson:** A GOMS model of the broader organisation makes spin-off effects discoverable

---

# Reactivity to the Environment

- Traditional GOMS assumes a **pristine task environment** — no unrelated interruptions
- In social/organisational settings, users **are** interrupted and information is injected that alters the task

## Two Aspects of GOMS Modelling Relevant to Reactivity

1. **Goal stack depth** — a *shallow* goal stack increases reactivity by allowing the system to more frequently check the environment between executing goals
2. **Level of abstraction of operators** — operators defined at a gross level of granularity overlook interruption opportunities

## CPM-GOMS Approach
- **CPM-GOMS** (Gray, John & Atwood, 1993) uses a **schedule chart** to represent simultaneously occurring activity
- Analysed using **critical path analysis**
- Allows the environment to be monitored **in parallel** while other tasks proceed
- Example: an engineer waiting for plans works on a side task while monitoring for news that plans have arrived

---

# Case Study: Satellite Maneuver Operations

## Context
- Satellite technicians (STs) perform **attitude maneuvers** — routine but requiring high environmental reactivity
- STs must attend to both the computer interface and to each other
- Task occurs within a larger satellite management organisation

## Method
- Unobtrusive observation of maneuvers
- Data sources: task manual, checklists, handbooks, post-mission interviews
- All STs fully trained, average 6 months job experience

## The Seven Tasks of an Attitude Maneuver

1. **Configure system** — call up the semi-automated program (batches of commands and instructions)
2. **Prepare for phase check** — select data channels, switch on printer, refill paper
3. **Execute phase check** — synchronise with satellite; specify parameters; start printer; chart time-graph
4. **Prepare maneuver** — specify execution time; switch off automated notation control and antenna pointing
5. **Execute maneuver** — fully automated; printer must start 10 seconds before execution
6. **Finish maneuver** — check data; return spin rate and temperature to normal; restore automated systems
7. **Attend alarm** — alarms can occur at any time; each must be acknowledged and analysed before continuing

## Key Observation: Interface-Driven Reactivity
- STs' actions were **intimately dependent on cues from the computer interface** (primarily the monitor screen)
- Although the task appeared retrospectively as a large serial plan, STs were actually **highly reactive** to environmental cues
- Evidence:
    - STs constantly referred to monitor screens
    - STs waited for external cues before acting
    - When alarms interrupted, STs completed the current sub-goal, dealt with the alarm, then looked to the interface to resume

## Modelling Strategy: Shallow Goal Stacks
- Used **very shallow goal stacks** prompted by system cues
- Example: perceiving the cue "APE to manual" pushes the sub-goal of turning off the antenna pointing system
- Each unit task consists of only **two operators**: "enter command" and "verify command"
- This allows STs to frequently return to monitoring the environment

## Limitations of the Cue-Only Model
- Some sub-goals were **not cued by the interface** (e.g., turn on printer, collect data, select data channels)
    - In one observed instance, STs forgot to run the printer → procedure had to be repeated
- STs were also found to have **knowledge of the expected sequence** — an unexpected or missing cue signals a problem
- Solution: model assumes STs maintain a **knowledge structure of the sub-goal sequence**; interface cues are **verified against this structure** — conflict triggers problem-solving behaviour

---

# Three Levels of Analysis

| Level | Description | Focus |
|---|---|---|
| **1. The room as a distributed cognitive system** | Functional description without distinguishing agents | What gets done |
| **2. Computers vs. STs (including non-computerised reference material)** | Interaction between human and computer distributed systems | HCI characteristics |
| **3. Individual STs interacting with manuals, checklists, and interface** | Flow of information around the room | Knowledge sources and transfer |

- Task knowledge is **distributed** across STs and computer systems, with some **redundancy**
- In practice: supervisor + two operators (one executes commands, one verifies)
- Knowledge drawn from: long-term memory, system cues, job manuals, checklists, and other STs

---

# Social Actions in the Satellite Case

- Social interactions among STs were **highly constrained** by task demands and organisational policy
- Behaviour is very routine → can be captured at a fairly detailed level using GOMS
- Role allocation (who executes, who verifies) is modelled as an **operator** attached to the distributed cognitive system of all three STs — the internal decision process is abstracted away
- Inter-departmental interactions (with control room and orbital engineers) are modelled at the **department level** — as distributed cognitive entities without reference to individual agents

---

# Conclusions

- GOMS can model large, interactive systems (organisations, institutions) by treating them as **distributed cognitive systems**
- Unlike social psychology (seeks general mechanisms) or sociology/anthropology (seeks general principles), GOMS provides a **specific, process-level knowledge description** of how a particular task is performed
- Considering organisational context gives a **broader picture of any HCI task** — increasingly important as organisations rely on computer networks rather than isolated PCs

---

# Key Terms

| Term | Definition |
|---|---|
| **GOMS** | Goals, Operators, Methods, Selection Rules — a modelling system for expert routine task performance |
| **Distributed cognition** | A framework in which cognitive processes are distributed across people, artefacts, and the environment (Hutchins, 1994) |
| **Distributed cognitive system** | A system (e.g., a room of humans and computers) that collectively possesses and applies expert knowledge |
| **Knowledge level** | The level of description focusing on what an agent knows and its goals, independent of physical implementation |
| **Spin-off effects** | Unintended consequences of a method on goals elsewhere in the system |
| **Reactivity** | A system's ability to respond to environmental changes and interruptions mid-task |
| **Goal stack** | The ordered list of goals currently being pursued; shallow stacks allow more frequent environment checks |
| **CPM-GOMS** | A variant of GOMS using schedule charts and critical path analysis to model parallel activity |
| **Social operator** | An operator representing a social action (e.g., "behave politely towards the customer") |
| **Selection rule** | A rule that determines which method to apply when multiple methods could achieve the same goal |

---

# 2.8

# How a Cockpit Remembers Its Speeds
**Author:** Edwin Hutchins  
**Source:** *Cognitive Science*, Vol. 19, pp. 265–288 (1995)  
**University of California, San Diego**

---

## Core Argument

> The cockpit — not the individual pilot — is the proper unit of cognitive analysis. The cognitive properties of distributed socio-technical systems cannot be reduced to the cognitive properties of the individuals within them.

- Classical cognitive science asks: how does the *individual* represent and process information?
- Hutchins extends this frame to a **larger unit of analysis**: the cockpit as a whole
- Many representations inside the cockpit system are *directly observable* (unlike internal mental states)
- Outcomes in aviation are produced by **systems**, not individuals alone

---

## Part 1: Background — Why Speeds Must Be Remembered

### The Problem of Wing Configuration and Speed

- Airliner wings are designed for fast flight; they cannot generate enough lift at low speeds without modification
- **Slats** (leading edge) and **flaps** (trailing edge) extend to change wing shape and increase lift coefficient
- Each flap/slat position = a **wing configuration**
- Each configuration has a **minimum maneuvering speed (MinMan)** — flying below this risks a stall
- As the plane slows for landing, crews must extend flaps/slats *in coordination* with decreasing airspeed

### Vref — The Reference Speed

- **Vref** = the target speed for the final approach and landing
- Must be slow enough to be ready to stop flying on touchdown, fast enough to maintain control
- Precise speed control at Vref is essential to safe landing

### Weight Dependency

- All MinMan speeds and Vref vary with **gross weight** of the aircraft
- This makes the task complex — there is no single fixed set of speeds

### Crew Division of Labor

| Role | Responsibility |
|------|----------------|
| **PF** (Pilot Flying) | Controls the airplane |
| **PNF** (Pilot Not Flying) | ATC communication, checklists, aircraft systems |

> Computing and setting approach speeds is a "killer" item — failure to do so can cause fatal accidents.

---

## Part 2: Three Descriptions of Memory for Speeds

### Description 1 — Procedural (What Pilots Do)

#### Prepare Landing Data (~25–30 min before landing)
1. Determine gross weight (displayed on fuel quantity indicator)
2. Select the matching **speed card** from the speed card booklet
3. Post the speed card visibly in the cockpit
4. Set **speed bugs** on both Airspeed Indicators (ASIs) to match the card

#### Speed Card (MD-80 example, 122,000 lbs)
- 0/RET MinMan → 227 kts
- 0/EXT MinMan → 177 kts
- Flaps 11 → 155 kts
- Flaps 15 → 152 kts
- Flaps 28 → 142 kts
- Flaps 40 → 137 kts
- Vref 28/EXT → 132 kts
- Vref 40/EXT → 128 kts

#### The Descent
- Below 10,000 ft: must slow to ≤250 KIAS (traffic separation requirement)
- At ~7,000 ft AFL: begin slowing to speeds requiring slat/flap extension
- Flaps/slats must be extended *near* MinMan speed — not early — to minimize air loads

#### The Final Approach
- Checklist item: *"Flight instruments and bugs / Set and cross-checked"*
- Both pilots cross-check their own ASI bugs against each other's ASI and the speed card
- At 500 ft AFL: PNF calls altitude, airspeed deviation, and descent rate
- After final flaps set: PNF calls out any deviation >±5 knots from approach speed

---

### Description 2 — Cognitive: Representations & Processes *Outside* the Pilots

> This description treats the cockpit as a cognitive system and catalogues the observable representational states.

#### Observable Representations in the Cockpit System
- Gross weight display (fuel quantity indicator)
- Speed card booklet
- Two ASIs with internal and external speed bugs
- Speed select window (flight guidance panel)
- Verbal exchanges between crew members

#### Speed Card Booklet as Long-Term Memory
- Stores weight/speed correspondences for the *entire operating life* of the aircraft
- **Physically durable** and nonvolatile — cannot be corrupted by crew actions
- Gross weight acts as a **filter**: selecting the correct page makes the right speeds the *only visible* ones
- Opening to the correct page = a representation of both gross weight *and* appropriate speeds

> Selecting the correct weight can't help but select the correct speeds. The computation is built into the physical structure of the booklet.

#### Posting the Speed Card
- Creates **distributed access** across social space — both pilots can see it
- Enables **redundant storage and processing**
- Provides a temporally enduring resource for checking/rechecking at any time
- Positioned near the gross weight display for easy cross-verification

#### Setting the Speed Bugs
- Speeds are re-represented from written (speed card) → spoken (PNF announces) → physical position (bug on ASI dial)
- PF reads back spoken values → allows PNF to verify
- Two ASIs = **redundant representation**
- Bug settings are **malleable memory**: specific to this approach, resistant to disruption

#### Using the Configuration Change Bugs
- ASI needle moves counterclockwise as speed decreases
- Bugs **segment the ASI face into regions**, each associated with a flap/slat configuration name
- The needle approaching a bug cues the PF to call for the next configuration
- PNF moves the flap handle → verifies slat extension → additional cross-checks occur

#### Using the Salmon Bug (orange/internal bug)
- Set to the commanded approach speed (Vref + additions)
- Provides the speed reference for both pilots on final approach
- Spatial relation between ASI needle and salmon bug = deviation from target speed
- Base of salmon bug ≈ 10 knots wide → if needle touches the body, within 5 knots of target
- PNF converts this visual judgment into an **auditory call-out** for the PF

> A conceptual task (compute speed deviation) is implemented by a perceptual task (is the needle on the bug?).

---

### Description 3 — Cognitive: Representations & Processes *Inside* the Pilots

> Individual cognitive tasks are *constrained and shaped* by the external representational structure.

#### Computing Speeds
- Pattern matching gross weight to speed card — no need to memorize weight intervals
- Experience may lead to implicit learning of weight intervals over time
- Reading speeds from card requires **working memory** — transposition errors most common

#### Setting Individual Bugs
- Hold target speed in memory → locate on scale → move bug
- Not all tick marks are labeled → interpolation required

#### Remembering the Speeds
- PNF: computing, announcing, and setting bugs creates multiple encoding opportunities → more durable internal memory
- PF: hearing values, possibly reading card, setting own bugs → similar encoding benefit

#### Seeing the ASI with Bugs Set
- Pilots do not merely read the scale; they **impose meaningful structure** onto the dial face
- Regions between bugs = speed regimes with associated flap/slat configuration names
- Must remember the *meanings* of each bug — not just their numeric positions

#### Speed Bugs and Functional Systems (Luria)
> A **functional system** = a constellation of structures, some internal, some external, that together accomplish an invariant task.

- Without bugs: pilot must remember speeds, read scale, compare values mentally
- With bugs: comparison becomes a **judgment of spatial proximity**
- Individual pilot memory is **not enhanced** — but the memory function has been **redistributed** to a larger system
- The pilot engages in a *different kind* of cognitive behavior, not a better-supported version of the old behavior

> Speed bugs do not help *pilots* remember speeds; they are part of the process by which the *cockpit system* remembers speeds.

#### Pilot Memory as Interaction, Not Retrieval
- Memory in the cockpit is not simple retrieval from an internal storehouse
- It is a **continual interaction** with a world of meaningful structure
- Combines: recognition, recall, pattern matching, cross-modality consistency checking, construction, reconstruction
- Pilots opportunistically exploit structure in the environment — including features *not designed* for that purpose (e.g., the width of the salmon bug base as a ±5-knot yardstick)

---

## Part 3: Cognitive Properties of the Cockpit System

### Information Flow Chain
```
Fuel quantity panel (gross weight)
    → Speed card booklet (weight/speed lookup)
        → Speed bugs (physical positions on ASI)
            → ASI regions (named by flap/slat configuration)
                → PF's spoken call for configuration
                    → Flap handle quadrant labels
                        → Flap handle position
                            → Wing configuration
```

### Properties of the Representations

| Medium | Durability | Modality | Vulnerability |
|--------|-----------|----------|---------------|
| Speed card booklet | Permanent | Visual | Misplacement only |
| Speed bugs | Approach-length | Visual | Low (physical state) |
| Verbal announcements | Ephemeral | Auditory | Must be attended immediately |
| Pilot internal memory | Variable/unknown | Internal | Interference, distraction |

### Key System-Level Features

#### Redundancy
- Redundant representation (two ASIs, speed card, verbal)
- Redundant processing (both pilots independently compute/verify)
- Redundant checking (multiple cross-check opportunities)

#### Distribution Across Social Space
- Speed bugs let the PNF transform visual information into auditory information for the PF
- Frees PF's visual resources for flight path monitoring

#### Distribution Across Time
- Speed computation done in **low-workload phase** (~25–30 min before landing)
- Results saved in physical bug positions for use later
- Physical bugs far more reliable than human memory across time — resistant to distraction and interruption

#### Mapping Conceptual onto Perceptual
> The analog ASI display maps an abstract quantity (speed) onto physical space, allowing conceptual operations to be implemented as simple perceptual judgments.

---

## Key Concepts & Definitions

| Term | Definition |
|------|-----------|
| **Distributed Cognition** | Cognitive processes distributed across people, artifacts, and the environment |
| **Functional System** | A constellation of internal and external structures that together accomplish a task (Luria) |
| **Cognitive Artifact** | An external device that participates in cognitive processing (e.g., speed bugs, speed card) |
| **MinMan Speed** | Minimum maneuvering speed; typically 1.3x stall speed for the configuration |
| **Vref** | Reference/approach speed for the final approach segment |
| **PF** | Pilot Flying — responsible for aircraft control |
| **PNF** | Pilot Not Flying — responsible for ATC, checklists, systems |
| **ASI** | Airspeed Indicator |
| **Speed Bug** | A movable marker on the ASI that represents a target speed |
| **Salmon Bug** | The orange internal bug indicating commanded approach speed |

---

## Theoretical Implications

> A complete theory of individual human memory would not be sufficient to understand cockpit memory, because so much of the memory function takes place *outside* the individual.

- The unit of analysis matters: taking the individual as the unit misses most of what is cognitively significant
- External representations are not merely memory *aids* — they are constitutive parts of the cognitive process
- Technological devices introduced into cockpits **change the flow of information** and the nature of cognitive tasks
- System-level cognitive properties **emerge from interactions** between people, artifacts, and physical structure
- What individual memory theory explains is *why* there must be so many external memory components — not how the system works

---

# Studying Context: A Comparison of Activity Theory, Situated Action Models, and Distributed Cognition
**Chapter 4 — Bonnie A. Nardi**

---

## Overview

> The unaided individual divorced from a social group and from supporting artifacts is no longer the model user.

- Central question: What is context, and how should we study it for HCI/technology design?
- Three frameworks compared:
  1. **Activity Theory (AT)**
  2. **Situated Action Models (SA)**
  3. **Distributed Cognition (DC)**
- Nardi argues AT is the richest overall framework, while recognising value in all three.

---

## Situated Action Models

### Core Idea
- Focus on the **emergent, contingent, improvisatory** nature of human activity
- Activity grows directly out of the particularities of a given situation
- Reaction against AI/cognitive science overemphasis on rigid plans and rational problem-solving

### Unit of Analysis
> "The activity of persons-acting in setting" — Lave (1988)

- Not the individual, not the environment — but the **relation** between the two
- **Arena**: stable institutional framework (e.g., a supermarket)
- **Setting**: the arena as personally experienced/edited by the individual

### Key Claims
- Activity is **not pre-structured**; structure only emerges moment-by-moment
- Goals and plans are **retrospective reconstructions** (Suchman 1987) — post hoc rationalisations
- Lave: goals are "constructed, often in verbal interpretation" — they are *retrospective and reflexive*

### Classic Examples
- *Cottage cheese story* (Lave): dieter improvises a measurement solution on the spot — one-time, personal, situational
- Suchman's copier experiment: novices figuring out double-sided copying
- Airport baggage-handling form use

### Research Methods
- Stationary video cameras, shadowing, artifact tracing, event-based analysis
- **No interviews** — verbal reports seen as unreliable rationalisations
- Focus on observable, recordable behaviour

### Strengths
- Corrects overly rationalistic cognitive science models
- Highlights flexibility, opportunism, real behaviour in real situations

### Weaknesses
- Poor fit for **durable, persistent structures** that span situations
- Difficult to **generalise or compare** across contexts
- Downplays consciousness, intentionality, motive, prior knowledge
- Analysis level (moment-by-moment) too low for comparative HCI work
- Somewhat **behaviouristic**: actor reacts to situation rather than proactively generating activity

---

## Activity Theory

### Origins
- Developed in the Soviet Union from the 1920s
- Key theorists: Vygotsky, Leont'ev, Luria

### Unit of Analysis
- The **activity** itself

### Core Structure of an Activity (Leont'ev)

| Component | Description |
|-----------|-------------|
| **Subject** | Person or group engaged in the activity |
| **Object** | The objective/motive — directs and motivates activity ("objectified motive") |
| **Actions** | Goal-directed, conscious processes undertaken to fulfil the object |
| **Operations** | Routinised, unconscious executions of actions (e.g., gear-shifting after driving becomes automatic) |

### Key Concepts

#### Objects
- Precede and motivate activity
- Distinguish one activity from another
- Can transform over time, but not moment-by-moment
- Example: detective's vision for a system that could handle a "Palme case"

#### Actions → Operations (Dynamic Levels)
- Actions become **operations** through habituation (e.g., gear-shifting)
- Operations become **actions** again when conditions impede (e.g., mail program breaks — must consciously use new commands)
- All levels can move **up and down** dynamically

#### Mediation by Artifacts
> "A tool mediates activity that connects a person not only with the world of objects, but also with other people." — Leont'ev

- Artifacts (instruments, signs, language, machines) mediate human activity
- Artifacts carry culture and history; persist across time and space
- Reframe: "computer-mediated activity" rather than "human-computer interaction"

#### Context in AT
- **The activity itself is the context** — not an outer container
- Context is both **internal** (objects, goals) and **external** (artifacts, people, settings)
- Internal and external are **unified**, not separate
- Example: Rostropovich and his cello — inextricably intertwined (Zinchenko)

### People vs. Things
- People and artifacts are **asymmetrical** — artifacts mediate, they do not cognise
- Humans have motive and consciousness; machines do not
- Leads to more humane, responsible technology design
- Critiques Fitts's Law (Bertelsen): treating the human as a "channel" reduces design to "economical optimisation"

### Strengths
- Rich conceptual vocabulary for comparison and generalisation
- Accounts for consciousness, intentionality, history, and durable structures
- Interview data is valid — people *can* articulate goals and actions (though not always operations)
- Longer time horizons supported
- Subjective experience of users is central

---

## Distributed Cognition

### Core Idea
> "A new branch of cognitive science devoted to the study of: the representation of knowledge both inside the heads of individuals and in the world..." — Flor & Hutchins (1991)

### Unit of Analysis
- A **cognitive system** composed of individuals and the artifacts they use
- Goal is at the **systems level**, not the individual level

### Key Example
- The **cockpit system**: pilots + instruments = one cognitive system; success = "completion of a flight"
- Ship navigation (Hutchins 1994)

### Emphasis
- **Representations** — internal and external — and the transformations they undergo
- **Coordination** among individuals and artifacts
- Detailed analyses of specific artifacts (cockpits, spreadsheets, nomograms, CAD systems)
- Finds **stable design principles** applicable across design problems

### People vs. Things
- People and artifacts treated as **conceptually equivalent "agents"** in a system
- Critiqued by Nardi: artifacts cannot *know* anything — they serve as *media* of knowledge for humans
- This equivalence "damps out sources of systemic variation and contradiction"

### Strengths
- Excellent at analysing **persistent structures** and artifacts in depth
- Generates comparative data on work practices across settings
- Useful, stable design principles

### Relationship to AT
> Activity theory and distributed cognition are "very close in spirit" and will likely mutually inform and merge over time — Nardi

- DC lacks AT's engagement with consciousness and individual motive
- DC uses "functional system" as unit — moving even further from the individual

---

## Key Differences: Comparative Table

| Dimension | Activity Theory | Situated Action | Distributed Cognition |
|-----------|----------------|-----------------|----------------------|
| **Unit of analysis** | Activity (subject + object + actions + operations) | Person-acting-in-setting | Cognitive/functional system |
| **Role of goals/motives** | Central — precede and shape activity | Retrospective rationalisations | Systemic goals (not individual consciousness) |
| **Persistent structures** | Central (artifacts, history, culture) | Marginal (tension with situatedness) | Central (especially artifacts) |
| **People vs. things** | Asymmetrical (artifacts mediate) | Asymmetrical (humans qualitatively different) | Symmetrical (both are "agents") |
| **Consciousness/intentionality** | Core — humans are sentient, motivated beings | Downplayed/rejected | Not central |
| **Time horizon** | Long-term | Moment-by-moment | Variable |
| **Comparability** | Strong | Weak | Moderate–strong |
| **Interview data** | Valid and valued | Distrusted | Used in some studies |

---

## The Structuring of Activity

### Activity Theory & Distributed Cognition
- Activity is shaped **before** it unfolds by an object/system goal
- Object partially determines activity
- Explains *why* different people in the same "situation" behave differently

### Situated Action
- Activity is shaped **only as it unfolds** — in situ
- Goals and plans are post hoc
- Cannot distinguish one activity from another by reference to motive

### Nardi's Nature Walk Example
- Bird watcher, entomologist, meteorologist — same environment, radically different behaviour
- Difference is the **subject's object**, not the situation
- Situated action cannot account for this without recourse to intentionality it rejects

---

## Persistent Structures

### Activity Theory
- Artifacts carry culture and history; stretch across activities through time and space
- Vygotsky/Leont'ev: tool use connects person to "the experience of humanity"

### Distributed Cognition
- Most thorough treatment of persistent artifact analysis
- Studies: cockpit devices, spreadsheets, CAD systems, door handles (Norman 1988)
- Properties of artifacts seen as persisting across situations

### Situated Action
- Tension between emphasis on emergence vs. acknowledgment of "routine practices"
- Routines introduced but not well theorised
- Routines imply mental representations — "a chink in the situated armor"

---

## Methodological Implications of Activity Theory

> Four key implications for HCI research:

### 1. Long Research Time Frame
- Sufficient to understand users' **objects** and how they change over time
- Activities are "longer-term formations" (Kuutti)

### 2. Broad Patterns over Episodic Fragments
- Look for overall direction and import of an activity
- Smaller episodes useful only within broader context

### 3. Varied Data Collection
- Interviews + observations + video + historical materials
- No over-reliance on any single method (e.g., video alone)

### 4. Users' Point of View
- Commitment to understanding from the native's perspective
- Essential for practical technology introduction (Bellamy on classroom technology)

---

## Conclusion

> "Activity theory seems the richest framework for studies of context in its comprehensiveness and engagement with difficult issues of consciousness, intentionality, and history." — Nardi

- All three frameworks have value and will mutually inform each other
- Ideal synthesis: **AT as backbone** + DC's focus on representations + SA's commitment to real activity in flux
- HCI still far from Brooks's (1991) ideal corpus: comparative, high-level, design-generative knowledge
- Design is a practical activity — it will proceed regardless; researchers must provide nuanced, generalisable findings

---

## Key Theorists & Works to Know

| Theorist | Contribution |
|----------|-------------|
| Leont'ev (1974, 1978) | Activity theory: subject, object, actions, operations |
| Vygotsky (1978) | Mediation, tools, zone of proximal development |
| Suchman (1987) | *Plans and Situated Actions*; plans as retrospective reconstructions |
| Lave (1988) | *Cognition in Practice*; person-acting-in-setting; cottage cheese example |
| Flor & Hutchins (1991) | Distributed cognition definition; programmer coordination study |
| Hutchins (1991a, 1994) | Cockpit cognition; *Cognition in the Wild* |
| Norman (1988) | *Psychology of Everyday Things*; artifact design principles |
| Brooks (1991) | Ideal for HCI: comparative, high-level, design-suggestive knowledge |

---

# 2.9

# Study Notes: "The Industrial Revolution in the Home"

**Author:** Ruth Schwartz Cowan  
**Source:** *Technology and Culture*, Vol. 17, No. 1 (Jan., 1976), pp. 1–23  
**Publisher:** The Johns Hopkins University Press / Society for the History of Technology

---

# I. Introduction & Thesis

> The industrialization of the home was a process very different from the industrialization of other means of production, and its impact was neither what we have been led to believe nor what students of other industrial revolutions would have predicted.

- Cowan argues that a largely overlooked **technological revolution occurred in the domestic sphere** during the 20th century
- This revolution **transformed daily life in unexpected ways** — not the ways sociologists predicted
- Focus: **middle-class American women** and how changing household technology affected their work, roles, and ideology
- Primary source: nonfiction articles and advertisements in women's magazines (*Ladies' Home Journal*, *Good Housekeeping*, *American Home*, *Parents' Magazine*, *McCall's*)

---

# II. The Standard Sociological (Functionalist) Model

## The Traditional Argument

- Preindustrial family: rural, large, self-sustaining, the basic social unit
- Women's time was entirely absorbed by household tasks
- Under industrialization: family becomes less important, smaller, urban
- Functions reduced to: consumption, socializing children, tension management
- Result: women have **less to do** → role anxiety, divorce, women's liberation

## Cowan's Critique of the Model

- The theory was **never empirically verified**, yet became universally accepted
- Historical evidence challenges it:
  - Phillippe Ariès: the small nuclear family ideal **predates industrialization** in France by over a century
  - Historical demographers: most pre-industrial families were already **small**, not extended
  - Rural English families employed servants; villages had tradespeople — housewives weren't doing everything alone
- Logical flaw: comparing **farm families in 1750** with **urban families in 1950** is like comparing apples to oranges
  - Need to compare families of **similar class and geography** across time

> The large rural family that was sufficient unto itself back there on the prairies may have been limited to the prairies — or it may never have existed at all.

---

# III. Technological Changes in the Home (1918–1930)

> The decade between the end of World War I and the beginning of the Depression witnessed the most drastic changes in patterns of household work.

## Electrification

- 1917: only 24.3% of US dwellings electrified
- 1920: 47.4% electrified
- 1930: ~80% electrified
- Electric lighting was the least of it — **small appliances** created more profound change

## Laundry

- **Electric irons**: inexpensive, rapidly replaced the old flatiron; by 1929, 98/100 Ford workers surveyed had one
- **Electric washing machines**: widespread by mid-1920s; did not fully automate — housewife still had to supervise cycles, add soap, attach drain pipes, and operate the wringer manually
- **Soap powders** (e.g., Rinso, 1918): eliminated need to scrape and boil bar soap
- Net effect: reduced drudgery, but did **not drastically reduce time spent** on laundry

## Bathrooms

- 1920s = "bathroom mania"
- Pre-war: porcelain fixtures custom-made by hand
- Post-war: **mass-produced cast iron enamelware**, standardized fittings
- Production value of enameled sanitary fixtures: $2.4M (1921) → $4.8M (1923) → $5.1M (1925)
- Standard American bathroom form achieved within a decade

## Hot Water & Heating

- Central hot water heating spread rapidly in the 1920s
- Zanesville, OH (1926): 61% of homes had indoor plumbing with centrally heated water
- Muncie, IN (1935): only 22.4% of homes still heated by a kitchen stove
- Eliminated chores: hauling water, heating water on the stove, maintaining the kitchen fire
- Added chores: keeping new rooms clean

## Cooking

- Gas stoves replaced coal/wood stoves
- Muncie, 1924: 2 out of 3 homes cooked with gas; by 1935, only 5% still used coal/wood
- After 1918: coal/wood stove ads disappeared from *Ladies' Home Journal*
- New stoves were easier to light, maintain, and regulate
- Kitchen cleaning reduced by approximately **one-half** when coal stoves were eliminated

## Food

- Canned foods became a **standard middle-class diet staple** in the 1920s
- Home canning became a "lost art" by mid-1920s
- Refrigerated railroad cars: fresh produce available year-round
- Convenience foods appeared: cold cereals, pancake mixes, bouillon cubes, packaged desserts
- Wartime shortages → lighter meals; fewer family members eating at home → **less cooking overall**

---

# IV. Structural Changes in the Household Labor Force

## Disappearance of Servants

- Pre-WWI magazine illustrations: housework shown being done **by servants**; the housewife was depicted as manager or supervisor
- By end of 1920s: all housework shown being done **by the housewife herself**
- Statistics:
  - Household servants employed nationally: 1,851,000 (1910) → 1,411,000 (1920)
  - Households: 20.3M → 24.4M in same period
  - Indiana: ratio of households to servants went from 13.5:1 (1890) to 30.5:1 (1920)
  - National: paid domestic servants per 1,000 population dropped from 98.9 (1900) to 58.0 (1920)
  - Muncie business-class wives: employed **half as many woman-hours** of domestic service as their mothers

> In 1937, Emily Post invented a new character: Mrs. Three-in-One — the woman who is her own cook, waitress, and hostess.

## Increased Tasks Despite Fewer Helpers

- As assistants disappeared, **tasks multiplied**
- Child care expanded dramatically:
  - Prepare special infant formulas, sterilize bottles, weigh children daily
  - Ensure nutritionally balanced meals, isolate sick children, consult teachers, chauffeur to lessons
  - Driven by **new child-rearing theories**, not Freudian psychology — nursemaids unavailable, so mothers had to be the "well-informed persons"
- Consumption became a new skill set:
  - Housewives had to be trained as **informed consumers** — their mothers hadn't shopped for towels, linens, clothing
  - Shopping wisely consumed increasing amounts of time
- Cleanliness standards rose:
  - Discovery of the "household germ" → near-fetishistic concern with cleanliness
  - More frequent laundering of bed linen, underwear, children's clothes

---

# V. The Paradox: Technology Did Not Save Time

> Housework, like so many other types of work, expands to fill the time available.

## Key Time Studies

| Study | Farm Wives | Town/City Wives |
|---|---|---|
| Oregon, 1928 | 61 hrs/week | 63.4 hrs/week |
| Bryn Mawr, post-WWII | 60.55 hrs/week | 78.35 (small city) / 80.57 (large city) hrs/week |
| Survey 1920–1970 (Vanek) | ~53 hrs/week average — **remarkably constant** throughout period |

- Town housewives with modern appliances spent **more** time on housework than rural wives without them — the **opposite** of what the model predicted
- Mechanization decreased time on some tasks but **substituted new tasks** and raised standards on old ones (especially laundering)

> The advantages of mechanization may be somewhat more dubious than they seem at first glance.

---

# VI. Ideological Changes: From Chore to Emotional "Trip"

## Pre-WWI Attitude

- Housework in a servantless home was seen as a **trial** — a necessity until a qualified servant could be found

## Post-WWI Attitude

- Housework reframed as **emotionally significant, deeply personal labor**:
  - Laundering = an expression of love (protecting family from "tattletale gray")
  - Cooking = artistic expression and a way to build family loyalty
  - Diapering = building the baby's sense of security
  - Cleaning = protecting the family from disease

> Tasks of this emotional magnitude could not possibly be delegated to servants.

## The Culture of Guilt

> If I had to choose one word to characterize the temper of the women's magazines during the 1920s, it would be "guilt."

- Housewives were portrayed as feeling guilty or embarrassed about:
  - Infants not gaining enough weight
  - Clogged drains
  - Children in soiled clothes
  - Uncleaned bathroom germs
  - Missing signs of illness
  - Body odor
  - Sons without good breakfasts
  - Daughters in unfashionable or dirty dresses
- Contrast: earlier guilt was about **moral failures** (abandoning children, sexual impropriety); now guilt centered on **domestic imperfection**

---

# VII. Testing the Functionalist Model Against Evidence

## Divorce Rate

- Rising between the wars, but **rising faster for lower classes**, not middle/upper classes who had more access to new technology
- Divorce rate consistently **higher** for those lower on the socioeconomic scale — contradicts the model

## Women's Labor Force Participation

- Strongest correlate of married women's employment: **husband's income** (strongly negative — higher income = less likely she works)
- 1920s increase in women's workforce participation = mostly **single women** and **factory labor**, not middle-class women with appliances
- Again, **opposite** of what the functionalist model would predict

---

# VIII. The Role of Advertisers as Ideological Agents

## The Connecting Link

- Between social change and technological change: **the advertiser** (manufacturer + ad agent + periodical)
- Major players: General Electric, Procter & Gamble, General Foods, Lever Brothers, Frigidaire, Campbell's, Del Monte, American Can, A&P Tea
- These firms funded national advertising campaigns; this expanded women's magazines in the 1920s

## How Advertising Shaped Change

- Appliance ads suggested gadgets would let housewives **fire the maid**, spend more time with children, have afternoons free
- Ads played on **guilt and embarrassment** to sell products (e.g., food brands capitalizing on anxiety over children's weight)
- "Consumer education" campaigns were often corporate promotional tools in disguise

> The advertisers could well be called the "ideologues" of the 1920s.

- Fewer servants → greater demand for appliances
- More tasks for women → more specialized products to buy
- More guilt → more purchasing to minimize failure

---

# IX. Causality: Chicken or Egg?

- Did servant scarcity **cause** mechanization, or did mechanization **cause** servant scarcity?
- Cowan's conclusion: **cause and effect are not separable** — dynamic interaction between social and technological change
  - Servant disappearance stimulated mechanization
  - Mechanization contributed to servant disappearance
  - Emotionalization of housework = both cause and effect of mechanization
  - Time spent on new tasks = both cause and effect of time-saving devices

---

# X. Conclusions & Broader Implications

## Revisions to the Functionalist Model

- For middle-class nonrural American families in the 20th century:
  - The housewife's **functions increased**, not decreased
  - **Family dissolution** did not occur as predicted

## Reversal of Expected Workforce Patterns

When industries mechanize, we expect: more differentiation, more specialization, more managerial roles, less emotional context. For housework, **all four were reversed**:

| Expected | What Actually Happened |
|---|---|
| More differentiated workforce | Less differentiated — one woman did everything |
| More specialization | Less — housewife became generalist |
| More managerial roles | Fewer — she became the manual worker too |
| Less emotional content | More — emotional stakes of housework intensified |

## Proletarianization of the Housewife

- Formerly: manager of subordinate workers
- After: combined manager and manual laborer
- Became a **chauffeur, charwoman, and short-order cook**
- Cowan suggests this "proletarianization" helps explain why **the women's liberation movement of the 1960s–70s** drew its greatest strength from white, educated, middle-class women — those who had most acutely experienced the downgrading of their domestic role

## The Emotional Trap

> That pervasive social illness which Betty Friedan characterized as "the problem that has no name" arose not among workers who found that their labor brought no emotional satisfaction, but among workers who found that their work was invested with emotional weight far out of proportion to its own inherent value.

---

# Study Notes: "Value Sensitive Design and Information Systems"

**Authors:** Batya Friedman, Peter H. Kahn, Jr., and Alan Borning  
**Institution:** University of Washington  
**Source:** Forthcoming in P. Zhang & D. Galletta (Eds.), *Human-Computer Interaction in Management Information Systems: Foundations*. M.E. Sharpe, Inc: NY.

---

# I. Introduction & Thesis

> Value Sensitive Design is a theoretically grounded approach to the design of technology that accounts for human values in a principled and comprehensive manner throughout the design process.

- There is longstanding interest in designing systems that support human values (privacy, autonomy, trust, fairness, etc.) but **no overarching theoretical/methodological framework** existed before VSD
- VSD aims to fill that gap — providing a principled, comprehensive, and practical framework
- Paper structure: define VSD → explain methodology → three case studies → practical suggestions

---

# II. What is Value Sensitive Design?

## Defining "Value"

- Narrow sense: economic worth of an object
- VSD uses a **broader sense**: what a person or group considers important in life
  - Examples: friendship, education, clean air, good science, privacy
- Roots in philosophy since Plato — "the good, the end, the right, obligation, virtue, moral judgment, aesthetic judgment, the beautiful, truth, and validity"
- Key philosophical distinction: **fact/value distinction** — "is" does not imply "ought" (naturalistic fallacy)
  - Values cannot be derived purely from empirical facts; they depend on human interests and cultural context

## Related Approaches (and how VSD differs)

| Approach | Focus | Limitation Addressed by VSD |
|---|---|---|
| Computer Ethics | Key values at intersection of tech and human life | Lacks design methodology |
| Social Informatics | Socio-technical analyses of deployed tech | Retrospective, not proactive |
| CSCW | Collaborative workplace technologies | Limited to workplace and cooperation |
| Participatory Design | Democratic values embedded in design | Narrower value scope; limited to participation/democracy |

> VSD builds on all four but contributes a unique constellation of features not present in any single one.

---

# III. The Tripartite Methodology

> Think of an oil painting by Monet or Cézanne. From a distance it looks whole; but up close you can see many layers of paint upon paint... Together they create an artifact that could not have been generated by a single technique in isolation of the others. So, too, with Value Sensitive Design.

VSD uses **three types of investigations**, applied **iteratively and integratively** — not sequentially.

## Conceptual Investigations

- Identify **direct and indirect stakeholders** and how each is affected
- Identify **which values are implicated**
- Resolve **trade-offs among competing values** (e.g., autonomy vs. security; anonymity vs. trust)
- Determine whether **moral values should trump non-moral ones** (e.g., right to privacy vs. aesthetic preference)
- Develop **philosophically informed working conceptualizations** of specific values
  - Example: Trust defined as vulnerability + belief that others won't exploit that vulnerability; depends on assessments of potential harm, others' good will, and whether harm falls within trust parameters

## Empirical Investigations

- Conceptual analysis alone is insufficient — human context must be investigated
- Uses **full range of social science methods**: observations, interviews, surveys, experiments, document collection, physiological measurements
- Key questions:
  - How do stakeholders understand individual values in context?
  - How do they prioritize competing values?
  - What are differences between **espoused** vs. **actual** practice?
  - How do organizations handle value considerations (motivations, training, rewards, economic incentives)?

## Technical Investigations

- Technologies have **value suitabilities** — they more readily support some values and hinder others
- Two forms:
  1. **Retrospective**: analyze how existing technology supports or hinders values
  2. **Proactive**: design systems to support values identified in conceptual investigation
- Unit of analysis = **the technology itself** (vs. empirical investigations which focus on people/groups)

---

# IV. Three Case Studies

## Case Study 1: Cookies and Informed Consent in Web Browsers

**Values implicated:** Informed consent, autonomy, privacy, trust

### Conceptual Investigation
- Drew on the Belmont Report and bioethics literature to define **informed consent** via five criteria:
  - **Disclosure**: accurate info about benefits and harms
  - **Comprehension**: individual accurately understands what is disclosed
  - **Voluntariness**: action is not coerced
  - **Competence**: person has mental/emotional/physical capacity to consent
  - **Agreement**: clear opportunity to accept or decline, and to withdraw at any time

### Technical Investigation (Retrospective)
- Evaluated Netscape Navigator and Internet Explorer over 5 years (1995–1999) against the five criteria
- Problems found as of 1999:
  - Browsers disclosed *some* cookie info but not the right kind (no info on potential harms/benefits)
  - Internet Explorer placed burden entirely on user to decline third-party cookies one at a time
  - Default setting ("accept all cookies") unchanged from 1995 to 1999 — novice users never warned
  - No alert when a site wished to *use* a cookie vs. merely *store* one

### Technical Investigation (Proactive) + Empirical Iteration
- Redesigned Mozilla browser with three new mechanisms:
  - Peripheral awareness of cookies (color-coded sidebar: red = third-party, green = others)
  - Just-in-time information about individual cookies
  - Just-in-time management of cookies
- Formative evaluations (empirical) added a **sixth criterion**: **minimal distraction**
  - Too many consent queries → users become numbed or disengage entirely (consent by rote)
  - Undue distraction can **single-handedly undermine** informed consent

> This project illustrates the iterative and integrative nature of Value Sensitive Design.

---

## Case Study 2: Room with a View — Plasma Displays in Interior Offices

**Values implicated:** Physical health, psychological well-being, creativity, privacy, civil rights, trust, security

### Conceptual Investigation
- Hypothesis: augmented "window" of nature could provide psychological and physiological benefits in workplaces lacking real windows
- Based on psychological literature:
  - Ulrich (1984): post-operative recovery improved with a view of nature vs. a brick wall
  - Even minimal nature exposure reduces stress, reduces prisoner sickness, calms surgical patients

### Empirical Investigation (Multiple Methods)
- Lab study: compared three conditions — real window, plasma display window, blank wall
- Measures:
  - Physiological (heart rate)
  - Performance (cognitive and creativity tasks)
  - Behavioral (eye gaze, second-by-second)
  - Social-cognitive (50-minute interview per subject)
- Preliminary results:
  - Participants looked at the plasma display **as frequently** as the real window (more than the blank wall)
  - But for gazes of 30+ seconds, the **real window provided greater physiological recovery** than the plasma display

### Key VSD Lessons from this Case Study

#### Multiple Empirical Methods
- Multiple methods increase veracity of accounts of technology in use

#### Direct and Indirect Stakeholders
- Direct stakeholders: office occupants ("The Watchers") — values of health, well-being, creativity
- Indirect stakeholders: passersby in the plaza ("The Watched") — values of privacy, informed consent, trust, safety
- Additional empirical investigations added for indirect stakeholders:
  - Survey of 750 plaza passersby
  - In-depth interviews with 30 plaza passersby
- Key finding: **more women than men** expressed concern about privacy invasion through cameras in public spaces — held regardless of whether images were local, in another city, viewed by one person or millions
- Design implication: future systems must be responsive to **gendered differences** in perceived harm

#### Coordinated Empirical Investigations
- Identical questions were asked of both direct and indirect stakeholders for comparison
- Men in "The Watched" condition expressed more concern about image display than men in "The Watcher" condition — no such difference found for women

#### Value Conflicts
- Physical health and creativity (for direct stakeholders) partially conflict with privacy and civil rights (for indirect stakeholders)

#### Technical Implications
- Cannot psychologically substitute digitized nature for the real thing
- Possible design guideline: design buildings with nature **within view**
- Application to Boeing airplane design: windows matter to human experience of flight even if costly and fuel-inefficient

---

## Case Study 3: UrbanSim — Integrated Land Use, Transportation, and Environmental Simulation

**Values implicated:** Fairness, accountability, democracy, environmental sustainability, walkable neighborhoods, affordable housing, property rights, freight mobility, open space, and many more stakeholder-specific values

### Context
- Problem: urban planning decisions (rail lines, freeways, growth boundaries, taxes) have complex, interacting long-term consequences that current analytic tools cannot model adequately
- UrbanSim: large simulation package predicting urban development patterns over 20+ years under different policy scenarios
- Applied to: Eugene/Springfield OR; Honolulu HI; Salt Lake City UT; Houston TX; Puget Sound WA

### Key VSD Lessons from this Case Study

#### Distinguishing Explicitly Supported Values from Stakeholder Values
- **Explicitly supported values** = ones the team commits to embed in the simulation:
  1. **Fairness** (freedom from bias): simulation must not privilege any group, transportation mode, or policy
  2. **Accountability**: stakeholders can confirm their values are reflected, evaluate validity, develop appropriate confidence
  3. **Democracy**: simulation supports democratic process; does not a priori favor or rule out any stakeholder values
- **Stakeholder values** = important to some but not all stakeholders:
  - Environmental sustainability, walkable neighborhoods, business expansion, affordable housing, freight mobility, minimal government, open space, property rights, environmental justice, etc.

#### Handling Widely Divergent and Conflicting Stakeholder Values
- Cannot focus on a few values (as in the cookies or plasma display cases)
- Solution: web-based interface grouping indicators into three broad categories:
  - Economic, Environmental, Social
- **Indicators**: variables that distill an attribute of interest (e.g., acres of rural land converted, degree of poverty segregation, auto vs. transit mode share)
- Stakeholders select indicators that speak to their values
- Indicator categories rooted in empirical research on human environmental concepts and values, community-based indicator projects, and policy literature

#### Technical Choices Driven by Value Considerations
- Walkable neighborhoods as a value → requires **finer-grained spatial scale** in the simulation than auto-only modeling
- This technical requirement serves both **fairness** (don't privilege automobile) and **democracy** (answer questions important to a significant number of stakeholders)
- Software architecture designed for **rapid evolution**: decoupled component models, SQL database for quick indicator queries, agile development (YP methodology)

#### Designing for Credibility, Openness, and Accountability
- **Credibility**: behaviorally transparent simulation (models households, businesses, developers as agents rather than abstract techniques); sensitivity analyses; historical validation (1980 data → simulated to 1994 → compared with actual 1994 data; 0.917 correlation)
- **Openness**: Open Source software (source code released); code written clearly; rigorous testing
- **Open Process**: development state visible to anyone; physical + virtual traffic light system (green = all tests pass, yellow = testing in progress, red = test failed); bug reports and plans public on website (urbansim.org)

---

# V. VSD's Constellation of Eight Unique Features

| # | Feature | Description |
|---|---|---|
| 1 | **Proactive** | Influences design early and throughout the design process |
| 2 | **Enlarged arena** | Covers workplace, education, home, commerce, online communities, public life |
| 3 | **Tripartite methodology** | Conceptual + empirical + technical investigations, applied iteratively and integratively |
| 4 | **Broad value scope** | All values — especially moral ones (deontology, consequentialism, virtue ethics); also conventions and personal values |
| 5 | **Usability ≠ ethical values** | A highly usable system may still violate ethical values (e.g., a fraud-checking system that is easy to use but violates privacy) |
| 6 | **Direct and indirect stakeholders** | Takes seriously both groups; indirect stakeholders often ignored (e.g., patients in medical records systems) |
| 7 | **Interactional theory** | Values are neither inscribed into technology (endogenous) nor purely socially transmitted (exogenous); technology supports certain values more readily, but actual use depends on people's goals |
| 8 | **Universal + culturally variable values** | Certain values are universally held; how they manifest varies by culture and time. More concrete conceptualizations → more cultural variation; more abstract → more universals |

> The housewife is just about the only unspecialized worker left in America — a veritable jane-of-all-trades at a time when the jacks-of-all-trades have disappeared.

*(Note: above quote is from Cowan, not VSD — verify attribution in exam context)*

### Feature 7 Illustrated (Interactional Theory)
- A screwdriver suits turning screws but can also be used as a pry bar or cutting device — never as a ladle
- An online calendar displaying scheduled events supports accountability but makes privacy difficult
- Technology changes through human interaction: invented → redesigned based on use → reintroduced → further redesign (typified by software updates)

### Feature 8 Illustrated
- Even Inuits living in igloos have conventions ensuring some forms of privacy — though not via separated rooms as in Western cultures
- This is an **empirical** claim (based on psychological and anthropological data), not a philosophical one
- Applies only to **certain** values — some are clearly culture-specific

---

# VI. Practical Suggestions for Engaging in VSD

## 6.1 Start With a Value, Technology, or Context of Use
- Any of the three can be the entry point
- Cookies project: started with a **value** (informed consent) → moved to browser design implications
- UrbanSim: started with a **technology + context** → value issues emerged

## 6.2 Identify Direct and Indirect Stakeholders
- Direct: interact directly with the system or its output
- Indirect: affected by the system without direct interaction
- Key considerations:
  - Multiple subgroups may exist within each category
  - One individual may belong to **multiple** stakeholder groups (e.g., urban planner who also lives in the affected area)
  - Organizational power structure is **orthogonal** to the direct/indirect distinction

## 6.3 Identify Benefits and Harms for Each Stakeholder Group
- Prioritize indirect stakeholders who are strongly affected or who constitute large affected groups
- Attend to technical, cognitive, and physical competency (e.g., children, elderly)
- **Personas** can be useful but have two caveats:
  1. Tend to reinforce stereotypes (require "socially coherent" attributes)
  2. Standard personas map one person to one group; VSD allows one persona to map to multiple stakeholder groups

## 6.4 Map Benefits and Harms onto Corresponding Values
- Sometimes direct: invasion of privacy → privacy value
- Sometimes multifaceted: improved mood at work → psychological welfare AND creativity AND physical health AND productivity

## 6.5 Conduct a Conceptual Investigation of Key Values
- Turn to philosophical/ontological literature for criteria defining the value
- Criteria then enable empirical assessment

## 6.6 Identify Potential Value Conflicts
- Common conflicts:
  - Accountability vs. privacy
  - Trust vs. security
  - Environmental sustainability vs. economic development
  - Privacy vs. security
  - Hierarchical control vs. democratization
- Conflicts are **constraints on the design space**, not binary either/or situations
- If one value directly hinders another, extensive stakeholder discussion is warranted

## 6.7 Integrate Value Considerations Into Organizational Structure
- Ideally VSD works in concert with organizational objectives (increased revenue, employee satisfaction, customer loyalty)
- When human values collide with economic objectives: VSD can show alternate designs that better support values while retaining needed properties
- Enables more effective arguments against claims that a given (value-violating) design is the "only reasonable choice"

## 6.8 Human Values with Ethical Import Often Implicated in System Design

| Value | Core Definition |
|---|---|
| Human Welfare | Physical, material, and psychological well-being |
| Ownership and Property | Right to possess, use, manage, derive income from, and bequeath an object or information |
| Privacy | Individual's right to determine what information about themselves can be shared |
| Freedom from Bias | Absence of systematic unfairness (pre-existing, technical, or emergent social bias) |
| Universal Usability | Making all people successful users of information technology |
| Trust | Expectations between people involving good will, vulnerability, and potential betrayal |
| Autonomy | Ability to decide, plan, and act in ways one believes will achieve one's goals |
| Informed Consent | Agreement encompassing disclosure, comprehension, voluntariness, competence, and agreement |
| Accountability | Actions of a person or institution can be traced uniquely to them |
| Courtesy | Treating people with politeness and consideration |
| Identity | Understanding of who one is over time |
| Calmness | Peaceful and composed psychological state |
| Environmental Sustainability | Meeting present needs without compromising future generations |

> This list is a heuristic — not comprehensive. Peacefulness, respect, compassion, love, creativity, humor, loyalty... could extend indefinitely.

## 6.9 Heuristics for Interviewing Stakeholders
- Semi-structured interviews offer a good balance between focused inquiry and new insights
- Use **"Why?"** iteratively to probe values and value conflicts (example: senior with ubiquitous surveillance system → first "why" reveals value conflict; second "why" reveals privacy value)
- Ask about values both **directly** and **indirectly**:
  - Direct: "What is X? Can you give an example from your life?"
  - Indirect (preferred): use hypothetical situations, everyday events, tasks, or behaviors just engaged in
  - Reason: people often cannot directly reflect on concepts they nonetheless hold

## 6.10 Heuristics for Technical Investigations
- Make explicit how each **design trade-off maps onto a value conflict** and differentially affects stakeholder groups
- Design **flexibility into the technical architecture** to accommodate unanticipated values and value conflicts that emerge after deployment
- Underlying protocols that release information should be **turn-off-able** — and stakeholders should be confident they have been turned off (especially important for ubiquitous computing/sensors)

---

# VII. Conclusion

> Our hope is that this approach can contribute to a principled and comprehensive consideration of values in the design of information and computational systems.

- VSD emerged over roughly a decade of research
- Provides both theory and practical tools for integrating human values into technology design
- The three case studies collectively validate VSD across different scales:
  - Cookies: proof-of-concept for mainstream internet software
  - Room with a View: cutting-edge display technology, multiple stakeholder groups
  - UrbanSim: complex large-scale sociotechnical system with politically contentious stakeholder values

---

# Study Notes: "Do Artifacts Have Politics?"

**Author:** Langdon Winner  
**Source:** *Daedalus*, Vol. 109, No. 1, Modern Technology: Problem or Opportunity? (Winter, 1980), pp. 121–136  
**Publisher:** The MIT Press on behalf of American Academy of Arts & Sciences

---

# I. Introduction & Central Claim

> At issue is the claim that the machines, structures, and systems of modern material culture can be accurately judged not only for their contributions of efficiency and productivity, not merely for their positive and negative environmental side effects, but also for the ways in which they can embody specific forms of power and authority.

- Winner's provocative thesis: **technical artifacts are not politically neutral** — they can embody specific forms of power and authority
- This is not merely about how technology is *used*, but about what is built into its **design and arrangement**
- Definitions:
  - **"Politics"** = arrangements of power and authority in human associations, and the activities within those arrangements
  - **"Technology"** = modern practical artifice; pieces or systems of hardware of a specific kind (narrower than Jacques Ellul's "technique")

## The Two Dominant (and Opposing) Views Winner Critiques

### 1. Naive Technological Determinism
- Technology develops from its own internal logic and then molds society to fit its patterns
- No recognition of social and economic forces shaping technology
- Winner considers this view inadequate

### 2. Social Determination of Technology
- "What matters is not technology itself, but the social or economic system in which it is embedded"
- Useful corrective to determinism — reveals social origins and power behind technological change
- **Shortcoming**: taken literally, suggests technical things do not matter at all; reduces technology studies to standard models of social power (interest groups, class struggle, bureaucratic politics)

> Winner's position: both are incomplete. A third view — **technological politics** — is needed, one that takes technical artifacts seriously as political phenomena in their own right.

---

# II. Two Ways Artifacts Can Have Political Properties

Winner identifies two distinct types:

| Type | Description | Flexibility | Key Question |
|---|---|---|---|
| **Type 1: Technical Arrangements as Forms of Order** | Specific designs or arrangements settle social/political issues in particular communities | Flexible — could have been built differently | Who chose the design, and why? |
| **Type 2: Inherently Political Technologies** | Some technologies by their very nature require or are strongly compatible with particular political arrangements | Inflexible — no alternative design resolves the issue | Does adopting this technology commit us to a particular form of political life? |

---

# III. Type 1: Technical Arrangements as Forms of Order

## Core Argument
- Technologies are **ways of building order in the world**
- Societies choose structures for technologies — consciously or not, deliberately or inadvertently — that shape how people work, communicate, travel, and consume for a very long time
- The **greatest latitude of choice** exists at the moment of first introduction; once choices are fixed in material equipment, economic investment, and social habit, the original flexibility largely vanishes
- Technological innovations are therefore analogous to **legislative acts or political foundings** — they establish frameworks for public order that endure across generations

## Key Examples

### Robert Moses's Low Overpasses (Long Island, NY)
- Moses (master builder of NY public works, 1920s–1970s) had ~200 overpasses built with as little as **9 feet of clearance** — too low for twelve-foot-tall buses
- **Intent**: Documented by Robert Caro (*The Power Broker*) — Moses's racial and class prejudice
  - Automobile-owning white middle and upper classes could use parkways freely
  - Poor people and Black residents, who relied on public transit, were physically excluded
- **Effect**: Limited access of racial minorities and low-income groups to Jones Beach (a public park); Moses also vetoed a proposed extension of the Long Island Railroad to Jones Beach
- **Legacy**: Long after Moses and his political alliances are gone, the physical structures continue to enforce social inequality

> "Many of his monumental structures of concrete and steel embody a systematic social inequality, a way of engineering relationships among people that, after a time, becomes just another part of the landscape."

### McCormick's Pneumatic Molding Machines (Chicago, 1880s)
- Cyrus McCormick II installed pneumatic molding machines at his reaper plant at ~$500,000
- Standard economic interpretation: modernization for efficiency
- **Actual purpose**: Defeat the National Union of Iron Molders — "weed out the bad element among the men" (the organized skilled workers)
- The new machines (run by unskilled labor) produced **inferior castings at higher cost**
- After three years the machines were **abandoned** — but by then the union had been destroyed
- Cannot understand this technological development outside the history of labor organizing and the Haymarket bombing

### Haussmann's Parisian Boulevards
- Baron Haussmann widened Parisian streets at Louis Napoleon's direction after the Revolution of 1848
- Broad thoroughfares made it **impossible to build barricades** and easier to deploy troops
- Architecture and urban design as counter-revolutionary political technology

### American University Campuses (1960s–70s)
- Concrete buildings and large open plazas designed to **defuse student demonstrations**
- Physical design as a form of political crowd control

### Mechanical Tomato Harvester (UC, 1940s–present)
- Developed at University of California; harvests tomatoes in a single pass; led to breeding of harder, less tasty tomatoes
- Reduces costs ~$5–7/ton vs. handpicking
- **Social effects**:
  - Machines cost $50,000+ each → compatible **only** with concentrated, large-scale farming
  - Tomato growers: ~4,000 (early 1960s) → ~600 (1973)
  - ~32,000 farmworker jobs eliminated by late 1970s
  - Benefit concentrated among very large growers; harm concentrated among farmworkers, small farmers, rural communities
- No conspiracy: developers not motivated by desire to concentrate industry
- Instead: scientific knowledge, technological invention, and corporate profit reinforce each other in **deeply entrenched patterns** bearing the stamp of political and economic power
- Agricultural R&D in American land-grant colleges has **structurally favored** large agribusiness for decades
- Opponents of the harvester were made to seem "antitechnology" or "antiprogress"

> "The harvester is not merely the symbol of a social order that rewards some while punishing others; it is in a true sense an embodiment of that order."

## Important Nuances

### Political Consequences Do Not Require Malicious Intent
- Moses and McCormick: intentional and somewhat conspiratorial
- Inaccessible design for the handicapped: arose from **long-standing neglect**, not active intention — yet the political consequence (exclusion from public life) was real and required remedy
- Many of the most important cases **transcend the "intended/unintended" distinction** entirely — the technological deck is stacked long in advance

### Two Types of Choices Within a Given Technology
1. **"Yes or no"** — whether to adopt the technology at all (e.g., nuclear reactors, highways, pesticides)
2. **Specific design features** — after the basic decision to adopt, controversies over placement, components, modes of access, etc. (e.g., route of power lines; design of computer systems)
  - David Noble's study of record/playback vs. numerical control machine tool systems: **same basic components, but different implications for the balance of power between management and labor on the shop floor**

---

# IV. Type 2: Inherently Political Technologies

## Core Argument

> Some technologies are by their very nature political in a specific way. The adoption of a given technical system unavoidably brings with it conditions for human relationships that have a distinctive political cast — centralized or decentralized, egalitarian or inegalitarian, repressive or liberating.

- Unlike Type 1 (where the artifact is flexible and could have been built differently), here **the choice of technology is itself a choice of a form of political life**
- No alternative design or arrangement would significantly change the political implications

## Friedrich Engels's "On Authority" (1872) — Classic Statement

- Arguing against anarchists who wanted to abolish all authority:
- Cotton-spinning mills, railways, ships at sea all require workers to **subordinate their individual wills** to centralized command — not because of capitalism, but because of the technology itself
- The timing of factory work is "fixed by the authority of the steam"
- Railway and ship operations require workers to submit to "imperious authority"
- Relationships of authority and subordination arise "independently of all social organization" — imposed by the material conditions of production

> "The automatic machinery of a big factory is much more despotic than the small capitalists who employ workers ever have been."

- If Engels is right: as society adopts increasingly complex technologies, **prospects for authoritarian life are greatly enhanced**
- Note: **tension with Marx** — in *Capital*, Marx argued that increasing mechanization would eventually render obsolete the hierarchical division of labor; Engels's position suggests the opposite
- This theoretical tension mirrors real troubles in socialist revolutions

## Two Versions of the "Inherently Political" Argument

### Stronger Version: Technology *Requires* Specific Political Conditions
- Adoption of the technical system **actually requires** the creation and maintenance of particular social conditions — as a matter of **practical necessity**
- Example: Nuclear power requires a "techno-scientific-industrial-military elite"
- Example: Plato's ship — requires one captain and an unquestioningly obedient crew (practical necessity, not logical necessity)

### Weaker Version: Technology is Strongly *Compatible With* Specific Political Conditions
- The technology does not strictly require a political form, but is much more compatible with one than another
- Example: Solar energy advocates — solar is decentralizing both technically (distributed, disaggregated systems) and politically (accessible, comprehensible, controllable at the local level) → more compatible with democratic, egalitarian society
- Solar does not *require* democracy, but suits it; coal, oil, and nuclear power suit centralization

### Internal vs. External Conditions
- **Internal**: conditions required within the workings of the technical system itself (Engels's factory authority)
- **External**: how the technology complements or conflicts with the broader organization of society (solar energy and democratic governance)

## Key Examples of Inherently Political Technologies

### The Atom Bomb
- Most obvious case: its lethal properties demand a **centralized, rigidly hierarchical chain of command**, closed to any influences that might make its workings unpredictable
- The internal social system of the bomb must be authoritarian — this is true regardless of what kind of political regime controls it
- Democratic states must actively work to prevent the authoritarian mentality of nuclear weapons management from "spinning off" into the polity as a whole

### Railroads and Large Industrial Systems (Alfred Chandler, *The Visible Hand*)
- Safe, reliable railroad operation required the development of **large-scale, centralized, hierarchical organizations administered by skilled managers** — the first administrative hierarchies in American business
- The same pattern holds for oil pipelines, refineries, electrical systems, chemical production, and communications
- These technologies "demanded" or "required" this form of human association
- Not just capitalism — Chandler's evidence suggests the pattern transcends any particular social or political system
- **Key open question**: Could decentralized, democratic worker self-management administer these systems as well? (Examples from Sweden and Yugoslavia offered; Winner does not settle the question)

### Plutonium Recycling and Civil Liberties
- As uranium runs out, plutonium recycling is proposed as an alternative nuclear fuel
- Beyond known economic, environmental, and weapons proliferation risks:
- Plutonium theft risk would create pressure for **background checks, covert surveillance, wiretapping, informers, emergency martial law** — all justified by the need to protect the substance
- Russell Ayres: "Once recycling begins and the risks of plutonium theft become real rather than hypothetical, the case for governmental infringement of protected rights will seem compelling."
- After a certain point, those who resist the "hard requirements" will be dismissed as dreamers

> "Once a course of action is underway, once artifacts like nuclear power plants have been built and put in operation, the kinds of reasoning that justify the adaptation of social life to technical requirements pop up as spontaneously as flowers in the spring."

---

# V. The "Practical Necessity" Problem in Political Life

- In societies built on large, complex technological systems, **moral reasons** (liberty, justice, equality) appear increasingly "idealistic" and irrelevant
- Any ethical argument can be neutralized by: *"Fine, but that's no way to run a railroad"*
- This is a critical feature of modern political discourse: **practical necessity eclipses other forms of moral and political reasoning**
- The question of whether democracy "stops at the factory gates" is not as harmless as Americans have traditionally assumed
  - Study of American business leaders: those who run hierarchical firms tend to see corporate authority as **the desirable model against which to compare political relationships in the rest of society**
  - Energy crisis discourse: calls not for wealth redistribution or broader participation, but for **stronger, centralized management** (e.g., Carter's Energy Mobilization Board)

---

# VI. Conclusion: Winner's "Both/And" Position

> I have argued a "both/and" position here, for it seems to me that both kinds of understanding are applicable in different circumstances.

- Both Type 1 and Type 2 interpretations are valid — applicable in different circumstances; can overlap within a single complex technology
  - Example: A communication or transportation system may have some aspects that are flexible and others that are completely intractable
- **On renewable/solar energy**: Winner is skeptical that they are *intrinsically* democratic — their social consequences will depend on the specific configurations of both hardware and social institutions created around them
- **On nuclear power**: Winner believes it is **not flexible** — its adverse social effects cannot be fixed merely by adjusting design parameters; the long-range toll on human freedom is the critical unasked question

> "People are often willing to make drastic changes in the way they live to accord with technological innovation at the same time they would resist similar kinds of changes justified on political grounds. If for no other reason than that, it is important for us to achieve a clearer view of these matters than has been our habit so far."

---

# VII. Summary: Key Conceptual Distinctions

| Concept | Winner's Position |
|---|---|
| Are artifacts politically neutral? | No — they can embody specific forms of power and authority |
| Do we need to find a conspiracy? | No — political consequences can be unintended, systemic, or structural |
| Is social determination of technology enough? | No — it reduces technology to nothing special; ignores properties of artifacts themselves |
| Are all technologies equally flexible? | No — some are flexible (Type 1), some are inherently political (Type 2) |
| Does inherently political mean absolutely required? | No — "required" here means **practical necessity**, not logical necessity |
| Can we ignore context? | No — but context alone is insufficient; the artifact itself must be examined |
| Is solar energy inherently democratic? | Winner is skeptical — consequences depend on hardware AND social institutions |
| Is nuclear power inherently authoritarian? | Yes — Winner argues this strongly |

---

# 2.10

# Study Notes: "Don't Forget the Teachers": Towards an Educator-Centered Understanding of Harms from Large Language Models in Education

**Authors:** Emma Harvey, Allison Koenecke, René F. Kizilcec  
**Institution:** Department of Information Science, Cornell University  
**Source:** *CHI '25: Proceedings of the 2025 CHI Conference on Human Factors in Computing Systems*, April 26–May 1, 2025, Yokohama, Japan  
**DOI:** https://doi.org/10.1145/3706598.3713210

---

# I. Introduction & Central Argument

> While edtech providers focus primarily on mitigating technical harms, i.e., those that can be measured based solely on LLM outputs themselves, educators are more concerned about harms that result from the broader impacts of LLMs, i.e., those that require observation of interactions between students, educators, school systems, and edtech to measure.

- LLM-based edtech is proliferating rapidly (personalized tutoring, writing feedback, language learning, lesson planning) and is being used in classrooms **before its risks are fully understood**
- Prior LLM harm taxonomies (Bender et al.; Weidinger et al.) are **domain-agnostic** and do not address education's unique features
- Education is uniquely different from other AI domains because:
  - Its population (K-12 students, often children — special privacy and ethical considerations)
  - Its goals (learning *how* to arrive at an answer matters more than getting the right answer)
  - Its higher-order outcomes (critical thinking, collaboration, social skills — not automatable or directly observable)
  - It involves direct human interaction — cannot be studied outside the context of teachers and students using these tools

## Three Paper Contributions
1. An **education-specific overview of potential harms** from LLMs
2. **Gaps between edtech providers' and educators'** conceptions of harm
3. **Recommendations** to facilitate educator-centered edtech design and development

---

# II. Background & Related Work

## What is Edtech?
- "Technologies specifically designed for educational use as well as general technologies that are widely used in educational settings"
- Not necessarily AI-based (abaci, calculators, WolframAlpha are all edtech)
- Recent AI advances have intensified interest in AI-powered edtech for personalized learning

## What are LLMs?
- Models trained on massive internet text data to predict the most probable next token in a sequence
- Enable fluent text generation; used for natural language understanding and generation
- Key risk taxonomies: Bender et al. (2021) "Stochastic Parrots" and Weidinger et al. (2022) "Taxonomy of Risks" — but both are **domain agnostic**

## Prior Work on AI Harms in Education
- Holmes et al.: ethical concerns include data privacy, quality of AI instruction, teacher/student agency, equity in AI decision-making
- Yan et al.: similar concerns plus inequality from English-language bias in LLM research
- Lee et al.: mapped sources of bias across the "life cycle" of an LLM
- Documented real harms: AI edtech discriminates by race, gender, disability; impinges on privacy and autonomy; provides inaccurate tutoring

## Existing Frameworks and Their Gaps
- US Department of Education: humans-in-the-loop; evidence-based pedagogies; privacy, explainability, non-discrimination
- Institute for Ethical AI in Education: additionally includes learner autonomy and informed deployment
- **Limitation of all these frameworks**: not specific to LLMs; do not address hallucinations, academic dishonesty, or the unique dynamics of LLM-based interactions
- UNESCO and others call for examining "uncharted ethical issues" around access, equity, and human social/intellectual development
- Williamson et al.: call for a **pause** on LLM-based edtech adoption until responsible AI frameworks are in place
- US DOE (new guidance): proposes "designing for education" via co-design between edtech providers and educators, with trust-building as a crucial first step

---

# III. Method

## Study Design
- **29 semi-structured interviews** conducted November 2023 – February 2024 via Zoom (30–60 minutes each)
- Inductive-deductive **thematic analysis** (Braun & Clarke 2006)
- Interview saturation reached: defined as 5 consecutive interviews with no new harms proactively raised

## Participants: Edtech Providers (N=6, IDs: T1–T6)
- International leaders in edtech; each product has ≥10,000 active student users
- LLM functionalities covered: live chat, live feedback, content pre-generation, report generation
- Mix of for-profit/non-profit and STEM/multi-subject focus
- All have research backgrounds and hold leadership/development team roles
- Limitation: only 6 participants → **cannot generalize** to the full edtech market

## Participants: Educators (N=23, IDs: E1–E23)
- Roles: teachers (12), instructional support (6), guidance counselors (2), administrators (2), prefer not to say (1)
- School types: public (12), charter (6), private (4)
- Subjects: STEM (10), language (4), social studies (3)
- LLM experience ranged from none to significant (custom chatbot creation)
- Recruited via professional networks, educator listservs, and **snowball sampling** to increase diversity
- Compensated $50 per interview

## Coding Approach
- Started with pre-identified domain-agnostic harms as initial code set
- Codes tracked: whether harm was proactively raised or prompted; level of concern; experience with harm; mitigation strategies
- Two passes through all transcripts; synthesis reviewed by all three authors
- Concern levels coded as "higher" or "lower" based on explicit statements or inferred impact on LLM use

## Positionality
- Interdisciplinary team: algorithmic fairness, computational social science, learning sciences
- None have been K-12 educators; one has held a research role at an edtech startup
- All identify as holding "mixed" prior opinions on LLMs
- Focused primarily on the US education system

---

# IV. How Edtech Providers Account for LLM Harms

## 4.1 Technical Harms (Primary Focus of Providers)

All six providers were aware of and actively mitigating technical harms.

### Mitigation Approaches
- **Human oversight**: internal moderation teams reviewing flagged content (T1, T5, T6); educators given access to student chat logs (T1, T5)
- **Technical guardrails**: LLM-based toxicity detectors like Perspective API (T1, T2, T5, T6); filtering personal information (T2, T4, T5); retrieval-augmented generation (RAG) to validate correctness (T1, T2)
- **Bias**: handled with less certainty than toxicity; some used prompt engineering to instruct tools to avoid biased responses (T1, T5)

### Open Challenge: Inherently Stochastic Outputs
- Most providers acknowledged that mitigations **cannot guarantee** harm-free outputs (T1–T4, T6)
- Even a small chance of harm is too high a risk for some: *"I only need one student or one teacher to tweet about how [the product] told something very, very inappropriate to a student, and that's it, really"* (T4)
- Key mitigations: generating only static, human-reviewed content (T1, T3, T4, T6); restricting live LLM access to adult users only (T4); limiting chat context windows (T1, T3)

### Open Challenge: Dependence on OpenAI
- Several providers lacked control over a core component of their platform (T2, T4, T5)
- Must repeatedly re-test prompts and guardrails after each LLM update (T2)
- Fine-tuning out of reach for providers lacking resources to redo fine-tuning after each update (T4, T5)

## 4.2 Harms from Human-LLM Interactions (Limited Provider Focus)

- Only two providers reported exploring these harms
- T1: gate agent designed to reject adversarial prompts (e.g., prompts that elicit answers instead of advice)
- T5: lockdown browser-style guardrails to prevent LLM use during assessments

## 4.3 Harms from Broader Impacts (Partial Provider Focus)

### Inhibiting Student Learning
- Almost all providers raised the importance of measuring tool "helpfulness" (T1–T4, T6)
- Approaches: collecting user feedback/ratings; A/B testing academic performance; risk-benefit analyses before integrating LLMs
- One provider specifically checked that helpfulness did not vary across demographic groups (T2)
- Others deliberately limited data collection for fear of appearing "creepy" (T3, T5)

### Open Challenge: Adherence to Pedagogy
- LLMs tend to produce "the average of the internet instructional style" rather than following evidence-based curricula — a problem providers are still struggling to solve (T1, T4)

---

# V. How Educators Account for LLM Harms

## Key Contrast with Providers

> Educators were most concerned about technical harms occurring in cases when LLMs disrupted the teacher-student relationship, as this reduced their ability to personally mitigate harms.

- Educators feel **most equipped** to handle technical harms and academic dishonesty through their own teaching practices — precisely the harms providers focus on
- Educators feel **least equipped** to handle the broader impacts of LLMs — precisely the harms providers cannot currently measure or mitigate

## 5.1 Technical Harms

### Toxic Content, Stereotyping, and Bias
- Most educators found outright toxic content unlikely (suggesting provider mitigations have been effective)
- Multiple educators had personal experience with **biased content**: "Eurocentric" outputs (E1, E13, E18); negative stereotypes about Black children (E3)
- Most educators felt confident mediating bias by creating "teachable moments"
- Concern intensified when educators could **not be the intermediary**: *"I can't even fathom having to plan for a computer program making those mistakes... And then I can't correct that either"* (E7)

### Privacy Violations
- Mixed levels of concern; even those most concerned felt able to teach students safe LLM use
- Most pressing educator privacy concern: students might **confide personal details about abuse or harm to a chatbot** rather than to an educator who could intervene (E4, E17)
- Educators are less worried about LLMs collecting sensitive data than about LLMs **preventing educators from accessing** critical student information

### Hallucinations
- Most direct experience of any harm — many educators personally encountered hallucinations
- Mitigation: reviewing AI-generated content before it reaches students; teaching students to fact-check
- Concern highest when students use LLMs **without educator oversight**: *"especially when you're young and a kid, you're like, 'oh, well, the computer said it'"* (E16)

## 5.2 Harms from Human-LLM Interactions

### Academic Dishonesty
- High awareness but **mixed concern** — most educators felt able to address it through teaching
- Preferred detecting dishonesty through their **own intuition and relationships** with students rather than AI detectors like Turnitin
- Reasons: AI detectors are fallible (false positives on translated text, old dissertations — see E5's story); educators prefer cultivating discussions over "calling the whatever-you-call-it-police" (E4)
- Some educators simply changed their teaching practices: *"if a computer can do the task that you assigned, is it the most meaningful task?"* (E21)

## 5.3 Harms from the Broader Impacts of LLMs (Educators' Primary Concerns)

> These were proactively raised by multiple educators without any prompting from interviewers.

### Inhibiting Student Learning
- Most prominent educator concern: LLMs erode **critical thinking** skills and students' unique **voice**
- *"I've noticed that as students become more tech aware, they also tend to lose that critical thinking skill. Because they can just ask for answers."* (E18)
- Mitigation: having students critique LLM outputs or consider alternatives (E5, E11, E15); most educators simply **limited LLM use** or said they did not know how to address it
- Related: educators frustrated that LLM tools cannot align with their specific evidence-based curricula, undermining best practices and confusing students

### Inhibiting Student Social Development
- Concern: reliance on LLMs will reduce group work and human interaction; worsen social isolation already seen from social media, cell phones, and COVID lockdowns
- *"Instead of working in groups — cause a lot of kids don't like working in groups — they'll work with the AI and get the answers. So, human interaction, I think, is going to be cut in half."* (E14)
- Mitigation: limiting LLM use especially in homework assignments
- Educators also worried about erosion of **trust between students and teachers**: *"especially working in juvie, if you don't make that personal connection with your students, they'll shut you out for the rest of your life"* (E18)

### Increasing Educator Workload
- Educators feel obligated to spend significant personal and professional time:
  - Vetting LLM tools for classroom suitability
  - Attending professional development (often sponsored by edtech providers themselves)
  - Taking external courses (sometimes of poor quality: *"With the class I'm taking, the professor, the way they talk about AI, it's like it's foolproof. It's everything. That's the impression I got. It can't make any mistakes,"* E14)
  - Conducting independent research
- **No mitigation strategies** surfaced from either providers or educators for this harm

### Decreasing Educator Autonomy
> "Don't forget the teachers... The teachers are supremely important in making all of this happen. So listen to them." — E7

- Educators report that tools are often designed and procured **without educator input or concrete educational goals** in mind: *"I don't know that anybody thought about education when any of these tools came out"* (E1)
- Many educators are excluded from school/district-level LLM procurement decisions
- Restricted by decisions made at the school, district, or state level: tools they liked being replaced by institutionally vetted (but often worse) alternatives (E6)
- Simultaneously restricted by **lack of clear guidance** from leadership: *"The district doesn't know what to do with [generative AI]. So I also have to be careful I don't go too far with it, and then get myself in trouble"* (E8)
- No mitigation strategies surfaced from providers; educators' only self-help is educating themselves on the LLM ecosystem

### Exacerbating Systemic Inequalities
> "I feel like it's always gonna be this income-level gap. Well-off districts are gonna pay for this stuff and struggling districts aren't. And those are the kids that are behind." — E9

- LLM-based edtech often priced at district/school license levels — inaccessible to under-resourced schools
- Financial burdens of vetting tools fall disproportionately on smaller/poorer districts
- Broader critique: edtech platforms prioritize monetization over public good
- **No mitigation strategies** surfaced from either providers or educators

---

# VI. Key Gaps Between Providers and Educators

| Harm Category | Harm | Raised by Providers | Raised by Educators |
|---|---|---|---|
| Technical | Toxic or biased content | ✓ | ✓ |
| Technical | Privacy violations | ✓ | ✓ |
| Technical | Hallucinations | ✓ | ✓ |
| Human-LLM Interaction | Academic dishonesty | ✓ | ✓ |
| Broader Impacts | Inhibiting student learning | ✓ | ✓ |
| Broader Impacts | Inhibiting student social development | ✗ | ✓ |
| Broader Impacts | Increasing educator workload | ✗ | ✓ |
| Broader Impacts | Decreasing educator autonomy | ✗ | ✓ |
| Broader Impacts | Exacerbating systemic inequalities | ✗ | ✓ |

> The harms edtech providers focus most on are the harms educators feel most equipped to handle themselves. The harms educators are most worried about are the ones providers cannot currently measure or mitigate.

---

# VII. Recommendations

## (1) Edtech Providers → Design for Educator Mediation
- Build opportunities for educator mediation **directly into tools** (e.g., educator control over oversight levels, co-design processes, adjustable guardrails)
- This simultaneously increases educator autonomy and mitigates a broad range of harms

## (2) Regulators → Centralized, Independent Edtech Reviews
- Create clear, unbiased, centralized vetting of LLM-based edtech
- Leverage existing infrastructure (e.g., What Works Clearinghouse) to build searchable repositories of vetted tools
- Reduces burden on individual educators and provides accurate, unconflicted information

## (3) Researchers + Providers → Entrust Tool-Building to Educators
- Educators want to build or customize tools that "speak the language" of their school and curriculum — some already plan to create custom chatbots via prompt engineering and fine-tuning (E12, E20)
- Current workarounds are inadequate: adapting off-the-shelf tools often creates **more work** than building from scratch
- Promising research avenue already emerging in HCI

## (4) Regulators + School Leaders → Educator-Centered Procurement
- Actively solicit educator input in procurement decisions
- Ensure educators are **not penalized** for declining to use school LLM tools
- Procurement processes should require risk-benefit analysis focused on improving existing practices without marginalizing educators

---

# VIII. Limitations & Ethical Considerations

## Limitations
- Only interviews from US, UK, and Canada → findings apply to **WEIRD** (Western, Educated, Industrialized, Rich, Democratic) contexts only
- Well-documented global harms (cultural bias, low-resource language performance, unequal labor and environmental costs) were not surfaced by interviewees
- Growing global scholarship on LLMs in edtech and decolonial considerations are not captured
- Only 6 edtech provider participants → **cannot generalize** across the full edtech market
- Sample of educators over-represents: those with prior LLM experience, positive LLM opinions, white people, men, STEM teachers (partially addressed via snowball sampling)

## Ethical Considerations
- Classic participatory AI tension: goal is to center educators, but method (Zoom interviews) demanded their already-limited time
- Mitigated by paying educators $50/interview ($50–100/hour)
- All participants guaranteed anonymity; risks of re-identification mitigated through: anonymized quotes, low-granularity descriptions, secure IRB-compliant data storage, deletion of original recordings after transcription

---

# IX. Taxonomy Summary: Education-Specific LLM Harms

| Harm Category | What is Required to Measure | Education-Specific Harms |
|---|---|---|
| **Technical Harms** | Outputs of LLM-based systems | Toxic content, biased content, privacy violations, hallucinations |
| **Human-LLM Interaction Harms** | Interactions between LLM-based systems and students/educators | Academic dishonesty |
| **Harms from Broader Impacts** | Interactions between LLM-based systems, students, educators, and/or school systems | Inhibiting student learning and social development; increasing educator workload; decreasing educator autonomy; exacerbating systemic inequalities |

---

# From Awareness to Action: The Effects of Experiential Learning on Educating Users about Dark Patterns

**Authors:** Jingzhou Ye, Yao Li, Wenting Zou, Xueqiang Wang  
**Institution:** University of Central Florida; Pennsylvania State University  
**Published:** CHI '25, April 26–May 1, 2025, Yokohama, Japan  
**DOI:** https://doi.org/10.1145/3706598.3713493

---

## 1. Introduction

> Dark patterns (DPs) are unethical UI designs that deceive users into unintended, potentially harmful decisions — ultimately benefiting online businesses.

### Key Background
- Term coined by **Harry Brignull in 2010**
- Examples: stealthy cart additions → financial loss; complex cookie opt-out → privacy violation
- Knowledge of DPs remains largely confined to research communities
- Legislative and technical mitigation efforts are **limited and not widely adopted**

### Research Gap
- Little attention given to educational interventions for DP awareness
- This study introduces **DPTrek** — an **Experiential Learning (EL)** platform using simulated real-world DP cases

### Study Contributions
- First attempt to educate users about DPs using concrete EL experiences
- Reveals limitations of existing DP taxonomies for end-users
- Identifies lack of effective mitigation tools as a critical gap

---

## 2. Related Work

### 2.1 Dark Patterns

> Taxonomies are often not designed with end users in mind.

- Research perspectives: definitions, taxonomies, empirical consequences (general + specific contexts like games, privacy settings)
- **Regulatory efforts:** FTC Act, CARU guidelines — limited to clear deception/privacy violations; constrained by limited investigative resources
- **Detection methods:** computer vision, NLP, empirical content analysis, user studies
  - e.g., Mathur et al. crawled 11,000 shopping websites
- **Mitigation attempts:** UI rewriting — not widely adopted due to deployment challenges (workload, scalability, warranty risks)

---

### 2.2 Cybersecurity Education

#### Formal Education
- Coursework, seminars, certifications — instructor-led, structured
- Influence often stays within home institutions

#### Informal Education
- **Fact-and-Advice:** text, graphic, video — lacks personal relevance
- **Storytelling:** narratives of incidents — no direct participation
- **Gamified education:** role-playing, card games, CTF, adventure — structured, lacks reflection support

> Existing informal methods fall short in providing first-hand experience, which is critical for understanding deceptive, complex DPs.

---

### 2.3 Experiential Learning (EL)

> EL is a model where learners gain knowledge through concrete experiences combined with critical reflection. — Kolb (2014)

#### Kolb's Four Components
1. **Concrete Experience** — hands-on engagement
2. **Reflective Observation** — reflecting on the experience
3. **Abstract Conceptualization** — learning concepts from reflection
4. **Active Experimentation** — applying new insights

#### Why EL for DP Education
- DPs require real-world problem-solving (core EL focus)
- DPs are context-specific — EL enables contextually rich scenarios
- DP consequences are dangerous/ambiguous — EL provides a safe exploration environment
- Enables the full cycle: experience → reflect → learn → experiment

---

## 3. Methods

### 3.1 DPTrek Platform

#### Five DP Modules (based on Gray et al. 2018 taxonomy)
| Category | Description |
|---|---|
| **Nagging** | Persistently reminding users to take an action in an annoying/coercive manner |
| **Obstruction** | Deliberately making a process harder to discourage specific actions |
| **Sneaking** | Hiding/disguising/postponing revelation of important information |
| **Interface Interference** | Manipulating UI to prioritize certain actions over others |
| **Forced Action** | Requiring users to complete an action to access functionality |

#### Four Simulated DP Cases Per Module
- 2 cases used **in DPTrek** (Experience + Experiment phases)
- 2 cases used **in the test**
- Cases sourced from Gray et al., Brignull's website, and companion site
- Generated via **ChatGPT** with manual adjustment for functionality/aesthetics

#### Four Phases Per Module
1. **Experience** → Concrete Experience: navigate a simulated DP freely; face consequences if trapped (e.g., ads, financial loss)
2. **Reflection** → Reflective Observation: record observations, feelings, frequency of daily encounters
3. **Learning** → Abstract Conceptualization: text + graphics on DP concepts, real cases, coping suggestions
4. **Experiment** → Active Experimentation: new DP case with feedback on actions; consequences if failed

> Pilot tested with 6 sessions (2 education experts + 4 learners); 8 follow-up meetings; ~3.5 months development

---

### 3.2 Study Procedure

#### Participants
- **38 participants** recruited in the U.S. (18+), mostly from UCF (36/38)
- Recruited via social media (Facebook, Twitter, Reddit), mailing lists, flyers, referrals
- Compensated: **$20 Amazon gift card**
- Demographically skewed: mostly 18–25, high education, STEM, Asian

#### Groups
| Group | n | Method |
|---|---|---|
| **Treatment** | 19 | DPTrek (EL platform) |
| **Control** | 19 | Web-based Static Content Learning (same content, no EL phases) |

- Study conducted via **Zoom** with screen-sharing and recording
- Actions logged via web logging (button clicks, timestamps, page events) → JSON → AWS S3

#### Post-Intervention Evaluations
1. **DP Coping Test** — 2 new simulated DP cases per module; success/failure logged
2. **DP Knowledge Quiz** — Multiple-choice; classifying DP categories + identifying consequences
3. **Survey-Based Subjective Evaluation** — 5-point Likert scale on 8 constructs
4. **Exit Interview** — Treatment group only; qualitative feedback

#### Survey Constructs
| Construct | What It Measures |
|---|---|
| Enjoyment | Pleasure/fulfillment from training |
| Confidence | Belief in ability to handle DPs |
| Perceived Usability | Frustration/difficulty with the platform |
| Aesthetic Appeal | Visual attractiveness |
| Reward | Perceived worthwhileness |
| Attitude of Coping with DPs | Overall attitude toward DP coping |
| Perceived Risk of DPs | Uncertainty/potential loss from DPs |
| Future Behavioral Intention | Intent to engage in DP training again |

#### Ethical Considerations
- Sensitive inputs (passwords, phone numbers) were optional, masked, and **not logged or stored**
- Raw data (Zoom recordings, logs) deleted after anonymization

---

### 3.3 Data Analysis

| Data | Collection Phase | Group | Method |
|---|---|---|---|
| Success/Failure on DPs | Experience + Experiment | Treatment | Wilcoxon signed-rank test (before-after) |
| # Successes on DPs | DP Coping Test | Both | Mann-Whitney U Test (between groups) |
| Quiz answers | DP Knowledge Quiz | Both | Mann-Whitney U Test |
| Likert ratings | Subjective Survey | Both | Mann-Whitney U Test |
| Interview recordings | Exit Interview | Treatment | Thematic Analysis |

> Mann-Whitney U used because: non-normal distribution, small sample, ordinal/continuous outcomes, independent groups.

---

## 4. Quantitative Results

### 4.1 Treatment vs. Control Comparison

#### DP Coping Test
> Treatment group significantly outperformed the control group across all DP categories.

- All p-values < 0.05 (Mann-Whitney U)
- Overall accuracy: Treatment ~85.3% vs Control ~44.2%
- Largest gap: Nagging (89.5% vs 28.9%), Forced Action (97.4% vs 81.6%)

#### DP Knowledge Quiz
- **Overall accuracy**: 65.8% (treatment) vs 60.5% (control) — **NOT significant**
- **Consequence questions**: 87.4% (treatment) vs 73.7% (control) — **Significant** (p = 0.031)
- **Category classification**: Not significantly different between groups

> DPTrek improves understanding of DP consequences, but not necessarily category classification.

#### Survey-Based Subjective Evaluation
- **Significantly higher** in treatment group:
  - **Enjoyment**: 4.46 vs 4.19 (p = 0.002)
  - **Aesthetic Appeal**: 4.00 vs 3.60 (p < 0.05)
- **Not significant**: Confidence, Perceived Usability, Reward, Attitude, Risk, Future Intention
- Notably: **Confidence and Reward were slightly lower** in treatment group (not significant)

---

### 4.2 Before-After Comparison (Treatment Group)

> Significant improvement from Experience → Experiment → DP Coping Test.

- Wilcoxon signed-rank: Experience vs Experiment (p = 0.000), Experience vs Test (p = 0.001) — **Significant**
- Experiment vs Test — **Not significant** (slight decrease)

#### Reflection Phase Findings
- **96.8%** successfully identified DPs and consequences during observation
- Most common emotion: **"Annoyed"** (46.3%) — strongest in Nagging (84.2%) and Forced Action (52.6%)
- "Concerned" common in Sneaking and Obstruction
- Most frequently encountered DPs daily: **Obstruction** (31.6% "always", 42.1% "often") and **Interface Interference** (52.6% "often")

---

## 5. Qualitative Results

### 5.1 Positive Impacts of DPTrek

#### Improved Awareness
- Participants more vigilant; better at recognizing risks in daily browsing
- e.g., P1: increased awareness of Sneaking on shopping websites

#### Better Coping Skills
- Participants learned to double-check and be more careful
- e.g., P2: importance of verifying receipts for discrepancies

#### Value of Real-World Examples
- Participants highly valued real cases from familiar platforms
- e.g., P12: "seeing these patterns in real-life examples makes it easier to identify them"

---

### 5.2 Negative Feedback on DPTrek

#### Impractical Coping Strategies
- "Leave the website" and "report the website" are not always viable
- e.g., P3: "Sometimes you really need to buy something, and just leaving the website isn't a practical solution"

#### Difficulty Memorizing DP Category Names
- Terms are unfamiliar and not part of everyday language
- e.g., P11: "I understand the concepts deeply, but the names of the dark patterns are somewhat confusing"

#### Difficulty Classifying DPs
- Perceived overlap between categories (e.g., Obstruction vs Forced Action)
- e.g., P6: confusion distinguishing obstruction from forced action

#### Educational Burden on Users
- P22 argued top-down regulation is more effective than user education alone
- "Those who design dark patterns can always come up with new tactics"

---

## 6. Discussion

### EL-Based DP Education is Effective
- DPTrek outperforms static content in coping skills and consequence understanding
- Traditional fact-based instruction may fail to convey the manipulative nature of DPs
- EL addresses this through hands-on experience, reflection, conceptualization, and experimentation

> Implication: EL-based education is broadly applicable to informal cybersecurity education (e.g., phishing, privacy policies).

---

### A User-Friendly DP Taxonomy is Needed

> Current taxonomies are built by HCI experts for UX designers — not for end users.

- Benefits of a user-friendly taxonomy:
  1. Enables transfer of coping strategies within a category across different website presentations
  2. Prepares users for **emerging DP variants** by enabling correct categorization
- Recommendation: Include end-user input in taxonomy development; evaluate ease of understanding

---

### Lack of Practical Solutions to Mitigate DPs

- **Nagging** and **Forced Action** are hardest to avoid — users are often forced to accept them
- Existing technical solutions (UI rewriting, highlighting) face scalability/robustness issues
- Proposed multi-layered approach:
  - **Laws and regulations** targeting DPs
  - **Education of practitioners** on ethical UI design
  - **Platform-integrated solutions** (OS, browsers, marketplaces) for robust mitigation
  - Collaborative effort across legislation, UI design, and user education

---

## 7. Limitations

- **Lack of demographic diversity**: mostly 18–25, STEM, high education, from one institution (36/38)
- Results may not generalize to broader populations (less tech-savvy users)
- Institutional cybersecurity culture may bias the sample
- Based on one taxonomy (Gray et al. 2018) — other variants not explored
- **No long-term follow-up**: effectiveness with evolving/new DPs not assessed

---

## 8. Conclusion

> DPTrek, an EL platform using simulated real-world DP cases, effectively enhances users' ability to identify and manage dark patterns.

### Key Takeaways
- EL outperforms static content learning for practical DP coping skills
- EL improves understanding of DP consequences specifically
- Users find EL more enjoyable and visually appealing
- Critical gaps remain: user-unfriendly taxonomies + lack of practical mitigation tools
- Future work needed: broader participant diversity, long-term evaluation, richer mitigation strategies

---

## Quick Reference: DP Categories & Examples

| Category | Real-World Example | Consequence | Strategy |
|---|---|---|---|
| **Nagging** | Persistent notification prompts with no clear opt-out | Promotional notifications | Reject/report app |
| **Sneaking** | Unwanted magazine subscription added to cart | Unintended financial loss | Remove extra items; be careful |
| **Obstruction** | Google made cookie refusal harder than acceptance | Pop-up ads | Stay persistent through extra steps |
| **Interface Interference** | Trump campaign preselected recurring donations | Unintended emails/charges | Uncheck default options |
| **Forced Action** | LinkedIn forced email address during registration | Forced to receive emails/SMS | Reject/report app |

---

# "I am a Technology Creator": Black Girls as Technosocial Change Agents in a Culturally-Responsive Robotics Camp

**Authors:** Chun Li, Jaemarie Solyst, Safiyyah Scott, Gabriella Howse, Tara Nkrumah, Erin Walker, Amy Ogan, Angela E.B. Stewart  
**Institutions:** University of Pittsburgh; Carnegie Mellon University; Arizona State University  
**Published:** CHI '25, April 26–May 1, 2025, Yokohama, Japan  
**DOI:** https://doi.org/10.1145/3706598.3713242

---

## 1. Introduction

> Much computing education positions Black girls as workers who execute tasks for others' purposes. This work repositions Black girls as **technosocial change agents**.

### Opening Vignette: Jada
- Day 1: "No — a technology creator has to have good experience, I'm not really an expert"
- Day 3: "No, I am?" (lingering doubt after making progress)
- Day 5: "Yeah, because I created a robot." ← shift in identity = TSCA development

### Core Concept: Technosocial Change Agency (TSCA)
TSCA is the ability to:
1. **Challenge dominant narratives**
2. **Construct more liberating identities**
3. **Construct more liberating social relations**
4. **Create new technologies**

> Coined by Dr. Kimberly Scott and colleagues; originally developed in the COMPUGIRLS program.

### Why Black Girls, Ages 9–12?
- Systemic racism + sexism shape CS learning experiences
- Early experiences shape attitudes toward technology and future participation
- Informal environments outside school can center their identities as assets

### Why Robotics?
- Robots enhance joyfulness in project-based learning
- **Hummingbird robotics kit** chosen: fun, open-ended, self-regulated pace, customizable
- Tangible feedback from robot behavior tracks progress and sense of agency

### Research Question
> How did Black girls exhibit their technosocial change agency while engaging in the open-ended creation of a robot within a CRC camp?

### Three Main Contributions
1. Analysis of how Black girls exhibit TSCA in a real-world technology creation experience
2. First paper to trace all **four TSCA dimensions** in the context of a CRC robotics camp for Black girls
3. Design guidelines for computing educators and CRC program developers on technology and curricula

---

## 2. Related Work

### 2.1 Black Girls and Women in Computing

> Only **2.6%** of CS PhDs were awarded to Black women (CRA Taulbee Survey, 2022–2023), vs. 14.4% for White women and 11.4% for Asian women.

#### Intersectionality (Kimberlé Crenshaw)
- Race, class, gender, sexuality all interact to shape Black girls' CS opportunities
- Combined effects of racism + sexism create structural barriers at school

#### 2.1.1 Curricula and Pedagogy
- Overemphasis on coding speed, numeric scores, and task competence → misleads girls' CS perceptions
- Disconnected curricula (not relevant to girls' real lives) hinder engagement
- Heavy reliance on lecturing, standardized testing, and abstract teaching
- This paper proposes **TSCA as an alternative metric of success**

#### 2.1.2 Classroom Environment
- Computing perceived as masculine and "hardcore"
- Boys are 1.5× more likely to receive teacher encouragement; 1.7× more likely to be told by parents they'd be good at computing; ~2× more likely to see role models like them on social media (Google/Gallup, 2020)
- 62% of Black girls reported teachers were less supportive of their career interests (vs. 73% of White girls felt supported)
- Black girls more likely to be scolded for "supposedly subverting authority" or not behaving "ladylike" (Morris, 2007)
- CS has been naturally associated with "really, really smart" White and Asian males (Margolis, 2017)
- "Geeky" learning environments (e.g., Star Wars décor) reduce Black girls' sense of belonging

---

### 2.2 A Preview of Promising CRC Programs

| Camp | Participants | Key Outcome |
|---|---|---|
| **Bulls-EYE PRIDE** | Underrepresented minority 7/8th graders | Designed robots to address social justice issues |
| **GET IT** | Middle/high school girls | Increased girls' knowledge and interest in IT careers |
| **Raspberry Pi Project** | K-12 teachers, UK | Teachers introduced student agency/choice into practice |
| **Digital Mirror Camp** | Girls from diverse races/classes | Designed feminist, creative computing products |
| **Digital Youth Divas** | Non-dominant urban middle school girls | Narrative + mentorship supported identity and interest in STEM |
| **COMPUGIRLS** | African American & Latina urban girls | Girls gained empowerment; maintained commitment to community |

> Informal learning spaces are helpful for positive emotional experiences with computing, especially when curricula foster learners' sense of possibility (Alexandre et al., 2022).

---

### 2.3 CRC and TSCA: Centering Systemically Marginalized Learners

#### Culturally Responsive Pedagogy (CRP)
- Promoted in the 1990s (Ladson-Billings, 1995)
- Builds on gendered-ethnic minority students' strengths; connects curricula to lived experiences

#### CRC (Culturally Responsive Computing) — Scott et al.'s Five Tenets
1. All students are capable of digital innovation
2. The learning context supports transformational use of technology
3. Learning about oneself along intersecting sociocultural lines allows for technical innovation
4. Technology should be a vehicle to reflect and demonstrate intersectional identity
5. Barometers for technological success should consider **who creates, for whom, and to what ends**

#### TSCA — Defined by Ashcraft, Eger & Scott (2017)
- Developed through COMPUGIRLS
- Four dimensions: challenging dominant narratives, constructing liberating identities, constructing liberating social relations, creating new technologies
- Shifted focus to girls' interactions with each other and teachers; emphasized sociocultural features

---

### 2.4 Technology Empowerment: HCI Community's Exploration of Agency

> In HCI, **sense of agency** = the feeling of being in control over actions and their consequences.

- Agency in HCI is often realized through intentional tool design that lets users modify their environment
- Shneiderman's 8 golden rules include keeping users feeling a sense of agency
- High-agency conditions → more efficient learning (Harpstead et al., 2019)
- **TSCA differs from individual HCI agency**: it emphasizes empowering *marginalized communities* to use technology for *social change and equity*, not just personal autonomy
- Technologies providing hands-on, personalized experiences (e.g., robotics kits) are most effective for enhancing young learners' agency

---

## 3. Methods

### 3.1 Participants

- **Camp held:** July 2022, East Coast USA
- **Partner:** Out-of-school education organization serving predominantly Black children for 50+ years (multi-year partnership)
- **7 participants** (out of 8 sign-ups), ages 9–12, average age 10.5, average grade 5.5
- All self-identified as girls; 6 described as "Black or African American," 1 also "Hispanic"
- 4 had some prior CS experience; 3 had little to none

| Pseudonym | Age | Prior Experience | Robot |
|---|---|---|---|
| Destiny | 12 | Computer activities/class | Cali (girl) |
| Diona | 10 | Smartphone, iPad, Apple Watch | Didn't clarify |
| Femi | 9 | None | Mariah (girl) |
| Hawa | 10 | Lego robotics class | Karii, formerly Steven (boy) |
| Panya | 10 | Coding class (3rd grade) | Kayla (girl) |
| Olivia | 11 | Not really | Cleo (girl) |
| Opal | 11 | Not really | Rob (boy) |

---

### 3.2 Data Collection Procedure

- **Duration:** 5 days, 4 hours/day (2 morning + 2 afternoon sessions), **20 hours total**
- **Facilitators:** 7, from diverse cultural/racial backgrounds (Asian, White, Black women); led by a Black American faculty with 20+ years of CRP experience in STEM
- All facilitators completed **multi-day professional development** in CRP principles

#### Three Types of Activities
1. **Culturally responsive warm-ups** — community building, identity reflection (e.g., name game, defining identity)
2. **AI fairness sessions** (Days 1–2) — AI bias, storytelling; *not the focus of this paper*
3. **Robot creation sessions** (afternoons, Days 2–5) — Hummingbird kit + craft materials; culminated in **Robot Runway**
4. **Dialogue creation sessions** (mornings, Days 3–5) — comic strips, robot dialogue

#### Robotics Workshop Sessions
| Session | Topics | Highlight |
|---|---|---|
| 1 | Flow of control, LEDs | Connected LED programming to TikTok lights |
| 2 | Rotation and position servos | Physical demonstrations on example robot "Stanley" |
| 3 | Sound sensor, loops, conditionals | Loops mastered; conditionals more challenging (abstract logic) |
| 4 | Finishing touches, Robot Runway (TikTok video) | Final video added per learners' request to share with friends/family |

---

### 3.3 Data Processing and Analysis

- **Qualitative approach:** facilitator observation notes, images/videos of artifacts, semi-structured interviews
- Interview questions: work process, self-perception ("Are you a technology creator?"), interactions, feelings, comfort with sharing
- Audio recorded and transcribed; **verbal permission obtained** before each interview session
- **Thematic analysis** of transcripts, artifacts, and facilitator notes

#### Coding Process (Hybrid)
- 2 authors: **inductive open coding** (chronological, descriptive labels)
- 2 authors: **deductive coding** using TSCA framework (4 dimensions)
- Team discussions until consensus; analysis organized into **2 main finding categories**:
  1. Creating technology helps Black girls refine and fulfill their definition of technical creators
  2. Helping, being helped, creating, and sharing — factors that influenced Black girls' agency

---

## 4. Findings

### 4.1 Creating Technology Helps Black Girls Refine and Fulfill Their Definition of Technical Creators

#### 4.1.1 Girls Set an Impossibly High Standard Initially
- Early definitions of technology creators: producing TVs/phones independently; working at Apple; wearing glasses and a vest with blue hair; knowing "hacking"
- "Doing it every day" = good creator; "not keeping stuff in order" = bad creator (Femi)
- Despite coding and assembling electronics, **none** considered themselves technology creators
- When asked if anyone in the room was a technology creator, Panya, Opal, and Olivia all answered **no**

#### 4.1.2 From Apple to My Community — Technology Creators Are People Around Me
- By Day 3, girls began naming **real people they knew** as technology creators
- Hawa: shifted from "people at Apple" → Ms. F (community staff member)
- Diona: recognized a facilitator who "taught us all the steps to build the robot"
- Olivia: later identified her teachers as technology creators
- Peers also began recognizing each other: Destiny (shared her solution), Hawa (presented work), Diona (explored coding blocks on her own)

#### 4.1.3 Through Creating Robotics, Black Girls Included Themselves
- By the final day, **6 out of 7 girls** identified themselves as technology creators
- Destiny: "kind of" a technology creator because she solved the same problems as her definition
- Opal: progress from "a technology creator knows how to fix anything" → "a little bit" (emerging identity)
- Femi: added "robots" to her list of what technology creators produce after making progress
- Key pattern: **definitions became more specific and grounded in the tasks they actually performed**

---

### 4.2 Helping, Being Helped, Creating, and Sharing — Factors That Influenced Black Girls' Agency

#### 4.2.1 Accepting Help Weakens Agency; Helping Others Strengthens It

> "I just built this without most of the help." — Panya (on why she was a technology creator)

- Learners were cautious about accepting help; independence was seen as achievement
- Olivia: doubted her capability to reproduce the robot — "No, because I got a lot of help"
- Hawa: "not sure about working... without any help" after camp
- **Destiny's paradox:** figured out robot wheel speed independently → helped peers → yet still said she was only "kind of" a technology creator because she also received help
- Learners perceived helping others as a characteristic of technology creators (e.g., teachers who "help us and make the robot")
- Over time, learners adapted and enjoyed more equitable relationships with facilitators
- **"Power switch" phenomenon:** Diona interviewed facilitators as if she were the teacher, Femi acted as camera person — roles were reversed

#### 4.2.2 Black Girls Demonstrate Agency by Creating, Controlling, and Sharing Their Robots
- Hawa: creating robot made her feel powerful "by motivating me to be good and cheer"
- All learners **mirrored their own identity** in their robots:
  - Destiny: bun and black clothing (matching her own style)
  - Femi: pink ribbon ponytail (matching her own)
  - Panya: headband and purse → "Kayla" is fashionable "because she is fashionable"
  - Destiny: named robot "Cali" because she always wanted to go to California
  - Femi's "Mariah" has ocean animal stickers because Femi likes swimming
  - Olivia's "Cleo" has favorite color blue — same as Olivia's
- Sharing also enhanced agency:
  - Olivia: "I want other people to be inspired by it"
  - Destiny: "I want to share with people who want to know about robots"
  - Olivia: linked sharing to career potential — "it can make a lot of money"
  - Opal: selective about audience — "people I trust... they don't laugh at it"

---

## 5. Discussion

> The discussion maps findings to the **four dimensions of TSCA**.

### 5.1 Black Girls Challenge Dominant Narratives to Build More Liberating Identities

- Initial answers connected to dominant narratives: "rock star" programmer, solo/nerdy profession, wealthy tech companies
- As girls progressed, the distance between them and "technology creator" narrowed:
  - Teachers/facilitators → peers → themselves
  - Vague (phones, TVs) → specific tasks they completed
- Open-ended creation strengthens technical identity and broadens perception of who can create
- CRC programs that center joyfulness and creative production support this shift
- Mainstream CS curricula lack cultural relevance for Black girls and do not create this space

> Building technical identities has positive long-term dynamics — learners who see themselves as technologists are more confident they can master STEM in the future.

---

### 5.2 Black Girls Challenge Dominant Narratives to Build New Technologies

- Robots reflected **Black feminine cultural elements**, especially hairstyles
- Hair for Black women/girls is "a historical heritage of Black cultural pride... symbolizes resistance, creative expression, and freedom" (Thompson, 2008)
- This is not commonly depicted in mainstream robotics media or education
- Girls created robots **they had never seen before** — challenging whose image technology can take

---

### 5.3 Black Girls Construct More Liberating Social Relationships

- Observed **bi-directional** relationship between individualism and communalism:
  - Individual → Community: Destiny solved a problem and shared it with peers
  - Community → Individual: peers recognized Destiny as a technology creator
- Tension: U.S. education and American culture strongly emphasizes individualism and rewards individual accomplishment → learners initially hesitant to collaborate
- Over time, girls embraced collaboration and found joy in creating as active community members
- Camp environment: flexible seating, group discussions, equitable dynamics supported this

---

### 5.4 Applications to Technology and CS Education — Design Guidelines

#### 1. Introduce Open-Ended Tasks at a Self-Regulated Pace
- Space for personalized expression (e.g., fashion, hairstyles) allows learners to connect with cultural identity
- Open-ended tasks let learners set their own goals and pace

#### 2. Encourage Reflection on Cultural Backgrounds and Aesthetic Expressions
- Products that differ from mainstream tech should be recognized and encouraged by facilitators
- Robotics is useful because of ease in creating humanoid-like artifacts
- Storytelling activities can support critical analysis of existing and new technologies

#### 3. Scaffold Collaboration with Peers
- Peer helping raises self-concept as a technologist; role model effect strengthens group dynamics
- Strategies: recognizing achievements, peer teaching, group projects
- Reflective activities needed to disrupt the idea that independent creation is the only valid achievement

#### 4. Intentionally Design the Physical Environment
- Flexible seating and shared workspaces support collaboration
- Desk arrangement facing front → teacher as sole knowledge source (discouraged)
- Physical setup can dismantle classroom hierarchies

---

## 6. Limitations and Future Work

- **Small sample (N=7):** intimate but limits generalizability; larger samples needed
- **Pre-existing friendships:** some girls knew each other, which may have influenced collaboration patterns
- **Exploratory, not causal:** cannot determine causation between camp and TSCA development; cannot confirm when/for how long/under what conditions TSCA emerges
- Future work: longitudinal experimental designs, larger and more diverse samples

---

## 7. Conclusion

> Involving learners in creating technology in an informal learning environment helps accomplish TSCA and supports the goals of CRC.

- Black girls moved from technology consumers to creators
- Through open-ended robot creation, they challenged dominant narratives, built liberating identities, formed more liberating social relationships, and created new technologies
- Key insight: **TSCA is a more meaningful and culturally appropriate metric of success than traditional technical competency scores**

---

## Quick Reference: TSCA Framework

| Dimension | What It Means | Evidence in This Study |
|---|---|---|
| **Challenging Dominant Narratives** | Pushing back on stereotypes of who creates technology | Girls redefining "technology creator" to include themselves and their peers |
| **Constructing Liberating Identities** | Building technical + cultural identity | 6/7 girls identified as technology creators by Day 5 |
| **Constructing Liberating Social Relations** | Changing power dynamics through collaboration and knowledge sharing | Destiny helping peers; "power switch" with Diona interviewing facilitators |
| **Creating New Technologies** | Making tech that reflects their values and community | Robots with Black hairstyles, fashion, personal stories — never seen in mainstream robotics |

---

## Key Theorists & Concepts to Know

| Name/Concept | Relevance |
|---|---|
| **Harry Brignull (2010)** | Coined "dark pattern" — also see other paper |
| **Kimberlé Crenshaw** | Intersectionality — how race + gender compound barriers |
| **Kimberly Scott et al. (2017)** | Coined TSCA; developed COMPUGIRLS |
| **Ladson-Billings (1995)** | Culturally Responsive Pedagogy (CRP) |
| **Scott, Sheridan & Clark (2015)** | Extended CRP to CRC; five tenets |
| **Kolb (2014)** | Experiential Learning — also central in the DPTrek paper |
| **Shneiderman** | 8 golden rules of UI design; includes maintaining user sense of agency |
| **COMPUGIRLS** | CRC program for adolescent girls; where TSCA was first developed |
| **Hummingbird Kit (BirdBrain Technologies)** | Robotics kit used in this camp; lights, motors, sensors; open-ended |

---

# Moving Beyond the Simulator: Interaction-Based Drunk Driving Detection in a Real Vehicle Using Driver Monitoring Cameras and Real-Time Vehicle Data

**Authors:** Robin Deuber, Patrick Langer, Mathias Kraus, Matthias Pfäffli, Matthias Bantle, Filipe Barata, Florian von Wangenheim, Elgar Fleisch, Wolfgang Weinmann, Felix Wortmann  
**Institutions:** ETH Zürich; University of Regensburg; University of Bern; University of St. Gallen  
**Published:** CHI '25, April 26–May 1, 2025, Yokohama, Japan  
**DOI:** https://doi.org/10.1145/3706598.3714007  
**Source code:** https://github.com/im-ethz/CHI25_Drunk-Driving-Detection-in-a-Real-Vehicle.git

---

## 1. Introduction

> Alcohol-related road crashes cause more than **700 fatalities daily**, accounting for **22% of fatal driving incidents globally**.

### Public Health Context
- ~5% of global deaths are attributable to alcohol consumption
- Alcohol impacts 27 different causes of disease, injury, and death (WHO)
- SDG Target 3.5: mitigate harmful alcohol use; Target 3.6: reduce road traffic mortality
- Drunk driving called "the cancer of mobility"

### Policy Context
- US Congress mandated future vehicles include in-vehicle drunk driving detection and prevention systems
- NHTSA (2023) specified the system must operate **"passively"** — breathalyzers do not qualify
- Ignition interlock breathalyzers: installation costs $70–200 USD; monthly fees $60–100 USD → not scalable

### The Solution
> Use sensors **already present in modern vehicles**: Driver Monitoring Cameras (DMC) + CAN bus data

- DMCs are **mandated by EU law** and required for high safety ratings globally
- CAN (Controller Area Network) bus connects vehicle components (steering, speed, etc.)
- This study develops and evaluates a **machine learning (ML) system** using DMC + CAN data to detect drunk driving

---

### 1.1 Contributions

1. Performance of the real-vehicle system is **comparable to prior simulator-based findings**, even using lower-quality industry-standard cameras (not lab eye-tracking)
2. Extended existing work with **two new camera feature types** and added CAN data as a second modality
3. Demonstrated **strong generalization to unseen drivers** (leave-one-subject-out validation)
4. Model relies on **well-known physiological patterns** of drunk driving — interpretable
5. Included **two control groups** (placebo + reference) to address placebo effects, training effects, and drowsiness

### Novelty
> First study to implement and rigorously evaluate a drunk driving detection system in **real vehicles** using DMC and real-time CAN bus data.

---

## 2. Related Work

### 2.1 Alcohol Detection and Harmful Use Prevention
- BAC detected via smartphone activity data: AUROC of 0.80 (Lee et al., 2024)
- SoberMotion: combined smartphone + breathalyzer to prevent DUI recidivism
- Wearable wristband sensors also used for alcohol detection
- SoberComm: communicates alcohol-use data to family and treatment teams
- Prior HCI work shows detecting alcohol through human-computer interactions is **feasible** and can support digital interventions

---

### 2.2 Driver State Detection
- **Active safety systems** (ADAS) proactively prevent accidents (vs. passive systems like crumple zones)
- Driver state detection types:
  - **Physiological:** heart rate, brain activity
  - **DMC-based:** gaze direction, head movements, facial expressions
  - **CAN data-based:** steering, lane-keeping, speed

> DMC and CAN systems each account for ~44% of the drowsiness detection market (88% combined). DMCs are becoming standard.

- Two DMC-based approaches: (1) human-interpretable features + ML model; (2) deep learning directly on raw images

---

### 2.3 Drunk Driving Detection
- Most existing studies use **simulators** (not real vehicles): fixed-frame simulators, stationary cars in front of screens
- Some use **intoxication-simulation goggles** rather than actual alcohol — validity issues
- **Major limitation:** most studies tested on participants already in the training set → poor generalizability
- Only one out-of-sample validated method exists prior to this study: Koch & Maritsch et al. (CHI '23)
  - Simulator study, n=30, AUROC 0.88 (Early Warning), 0.79 (Above Limit) — this is the **"original study"** used as baseline

---

### 2.4 Importance of Replication and Real Vehicle Studies
- Simulator-to-real-vehicle transfer is debated: some studies affirm, others show inconsistencies
- Three factors limiting simulator generalizability:
  1. Varying degrees of realism / simulator fidelity
  2. Absence of external real-world influences
  3. Modified driver behavior due to lack of genuine risk
- HCI has a known **replication crisis** (driven by emphasis on novelty); RepliCHI series (2011–2014) addressed this
- This study is a **conceptual replication** of Koch & Maritsch et al., adapted for real-vehicle environment

---

## 3. Data Collection

### Study Design
- **Randomized, controlled, interventional single-center study**
- Registered: ClinicalTrials.gov NCT05796609
- Ethics approved: Bern, Switzerland (ID 2022-02245)
- Conducted: April–July 2023
- Helsinki Declaration + good clinical practice guidelines followed

| Group | Masking | Treatment |
|---|---|---|
| **Treatment** | Single-blinded | Alcoholic drink |
| **Placebo** | Single-blinded | Non-alcoholic placebo drink |
| **Reference** | Unblinded (open-label) | No drink |

> Placebo group: controlled for expectancy effects and compensatory behaviors  
> Reference group: controlled for training effects (track familiarity), drowsiness, and environmental changes (e.g., sunlight variation)

---

### 3.1 Participants

- **n = 54** analyzed (55 eligible; 1 excluded due to CAN data errors)
- Treatment: n=31 | Placebo: n=12 | Reference: n=11
- Eligibility: valid Swiss driving license, age 21+, driven actively in past 6 months, occasional alcohol use
- Exclusions: health conditions, medications, excessive alcohol use (PEth >200 ng/mL or AUDIT ≥15), pregnancy, drug abuse
- **Screening tools:**
  - **PEth (phosphatidylethanol):** blood biomarker for chronic excessive alcohol use; threshold >200 ng/mL
  - **AUDIT:** 10-question WHO screening tool; excluded if score ≥15

| Characteristic | Treatment (n=31) | Placebo (n=12) | Reference (n=11) |
|---|---|---|---|
| Age | 37.5 ± 14.7 | 37.0 ± 17.0 | 36.5 ± 14.6 |
| Sex | 16F / 15M | 6F / 6M | 6F / 5M |
| Driver experience (yrs) | 18.5 ± 14.5 | 17.2 ± 17.4 | 17.4 ± 14.3 |
| AUDIT score | 4.81 ± 2.44 | 4.92 ± 2.02 | 3.82 ± 1.99 |

---

### 3.2 Alcohol Administration and Measurement

- Target BAC: **0.08 g/dL** (calculated individually using **Widmark formula** — accounts for sex, weight, age, height)
- Drink: vodka + orange juice (bitter variant to mask vodka; stored at -18°C; dispensed in neutral narrow-outlet bottles)
- Three driving phases for treatment group:
  1. **No alcohol** (BAC = 0.00 g/dL) — baseline / negative class
  2. **Severe** (BAC > 0.05 g/dL) — above WHO limit; commenced after BAC peaked then dropped below 0.075 g/dL
  3. **Moderate** (BAC < 0.05 g/dL) — commenced after BAC dropped below 0.035 g/dL
- BAC measured by **Dräger 6820** (professionally licensed in Switzerland); conversion factor: BrAC × 0.2 = BAC
- First measurement: 20 minutes post-consumption (to avoid mouth alcohol distortion)
- Placebo/reference groups followed identical timing but without alcohol

---

### 3.3 Driving

- **Vehicle:** 2020 Volkswagen Touran 1.5 TSI (110 kW, automatic, 7 seats, dual pedals)
- A licensed driving instructor sat in the passenger seat (blinded to BAC); dual pedals for emergency control
- **Three driving scenarios** per phase (random order):
  - **Highway:** max 80 km/h, straight roads, no stops
  - **Rural:** max 60 km/h, stop sign, one obstacle
  - **Urban:** max 50 km/h, multiple turns, crosswalk, simulated parked vehicles (cones)
- Test track: closed-off in Switzerland; varied road widths 6–10 m; developed with Automobile Club of Switzerland

---

### 3.4 Data Sources

| Source | What it captures |
|---|---|
| **DMC** | Near-infrared camera (Robert Bosch GmbH), mounted on steering column; 50 fps; detects face, eyes, pupils, gaze vector, head pose |
| **CAN bus** | Vehicle controls (brake, gas, steering) and dynamics (speed, yaw, acceleration) |

- Both resampled to **50 Hz** for consistency
- Missing values: linear interpolation (numerical), nearest-neighbor (categorical); gaps >5 consecutive entries omitted

---

## 4. Machine Learning Detection Approach

### Overview
- **Sliding window** (60-second window, 1-second step) + **logistic regression with Lasso (L1) regularization**
- 60s window = 3,000 samples (50 Hz × 60s); windows with <75% expected samples excluded
- Total features generated: **580**

### Two Classification Tasks

| Task | Positive class | Negative class |
|---|---|---|
| **Early Warning** | BAC > 0.00 g/dL (any intoxication) | Sober (phase 1) |
| **Above Limit** | BAC > 0.05 g/dL (WHO limit) | Sober + moderate (phases 1 and 3) |

---

### 4.1 Feature Groups (DMC)

| # | Group | What it captures | Count |
|---|---|---|---|
| 1 | **Head movement** | Linear + rotational velocity and acceleration (3 spatial components + magnitude) | 160 |
| 2 | **Eye state** | Binary open/closed signal per eye (blink patterns) | 6 |
| 3 | **Eye movement** | Gaze azimuth/elevation velocity and acceleration; gaze movement angle | 90 |
| 4 | **Gaze events** | Fixations and saccades (duration, amplitude, velocity) via REMoDNaV algorithm | 104 |
| 5 | **Region-specific gaze events** | Fixations assigned to 10 predefined gaze regions (windscreen, mirrors, instruments, etc.) | 20 |

> **Fixations** = gaze stable at one point; **Saccades** = rapid movements between fixations  
> REMoDNaV: min fixation duration 40ms; min saccade duration 10ms

---

### 4.2 Feature Groups (CAN)

| # | Group | Signals |
|---|---|---|
| 6 | **Controls interaction** | Brake pedal, gas pedal, steering wheel — position, velocity, acceleration, **jerk** |
| 7 | **Vehicle dynamics** | Longitudinal/lateral/yaw velocity, acceleration, jerk |

> **Jerk** = 3rd derivative of position (rate of change of acceleration); critical for vehicle stability and ride comfort analysis

**Statistical aggregation functions applied to all features:**
mean, median, standard deviation, IQR, 0.05/0.95 quantiles, skewness, kurtosis, power, number of sign changes

---

### 4.3 Model Evaluation

- **Leave-One-Subject-Out (LOSO) cross-validation**: train on n-1 participants, test on remaining; repeat for each
- **Primary metric: AUROC** (threshold-agnostic; handles imbalanced data well)
- Additional metrics: AUPRC, balanced accuracy, F1 score
- Robustness tested across: window sizes (5–300s), individual feature groups, different classifiers

---

## 5. Results

### 5.1 Performance Summary

| Task | Modality | AUROC |
|---|---|---|
| **Early Warning** | DMC + CAN | **0.84 ± 0.11** |
| **Early Warning** | DMC only | 0.79 ± 0.12 |
| **Early Warning** | CAN only | 0.75 ± 0.13 |
| **Above Limit** | DMC + CAN | **0.80 ± 0.10** |
| **Above Limit** | DMC only | 0.75 ± 0.10 |
| **Above Limit** | CAN only | 0.72 ± 0.10 |

> Combined modality always outperforms single modality. Early Warning consistently outperforms Above Limit.

### Confusion Matrix Highlights
- Early Warning FN rate: 30% for moderate; 17% for severe (more pronounced symptoms = easier classification)
- Above Limit FP rate: 36% for moderate; 16% for sober participants
- Pattern consistent with original simulator study

### Performance by Scenario
- Early Warning: best in rural (0.87), lower in urban (0.83)
- Above Limit: best in urban (0.82), lowest on highway (0.79)

---

### 5.2 Robustness Analysis
- AUROC improves with larger window sizes; diminishing returns beyond ~60s
- Feature groups provide **complementary information** (individual groups perform lower than combined)
- Performance **stable across classifier types** (logistic regression, SVM, random forest, gradient boosting, MLP)

---

### 5.3 Most Important Feature Groups (by coefficient share)

| Feature Group | Early Warning | Above Limit | Source |
|---|---|---|---|
| Head movement | 31% | 30% | DMC |
| Controls interaction | 21% | 16% | CAN |
| Eye movement | 18% | 17% | DMC |
| Gaze events | 18% | 18% | DMC |
| Vehicle dynamics | 11% | 11% | CAN |
| Region-specific gaze | 3% | 3% | DMC |
| Eye state | 2% | 2% | DMC |

---

### 5.4 Control Group Incorporation
- With control groups included: Early Warning AUROC 0.80 ± 0.11; Above Limit 0.80 ± 0.09
- Slight decrease in Early Warning AUROC (was 0.84 without controls) — expected due to training on more diverse sober data
- Results remain consistent — confirms system robustness against confounds

---

## 6. Discussion

### 6.1 Post-Hoc Interpretation

> Drunk drivers exhibit **diminished psychomotor skills, impaired perception, and divided attention**.

Model-captured physiological patterns:
- **Fewer saccades**, slower movements, decreased amplitudes, increased variability under alcohol
- **Longer fixation durations** under alcohol (consistent with prior studies)
- Braking, accelerating, and steering all impacted
- Features like **standard deviation of steering wheel acceleration** reflect known aggressive drunk driving behavior

---

### 6.2 Comparison to Previous Work

| Study | Setting | n | Method | Early Warning AUROC | Above Limit AUROC |
|---|---|---|---|---|---|
| Koch & Maritsch et al. (CHI '23) — *original* | Simulator | 30 | DMC only | 0.88 ± 0.09 | 0.79 ± 0.10 |
| Koch & Maritsch et al. (CHI '23) — *original* | Simulator | 30 | DMC + CAN | 0.91 ± 0.07 | 0.81 ± 0.11 |
| US NHTSA (CAN only, 0.08 threshold) | Simulator | — | CAN | 0.77 ± 0.08 | — |
| **This study** | **Real vehicle** | **54** | **DMC + CAN** | **0.84 ± 0.11** | **0.80 ± 0.10** |

> Performance on a real test track is **comparable** to the simulator baseline. The study successfully replicated simulator findings in a real-world setting.

---

### 6.3 Risk Mitigation Interventions
- After detecting intoxication, **personalized digital interventions** can be deployed:
  - Auditory, visual, or tactile in-vehicle warnings
  - ADAS adjustments (e.g., earlier brake triggering knowing driver is impaired)
  - Last resort: vehicle brought to a stop (requires further refinement given current FP rates)
- Drivers who **underestimate their own BAC** are particularly high-risk — warnings especially useful here

---

### 6.4 Privacy and Ethical Considerations

> Continuous driver monitoring involves processing **highly sensitive data**.

- System does **not identify specific individuals** — deliberately avoided personalization (no individualized decision thresholds)
- Only needs **last 60 seconds** of DMC + CAN data; all calculations done **on-board (edge computing)**
- EU GDPR principles apply: lawful processing, purpose limitation, data minimization, storage limitation, security
- Current EU regulations (drowsiness/distraction detection) need to be **extended to cover impairment detection**
- Risks of AI bias acknowledged; interpretable ML and diverse participants used to mitigate
- Source code published for transparency

---

### 6.5 Limitations and Future Work

- **n=54** limits diversity; ethnicity not recorded (eye-tracking performance can vary across ethnicities)
- Participants with eye-related health issues may affect DMC performance
- Older and novice drivers have different glance behaviors — not fully accounted for
- No comparison of advanced ML models (deep learning, etc.) — only basic models used
- Test track lacks: other road users, non-driving distractions, nighttime driving, real traffic
- Fully autonomous vehicles will reduce relevance of CAN features; DMC-only still viable (saccades and fixations consistent across driving modes)
- Future studies should validate in **real-world traffic** with legal exemptions and safety drivers

---

## 7. Conclusion

> The test track study successfully replicated simulator findings, confirming the generalizability of DMC + CAN-based drunk driving detection.

- Used human-interpretable features and parsimonious logistic regression — grounded in established physiology
- First clinical trial study using real intoxicated drivers on a test track for drunk driving detection
- Robust across unseen drivers, scenarios, and design choices
- Sets the stage for **digital interventions** (in-vehicle warnings, ADAS integration) that can significantly reduce societal harm from drunk driving

---

## Quick Reference: Key Terms and Concepts

| Term | Definition |
|---|---|
| **BAC** | Blood Alcohol Concentration (g/dL); WHO limit = 0.05 g/dL |
| **BrAC** | Breath Alcohol Concentration; BrAC × 0.2 = BAC (Swiss regulation) |
| **DMC** | Driver Monitoring Camera — near-infrared; captures face, eyes, gaze |
| **CAN bus** | Controller Area Network — in-vehicle communication system for sensors/controls |
| **AUROC** | Area Under the ROC Curve — primary performance metric; 1.0 = perfect, 0.5 = random |
| **AUPRC** | Area Under the Precision-Recall Curve |
| **LOSO** | Leave-One-Subject-Out cross-validation — tests on unseen participants |
| **Early Warning** | Classification task: sober (BAC=0) vs. any intoxication (BAC>0) |
| **Above Limit** | Classification task: below WHO limit vs. above 0.05 g/dL |
| **Lasso (L1)** | Regularization method that shrinks irrelevant features to zero (feature selection) |
| **Sliding window** | 60s window, 1s step; captures temporal dynamics of time-series driving data |
| **Saccade** | Rapid eye movement between fixation points |
| **Fixation** | Gaze stable at one point (min 40ms) |
| **Jerk** | 3rd derivative of position; rate of change of acceleration |
| **Widmark formula** | Calculates required alcohol dose to reach target BAC, based on sex/weight/age/height |
| **PEth** | Phosphatidylethanol — blood biomarker for chronic excessive alcohol use |
| **AUDIT** | WHO 10-question screening tool for harmful alcohol use |
| **RepliCHI** | CHI series (2011–2014) promoting replication studies in HCI |
| **ADAS** | Advanced Driver-Assistance Systems — active safety systems in modern vehicles |

---

## Performance Numbers Cheat Sheet

| Configuration | Early Warning AUROC | Above Limit AUROC |
|---|---|---|
| DMC + CAN (main result) | **0.84 ± 0.11** | **0.80 ± 0.10** |
| DMC only | 0.79 ± 0.12 | 0.75 ± 0.10 |
| CAN only | 0.75 ± 0.13 | 0.72 ± 0.10 |
| With control groups | 0.80 ± 0.11 | 0.80 ± 0.09 |
| Original simulator (Koch et al.) DMC | 0.88 ± 0.09 | 0.79 ± 0.10 |
| Original simulator (Koch et al.) DMC+CAN | 0.91 ± 0.07 | 0.81 ± 0.11 |


# Synthetic Human Memories: AI-Edited Images and Videos Can Implant False Memories and Distort Recollection

**Authors:** Pat Pataranutaporn, Chayapatr Archiwaranguprok, Samantha W. T. Chan, Elizabeth Loftus, Pattie Maes  
**Institutions:** MIT Media Lab; University of the Thai Chamber of Commerce; UC Irvine  
**Published:** CHI '25, April 26–May 1, 2025, Yokohama, Japan  
**DOI:** https://doi.org/10.1145/3706598.3713697  
**Pre-registered:** AsPredicted #188511

---

## 1. Introduction

> False memories are recollections of events that either never occurred or are significantly distorted from reality. Unlike misinformation, false memories are particularly insidious because the individual **genuinely believes** they are accurate — making them resistant to correction.

### Why This Matters Now
- AI editing tools are increasingly embedded in everyday apps (Instagram, TikTok, Google Photos, Apple Photos, Samsung Galaxy AI)
- Google's "Best Take" can remove unwanted elements automatically — potentially without the user's knowledge
- Generative AI models (OpenAI Sora, Luma's Dream Machine, Kling) can animate static images into realistic videos
- Prior false memory research used **manually edited** images in controlled lab settings — this study is the first to examine **AI-generated** edits at scale

### Deepfakes vs. AI-Edits — A Critical Distinction
- **Deepfakes:** entirely fabricated content, often for malicious disinformation; people tend to be vigilant
- **AI-edits:** modify *existing* content, subtly altering genuine memories or experiences; people are **less aware** and more susceptible

### Key Concern
> "Externalizing" memories (storing them as photos/videos) may fundamentally alter how we remember — especially when AI modifies those externalized memories.

### Positive Potential
- Therapeutic memory reframing (PTSD, phobias, anxiety)
- Self-esteem enhancement (visualizing past achievements more positively)

### Research Questions
1. To what extent do AI-edited images influence memory of the original scenario vs. control?
2. Does converting images to AI-generated videos further exacerbate false memories (count and confidence)?
3. How do different types of AI editing (people, objects, environment) affect false memory severity?
4. What factors (age, gender, AI familiarity, memory efficacy, skepticism, education) moderate false memory formation?

---

## 2. Related Work

### 2.1 Memory Augmentation and Vulnerability in HCI
- HCI has long explored memory augmentation: wearable "remembrance agents," life-logging, AR memory cues, conversational AI memory assistants
- **Engelbart (1962):** pioneering vision of computers as extensions of human cognitive processes
- **Key risk:** externalizing memories to digital files leaves users vulnerable to manipulation — both intentional and unintentional
- When memories are stored digitally, they become susceptible to alteration; AI makes this manipulation more accessible and automated

---

### 2.2 AI-Generated Media and Misinformation
- **Misinformation:** spread of falsehoods regardless of intent
- **Disinformation:** deliberately misleading content / propaganda
- AI-generated content shown to influence people's attitudes; factors that make it disruptive include authoritative tone, persuasive language, and targeted personalization
- Social robots providing incorrect information had an influence **comparable to humans** — 77% of falsely provided words were incorporated into participants' memories as errors (Huang et al., 2023)
- AI hallucination adds another layer: models can generate false information unintentionally

---

### 2.3 False Memories Research

> **Loftus and colleagues** established false memories as a central area of psychological research. Human memory is remarkably malleable.

#### Landmark Studies
- **Loftus & Palmer (1974):** Verb choice in questioning (e.g., "smashed" vs. "hit") altered participants' speed estimates of a witnessed car accident → language shapes memory
- **"Lost in the Mall" experiment (Loftus & Pickrell, 1995):** Implanted entirely false childhood memories; 25% false memory rate. Replication (Murphy et al., 2023) with larger sample found **35% false memory rate**
- **Wade et al. (2002):** "A picture is worth a thousand lies" — 50% of participants developed false memories after viewing fake childhood photos + guided imagery

#### Visual Stimuli and False Memories
- Visual stimuli can generate false memories of fictitious events
- Methods: presenting scenes with omitted elements, personal photos, narrative instructions
- VR introduces **source confusion** between real and virtual experiences
- Chatbot vulnerabilities: misinformation can be injected alongside personal knowledge

---

## 3. Methodology

### Study Design
- **Pre-registered between-group experiment** (AsPredicted #188511)
- **n = 200 participants**, U.S. residents, ages 20–73 (M=38, SD=12.25), 1:1 female:male ratio
- Recruited via **CloudResearch**; conducted via **Qualtrics**
- **50 participants per condition** (4 conditions)
- IRB approved

### 2×2 Experimental Design

| | Unedited Images | AI-Edited Images |
|---|---|---|
| **Static** | Control | AI-Edited Images |
| **Dynamic (Video)** | AI-Gen Videos of Unedited Images | AI-Gen Videos of AI-Edited Images |

---

### Stimulus Set
- **24 copyright-free images** across 3 content types: daily life, news, documentary/archival
- **12 images AI-edited** using **Adobe Photoshop AI**; 12 images kept as internal controls (same across all conditions)
- **Videos:** created using **Luma's Dream Machine** (image-to-video); 5 seconds each

### Three Types of AI Edits
| Edit Type | Examples |
|---|---|
| **People** | Changing facial expression, changing runner's ethnicity, changing gender in group |
| **Environment** | Removing ice melt, changing time of day, changing background setting |
| **Objects** | Adding military vehicle, removing military uniforms, adding a stop sign |

---

### Procedure
1. Consent form (disclosed possible deception)
2. Attention check
3. View **24 original unedited images** — 2 minutes, Instagram-like swipeable interface
4. **Filler task:** 2-minute Pac-Man game (clears working memory without inducing heavy natural forgetting)
5. View **second set of 24 stimuli** (condition-dependent), labeled "AI-enhanced image" — 2 minutes
6. Second attention check
7. **Memory Test Questionnaire:** 24 questions about the *original* images; each with a masked version of the image
8. Demographic + moderating factors survey

> The 2-minute viewing time was chosen to allow processing of each image while preventing unnatural detailed memorization.

---

### Measurement

#### Memory Classification
- **False memory:** incorrect answer
- **Uncertain:** "unsure" response
- **Non-false memory:** correct answer

#### Confidence Scale
- 7-point scale: 1 (extremely lacking confidence) → 7 (extremely confident)

#### Weighted Score
- False = **-1**, Uncertain = **0**, Non-false = **+1**
- Weighted by confidence level, then summed per participant
- Higher score = better memory accuracy with confidence

#### Moderating Factors Measured
| Factor | Scale |
|---|---|
| AI Filter Familiarity | 7-point (1=not familiar, 7=very familiar) |
| Frequency of Forgetting | 7-point (1=major problems, 7=no problems) |
| Memory Efficacy | 7-point subset scale |
| Skepticism toward media/institutions | 7-point (e.g., "The official media provides false information") |

---

### Statistical Analysis
- Normality tested with **Shapiro-Wilk test**
- If non-normal: **Kruskal-Wallis** → post hoc **Dunn test** (Bonferroni/FDR correction)
- If normal: **Levene test** for homogeneity → **Welch ANOVA** (heterogeneous) or **ANOVA** (homogeneous) → **Tukey's HSD**
- Moderating factors: **mixed-effects regression model**

---

## 4. Results — Primary Analysis

### 4.1 Number of False Memories

**Result: H=34.157, P=1.836e-07 — Significant**

| Condition | Mean (%) | False Memories out of 12 | Multiplier vs. Control |
|---|---|---|---|
| Control (unedited images) | 18.878 | 2.265 | 1.0× |
| AI-gen videos of unedited images | 23.667 | 2.840 | **1.25×** |
| AI-edited images | 31.373 | 3.765 | **1.67×** |
| **AI-gen videos of AI-edited images** | **38.667** | **4.640** | **2.05×** |

> **AI-generated videos of AI-edited images had the strongest effect: 2.05× the false memories of the control.**

Post hoc (FDR corrected): Control vs. AI-edited images (P=2.5e-4); Control vs. AI-gen videos of AI-edited images (P=7.654e-08); AI-gen unedited vs. AI-gen AI-edited (P=6.153e-05) — all significant.

---

### 4.2 Non-False Memories

**Result: H=30.448, P=1.111e-06 — Significant**

All three edited conditions showed fewer correct memories compared to control: 0.88×, 0.82×, and **0.67×** respectively. No significant differences in uncertain memories.

---

### 4.3 Confidence in False Memories

**Result: H=8.581, P=0.0354 — Significant**

| Condition | Mean Confidence | Multiplier vs. Control |
|---|---|---|
| Control | 4.536 | 1.0× |
| AI-edited images | 5.027 | **1.10×** |
| **AI-gen videos of AI-edited images** | **5.412** | **1.19×** |

> Not only do AI-edited videos create more false memories — participants are also **more confident** in those false memories. No significant differences in confidence for uncertain or non-false memories.

---

### 4.4 Weighted Score

**Result: ANOVA, F=14.577, P=1.312e-08 — Highly Significant**

| Condition | Weighted Score (higher = better) |
|---|---|
| Control | 32.061 |
| AI-gen videos of unedited images | 24.760 |
| AI-edited images | 15.803 |
| **AI-gen videos of AI-edited images** | **3.040** |

The weighted score systematically decreases with AI manipulation — worst in the combined video + edit condition.

---

### 4.5 Group Homogeneity Check
- 12 identical images embedded across conditions as internal controls
- Kruskal-Wallis on these identical images: all P-values 0.425–0.927 (not significant)
- Confirms **group homogeneity** — differences are due to experimental conditions, not pre-existing group differences

---

## 5. Results — Additional Analyses

### 5.1 False Memories by Image Content Type

> The effect is **consistent across all content types** — not limited to any specific domain.

| Content Type | H | P-value |
|---|---|---|
| Daily Life | 12.884 | 0.00489 |
| News | 27.712 | 4.174e-06 |
| Documentary/Archive | 23.617 | 3.003e-05 |

All three show a clear increasing trend from unedited → AI-gen videos of AI-edited images.

---

### 5.2 False Memories by Type of Edit

| Edit Type | Increase (AI-gen video of AI-edit vs. Control) | Highest Absolute % |
|---|---|---|
| **People** | 2.4× | **45.3%** (highest absolute) |
| **Environment** | **2.6×** (highest relative increase) | 33.3% |
| **Objects** | 2.3× | 36.7% |

Key insight: people edits produce the most false memories in absolute terms (people are complex, harder to recall); environmental edits show the most dramatic relative increase (context is less carefully attended to initially).

---

### 5.3 Moderating Factors (Mixed-Effects Regression)

| Factor | Coefficient | P-value | Significant? |
|---|---|---|---|
| AI Filter Familiarity | 0.040 | 0.650 | No |
| **Age** | **-0.031** | **0.010*** | **Yes (small negative effect)** |
| Gender (male vs. female) | -0.040 | 0.891 | No |
| Education Level | 0.103 | 0.389 | No |
| Cognitive Load | -0.133 | 0.262 | No |
| Memory Efficiency | -0.069 | 0.232 | No |
| Skepticism toward Media | -0.021 | 0.169 | No |

> **Only age was significant** — younger people were slightly more susceptible (small effect). No other factor mattered significantly.

Key interpretation: familiarity with AI is NOT protective; even **skeptical individuals** were not protected — false memory formation operates beyond "trust vs. mistrust." Anyone, regardless of background, is potentially vulnerable.

---

## 6. Discussion

### 6.1 AI-Edited Content Boosts False Memories with Alarming Confidence

> The combination of false memories **and** high confidence is particularly dangerous — people are more likely to believe and act upon incorrect information they perceive as true.

- Implications: eyewitness testimony, legal proceedings, political misinformation, spread of false beliefs
- Even brief single exposure causes significant effects — real-world repeated exposure would likely worsen outcomes

---

### 6.2 The Impact of Labels

- All AI-edited visuals were presented **with an "AI-enhanced image" label**
- Despite this label, significant false memory formation still occurred
- Passive notifications alone are **insufficient** to mitigate cognitive biases from manipulated media
- When people encounter plausible altered content, they integrate it into memory **regardless of labels**
- Implication: we need designs that **actively provoke critical engagement**, not just passive disclosure

---

### 6.3 Negative Implications

#### Wrongful Legal Accusations
- AI-manipulated content going viral can rapidly distort public perception and witness memories
- Case of Steve Titus: wrongfully convicted (1980) based on a witness's increased confidence in an initially uncertain identification — demonstrates memory distortion's devastating legal consequences
- Witnesses who see manipulated media before testifying may unknowingly incorporate false details with inflated confidence

#### Public Misinformation Spread
- AI could alter protest footage to appear violent; individuals who saw the real event may later misremember it as violent
- 2024 US election concerns: crowd sizes at political events; attendees' memories could be distorted by later AI-edited imagery
- Polarizes societal beliefs; erodes trust in **all** visual content — including authentic ones

#### Reinforcement of Biases and Stereotypes
- AI edits could systematically conform media to stereotypical representations of groups
- Creates feedback loop: AI-generated biased content → false memories → reinforced prejudice
- Particularly dangerous for racial, gender, and cultural bias

#### Mitigating AI-Implanted False Memories
- Detection tools, regulatory frameworks, and notification systems are vital but underutilized and insufficient alone
- Need mechanisms that encourage **active critical engagement**
- Future work must unite psychology, HCI, and AI experts

---

### 6.4 Positive Use Cases

**Therapeutic Memory Reframing:** AI modifies distressing elements in photos/videos under professional supervision; could reduce emotional charge of PTSD memories, phobias, anxiety disorders. Requires transparency and informed consent.

**Enhancing Self-Esteem:** AI enhances images of past achievements to boost confidence; aligns with visualization techniques from sports psychology. Example: enhancing a public speaking memory to reduce future anxiety.

---

## 7. Limitations and Future Work

- **Short-term exposure:** single viewing session; real-world repeated exposure would likely intensify effects (Loftus research shows repeated suggestion amplifies false memory implantation)
- **Sample constraints:** U.S.-only; 24 pre-selected images rather than personal photos reduces ecological validity
- **Only visual media:** future work should examine AI-edited audio and text
- **No self-editing condition:** future work should test whether people who edit their own photos later forget they did so (and experience similar false memory effects)
- **No forgetting analysis:** study did not examine AI *removing* elements vs. adding them
- **Controlled setting:** field experiments and ecological momentary assessments needed for real-world validity
- **Ethical future work:** long-term psychological effects, informed consent, equitable access to protective measures

---

## 8. Conclusion

> AI-edited media significantly increases false memory formation. AI-generated videos of AI-edited images have the **greatest effect** (2.05× false memories, 1.19× confidence vs. control). The effect is consistent across content types, demographic groups, and even people who are skeptical of media.

Key takeaways: anyone regardless of background can fall victim; labels don't work as passive interventions; active engagement mechanisms are needed; interdisciplinary collaboration (psychology, HCI, AI, policy) is essential.

---

## Quick Reference Cheat Sheet

### Key Results

| Condition | False Memory Multiplier | Confidence Multiplier |
|---|---|---|
| Control (unedited) | 1.0× | 1.0× |
| AI-gen video of unedited | 1.25× | not significant |
| AI-edited images | 1.67× | 1.10× |
| **AI-gen video of AI-edited** | **2.05×** | **1.19×** |

### Edit Type Effects (in AI-gen video of AI-edit condition vs. control)
- People: 2.4× — highest **absolute** false memories (45.3%)
- Environment: **2.6×** — highest **relative** increase
- Objects: 2.3×

### Key Terms

| Term | Definition |
|---|---|
| **False Memory** | Recollection of an event that never occurred or is significantly distorted |
| **Misinformation effect** | Post-event information alters memory of an original event (Loftus) |
| **Weighted score** | False=-1, Uncertain=0, Non-false=+1, multiplied by confidence — composite accuracy |
| **Kruskal-Wallis** | Non-parametric test for 3+ groups with non-normal data |
| **Tukey's HSD** | Post hoc pairwise comparisons after ANOVA |
| **Dunn test (FDR)** | Post hoc pairwise comparisons after Kruskal-Wallis |
| **Luma's Dream Machine** | AI image-to-video tool used to create 5-second videos |
| **Adobe Photoshop AI** | Tool used to add, remove, or alter image elements |
| **"Lost in the Mall" (1995)** | Seminal Loftus study; 25% false memory rate (replicated at 35%) |
| **Wade et al. (2002)** | "A picture is worth a thousand lies" — 50% false memories from fake childhood photos |

